# :bird: Twitter dashboard

[![License: CC BY-SA 4.0](https://img.shields.io/badge/License-CC%20BY--SA%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)

A simple Panel-based dashboard visualizing geotagged tweets with hvplot and Datashader.

The dashboard includes:

- An heatmap showing the number of tweets;

- A bar plot showing the 5 most common languages within the current map extent;

- A [wordcloud](https://amueller.github.io/word_cloud/) image showing the 10 most popular hashtags within the current map extent;

- Two numeric indicators showing the number of tweets and unique users on a daily basis within the current map extent;

- Two line charts showing the number of tweets and unique users on a daily basis within the current map extent;

### The dashboard in action!!! :tv:

<img src="https://github.com/ivandorte/panel-geodashboard-twitter/blob/main/art/twitter_dashboard.gif" width="400"/>

### Twitter data ([link](https://github.com/ivandorte/panel-geodashboard-twitter/blob/main/data/rome_tweets.parquet))

This dataset contains over 400k geotagged tweets in parquet format:

- Coverage: Historic Centre of Rome, Italy;

- [EPSG:3857](https://epsg.io/3857);

- Year: 2018;

- Language: Multi;

- Source: This dataset was scraped by myself with snscrape; 

| Column | Description |
| ------------- | ------------- |
| tweet_date (index) | Tweet creation date |
| user_id | Unique identifier of the tweet author |
| user_location | User location information |
| tweet_id | Unique identifier of the tweet |
| tweet_text | Tweet content |
| tweet_hashtags | Comma separated list of the tweet hashtags |
| tweet_lang | Tweet language |
| x | x-coordinate of the tweet |
| y | y-coordinate of the tweet |

## Set up
To run this dashboard you will need to do the following steps:

1. Git clone this repository:

`git clone git@github.com:ivandorte/panel-geodashboard-twitter.git`

`cd panel-geodashboard-twitter`

2. Install the required Python packages:

`python -m pip install -r requirements.txt`

3. Run the app

`panel serve app.py --show`

The dashboard will be available in your web browser!!!