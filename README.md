# BT4222 Project Group 11 - Sentiment Analysis on Social Media to Predict Stock Prices 
<br />
The stock market can be unpredictable and volatile, with prices fluctuating rapidly in response to various factors like economic news and investor sentiment. Traditionally, investors have relied on technical analysis to make investment decisions, but these methods have their limitations and may not always provide accurate predictions. They do not take into account the impact that social media brings to investor sentiment. Hence this project hopes to integrate social media insights to better 

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

