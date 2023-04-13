# BT4222 Project Group 11 - Sentiment Analysis on Social Media to Predict Stock Prices 
<br />
The stock market can be unpredictable and volatile, with prices fluctuating rapidly in response to various factors like economic news and investor sentiment. Traditionally, investors have relied on technical analysis to make investment decisions, but these methods have their limitations and may not always provide accurate predictions. They do not take into account the impact that social media brings to investor sentiment. Hence this project hopes to integrate social media insights to better predict stock prices, performing sentiment analysis on pertinent data from social media and combining that with financial data to predict stock prices more accurately.  
  
The social media and financial data collected spans 4 years, from 2019 to 2022. Apple was chosen as the stock to focus on for our project but users are able to run the project and similarly predict prices for any other stocks. We then performed exploratory data analysis on the collected data, performed feature selection and ran 4 different Machine Learning Models on the selected important features to predict the Stock prices. Our data was collected from these sources:

1. Top 2000 tweets of each day from 1st January 2019 to 31st December 2022 containing the keyword of the stock ticker 'aapl'.
2. Top posts and top level comments from 2019 to 2022 from the r/Apple subreddit, which amounted to 576 posts and 2533 comments.
3. $AAPL's Opening, Closing, Low, High prices and Trading volume and S&P500's Closing price.
4. Return on Equity(ROE), Debt to Equity, and other financial data using the Alpha Vantage API.
5. US GDP data from Federal Reserve Economic Data (FRED) and US Consumer Price Index from the US Bureau of Labor Statistics (BLS) API.
