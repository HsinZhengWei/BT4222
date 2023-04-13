# BT4222 Project Group 11 - Sentiment Analysis on Social Media to Predict Stock Prices 
<br />

The stock market can be unpredictable and volatile, with prices fluctuating rapidly in response to various factors like economic news and investor sentiment. Traditionally, investors have relied on technical analysis to make investment decisions, but these methods have their limitations and may not always provide accurate predictions. They do not take into account the impact that social media brings to investor sentiment. Hence this project hopes to integrate social media insights to better predict stock prices, performing sentiment analysis on pertinent data from social media and combining that with financial data to predict stock prices more accurately.  
  
The social media and financial data collected spans 4 years, from 2019 to 2022. Apple was chosen as the stock to focus on for our project but users are able to run the project and similarly predict prices for any other stocks. We then performed exploratory data analysis on the collected data, performed feature selection and ran 4 different Machine Learning Models on the selected important features to predict the Stock prices. Our data was collected from these sources:

1. Top 2000 tweets of each day from 1st January 2019 to 31st December 2022 containing the keyword of the stock ticker 'aapl'.
2. Top posts and top level comments from 2019 to 2022 from the r/Apple subreddit, which amounted to 576 posts and 2533 comments.
3. $AAPL's Opening, Closing, Low, High prices and Trading volume and S&P500's Closing price.
4. Return on Equity(ROE), Debt to Equity, and other financial data using the Alpha Vantage API.
5. US GDP data from Federal Reserve Economic Data (FRED) and US Consumer Price Index from the US Bureau of Labor Statistics (BLS) API.

## Setting Up

These instructions will get you a copy of the project up and running on your local machine. This is a runthrough on what each of the folders in this respository contains.

### Download the Files
1. The zipped version of our data files are available for download as some of the datasets such as extracted datasets are too big to publish on github. TO BE ADDED

### Installing the required packages
 Use requirements.txt to install the correct versions of the required Python libraries to run the Python code in your new Python environment.
 ```
 pip install -r requirements.txt
 ```
 2. Download the following lexicons which we used to perform NLP. Run the code chunks in your python notebook / script.
 ```
 nltk.download('stopwords')
 nltk.download('vader_lexicon')
 ```

## Running the Codes
### Data Extraction and Pre-Processing
1. Twitter Tweets
	- Run ../TwitterData/snscrape.ipynb  to scrape weekly tweets by changing the start_date and end_date parameters to specify the desired dates. This will output twitter_xxxx.csv in the same directory.
	- Run ../TwitterData/TwitterSentimentAnalysis.ipynb to obtain the weekly sentiment score. This will output twitterComments.csv in the same directory.
2. Reddit Posts
	- Run ../RedditData/get_reddit_data.ipynb to scrape the weekly reddit posts. This will output reddit comments.csv and reddit posts.csv
	- Run ../RedditData/reddit_sentiment_analysis.ipynb to obtain the weekly sentiment score. This will output reddit sentiment scores.csv
3. Finance Data
	- Run ../Data Extraction/data_extraction.ipynb to extract stock prices and financial data. This will combine the financial data and Reddit and Twitter sentiment data. This will output data.csv in the same directory
	- Run ../Data Extraction/feature_selection.ipynb to generate final training data. This will output training_data.csv (time-series input = 5, output =1) and training_data1.csv (time-series input = 8, output = 4). 

### Individual Model
Each model is separated to its individual notebook. The inputs are training_data.csv and training_data1.csv. Run the following notebook for:
1. AdaBoost 
	- Notebook: ../Models/adaboost.ipynb 
2. ElasticNets
	- Notebook: ../Models/ElasticNet.ipynb
3. XGBoost 
	- Notebook: ../Models/xgboost_train.ipynb
4. LSTM
	- Notebook: ../Models/lstm_train.ipynb
## Authors
- Brandon Angga - [brandonmanggo](https://github.com/brandonmanggo)
- Hsin Zheng Wei - [HsinZhengWei](https://github.com/HsinZhengWei)
- Joshua tan Zhi Yi - [joshualah](https://github.com/joshualah)
- Lee Jie Yi Estella - [eseutella](https://github.com/eseutella)
- Luah Jun Yang - [LuahJunYang](https://github.com/LuahJunYang)
