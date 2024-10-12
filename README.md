Stock Sentiment Analysis 

Project Overview
This project scrapes Reddit posts from the popular subreddit "r/wallstreetbets," extracts sentiment around a stock for this project i have used "Tesla" (TSLA),
and correlates the sentiment with Tesla’s historical stock price. The project consists of three main parts:

Data Collection:
Scraping posts mentioning TSLA using Reddit's API.

Sentiment Analysis:
Analyzing the sentiment of Reddit posts using VADER.

Data Visualization & Correlation: 
Comparing sentiment trends with Tesla’s stock price data using visualizations.

Installation and Setup
Dependencies
To run the project, you'll need to install the following Python libraries:

praw - For scraping Reddit data.
vaderSentiment - For sentiment analysis.
yfinance - For fetching stock market data.
pandas - For data manipulation.
matplotlib and seaborn - For plotting and data visualization.

You can install these dependencies using pip:
pip install praw vaderSentiment yfinance pandas matplotlib seaborn

Project Setup

API Credentials:

To scrape Reddit data, you will need to have Reddit API credentials:
Go to Reddit's Developer Portal and create an app.
Note the client_id, client_secret, and user_agent that will be required to access Reddit data.
Configure API Credentials: Open the code and set up your Reddit API credentials in the following lines:


reddit = praw.Reddit(
    client_id='YOUR_CLIENT_ID',
    client_secret='YOUR_CLIENT_SECRET',
    user_agent='YOUR_USER_AGENT')
    

Scraping Reddit Posts:

The script queries Reddit for up to 1,000 posts mentioning "TSLA" from the r/wallstreetbets subreddit.
Extracts the title, text, upvotes, and creation time for each post.
Saves the results into a CSV file: reddit_stock_data.csv.
Perform Sentiment Analysis:

Using the VADER sentiment analyzer, the script processes the post text and categorizes each as Positive, Neutral, or Negative.
Sentiment scores are saved into a CSV file: reddit_stock_sentiment.csv.
Fetch Historical Stock Data:

Historical stock price data for Tesla (TSLA) from 2019 to the present is downloaded using the yfinance API.
The stock data is saved into his_stock_data.csv.


Correlation and Visualization:

The project includes code to correlate the frequency of mentions and sentiment with stock price changes.
The code generates visualizations like:
Frequency of TSLA mentions over time.
7-day rolling average sentiment trends.
Heatmaps showing correlations between stock price and sentiment.


Usage
After setting up dependencies and API credentials, run the script in the order of the code blocks to:
Scrape Reddit posts.
Analyze sentiment.
Fetch stock data and visualize correlations.
The results will be saved as CSV files, and the graphs will be displayed using matplotlib and seaborn.


Conclusion
This project helps visualize the relationship between public sentiment on Reddit and stock performance, using Tesla (TSLA) as a case study. By scraping Reddit posts, performing sentiment analysis, and comparing it with stock market data, it provides insights into how online discussions might influence market movements.

