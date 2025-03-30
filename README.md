# Event-Based Forecasting of Stock Market Movements

### Project Overview

This project explores event-based forecasting, analyzing how breaking financial news influences stock market movements. Using a dataset containing news articles, headlines, and stock price data, the study investigates the impact of news sentiment on Cumulative Abnormal Returns (CAR) for a selected stock (SPY – S&P 500 ETF).

### Dataset

News Data (Financial Tweets & Headlines)
- date – Date of news publication
- source – News publication (e.g., Guardian, Bloomberg, etc.)
- Headlines – Title of the news article
- Description – Summary or excerpt of the article
- sentiment – Sentiment classification (bullish, bearish, neutral)

Stock Data (Historical Market Prices)
- Date – Trading date
- Open, High, Low, Close – Stock price data
- Adj Close – Adjusted closing price
- Volume – Number of shares traded

### Project Workflow

1. Load and Clean Data
- Reads news articles and stock prices.
- Converts dates to a standardized format.
- Drops missing values.

2. Match News with Trading Days
- Aligns news dates with stock trading days, adjusting for weekends/holidays.
- Uses Yahoo Finance API (yfinance) to retrieve historical stock data.

3. Compute Cumulative Abnormal Returns (CAR)
- Baseline Return: Average daily return of the stock.
- CAR Calculation: Measures stock performance before & after the news event.
- Sentiment Aggregation: Groups events by sentiment type.

4. Generate Insights
- Identifies top bullish & bearish events based on CAR.
- Displays key market-moving news dates.
- Saves results to a CSV file (car_results.csv).

### Future Improvements

1. Machine Learning – Train models to predict stock movement based on news sentiment.
2. Multi-Stock Analysis – Extend to other stocks/sectors.
3. Alternative Data Sources – Incorporate social media (Twitter, Reddit) sentiment.

### Source

![Financial News Headlines Data from Kaggle](https://www.kaggle.com/datasets/notlucasp/financial-news-headlines#%20Sentiment%20Analysis%20in%20Finance)
