 Stock Sentiment Analysis


This project analyzes the sentiment around Tesla (TSLA) by scraping Reddit posts from the popular subreddit r/wallstreetbets. It aims to correlate the online sentiment with Tesla’s historical stock price using various data visualizations and sentiment analysis techniques.

# Project Overview

## Data Collection:

Scrapes Reddit posts mentioning TSLA using the Reddit API.
Extracts key information such as the post title, text, upvotes, and creation time.


## Sentiment Analysis:

Uses the VADER sentiment analyzer to determine whether each post is Positive, Neutral, or Negative.
Saves sentiment results to a CSV file for further analysis.


## Data Visualization & Correlation:

Visualizes the frequency of mentions and sentiment trends over time.
Correlates sentiment with Tesla's historical stock price data using heatmaps and time-series plots.

## Installation and Setup

### Dependencies
To run this project, you need the following Python libraries:

praw - For scraping Reddit data.
vaderSentiment - For sentiment analysis.
yfinance - For fetching stock market data.
pandas - For data manipulation.
matplotlib & seaborn - For plotting and visualizations.

### Install all dependencies with:
'''pip install praw vaderSentiment yfinance pandas matplotlib seaborn'''



## Project Setup


### 1. API Credentials:
To scrape Reddit data, you'll need Reddit API credentials:

Go to Reddit's Developer Portal and create an app.

Copy your client_id, client_secret, and user_agent.

Update the following lines in the code with your credentials:

'''reddit = praw.Reddit(
    client_id='YOUR_CLIENT_ID',
    client_secret='YOUR_CLIENT_SECRET',
    user_agent='YOUR_USER_AGENT'
)'''


### 2. Scraping Reddit Posts:
   
The script queries up to 1,000 posts from the r/wallstreetbets subreddit mentioning "TSLA".
Extracts the title, text, upvotes, and created_at of each post.
Saves the data to a CSV file: reddit_stock_data.csv.

### 3. Perform Sentiment Analysis:
   
The script uses VADER to analyze the sentiment of each post and classifies them as Positive, Neutral, or Negative.
Results are saved to reddit_stock_sentiment.csv.

### 4. Fetch Historical Stock Data:
   
Retrieves Tesla (TSLA) stock price data from 2019 to the present using the yfinance API.
The stock data is saved in his_stock_data.csv.

### 5. Correlation and Visualization:
   
The script generates insightful visualizations:
Frequency of mentions of TSLA over time.
7-day rolling average of sentiment trends.
Heatmaps showing correlations between stock price changes and sentiment.


# How to Run the Project

Set Up API Credentials:

Update the client_id, client_secret, and user_agent in the code with your Reddit API credentials.

Run the Script:

Run the script to scrape Reddit, analyze sentiment, and fetch stock data.
Visualizations will be displayed automatically, and CSV files will be generated.

 After setting up, run the code blocks to:
 1. Scrape Reddit posts
 2. Perform sentiment analysis
 3. Fetch historical stock data
 4. Visualize correlations
    
##  Files and Outputs
reddit_stock_data.csv: Contains scraped Reddit data (post title, text, upvotes, created_at).
reddit_stock_sentiment.csv: Contains sentiment analysis results (positive, neutral, negative).
his_stock_data.csv: Historical stock data for Tesla (TSLA) (2019-2024).
Visualizations: The script generates visualizations like sentiment trends and correlation heatmaps.

## Visualization Examples
Frequency of Mentions: Number of times "TSLA" was mentioned in Reddit posts over time.
Sentiment Trends: Rolling 7-day average for positive, negative, and neutral sentiments.
Correlation Heatmaps: Shows the relationship between stock price changes and sentiment trends.


 ## Conclusion
This project demonstrates the relationship between Reddit sentiment and Tesla’s stock performance. By scraping posts, analyzing sentiment, and comparing it to historical stock data, it highlights how online discussions can potentially influence stock market trends.

