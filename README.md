# Stock Market Prediction

This project involves the application of machine learning algorithms and statistical models to analyze historical market data, identify patterns, and make predictions about future stock prices or market trends. The aim is to develop and identify the most effective model for accurately predicting stock prices.

## Project Overview

### 1. Introduction

- **Purpose:**  
  Stock market analysis involves applying machine learning techniques, such as regression, classification, clustering, and neural networks, to process vast amounts of data, recognize complex relationships, and improve prediction accuracy over time. This approach helps investors make more informed decisions by providing insights that are difficult to uncover through traditional analysis methods.

- **Scope:**  
  The project aims to develop and identify the most effective model for accurately predicting stock prices.

### 2. Data Collection

- **Data Sources:**  
  The financial information and historical market data were retrieved from Yahoo Finance.

- **Data Acquisition:**
  - Install the `yfinance` library:  
    ```bash
    pip install yfinance
    ```
  - Import necessary libraries:  
    ```python
    import yfinance as yf
    ```
  - Download data using `yf.download()` method:  
    ```python
    data = yf.download('AAPL GOOGL MSFT AMZN META', start='2020-01-01', end='2023-01-01')
    ```

- **Datasets:**  
  Datasets for five companies were imported: Apple, Google, Microsoft, Amazon, and Meta.

### 3. Data Preprocessing

- **Data Cleaning:**  
  No missing values or duplicate values are present in any of the datasets.

### 4. Exploratory Data Analysis (EDA)

- **Descriptive Statistics:**
  - META and Microsoft have the highest average adjusted closing prices, but META is the most volatile with the highest standard deviation and the widest price range.
  - Apple has the most stable prices with the lowest standard deviation, making it potentially less risky for investors who prioritize stability.
  - Google has the lowest average prices and also a relatively low standard deviation, indicating lower prices but not very high volatility.
  - Amazon and Google have lower average prices compared to META and Microsoft, but Amazon has slightly higher volatility than Google.

- **Visualization:**
  - **Close Value:**  
    The closing price is the last price at which the stock is traded during the regular trading day and is the standard benchmark used by investors to track its performance over time.
  - **Daily Return:**
    - All five companies show daily returns that are centered around 0, indicating that on most days, the returns are close to zero.
    - The distributions of daily returns for these stocks are approximately normal, with some skewness and kurtosis present.
    - META and Google seem to have more extreme daily returns compared to Apple, Microsoft, and Amazon, indicating higher volatility.
    - Microsoft’s daily returns appear the most stable, with a narrower range of daily return values and fewer outliers.

- **Correlations:**
  - The price-related attributes (Open, High, Low, Close, Adj Close) are highly correlated for all companies, as expected.
  - Volume generally shows a negative correlation with price attributes, indicating that higher trading volumes tend to coincide with lower prices.
  - Daily Return has low positive correlations with other attributes, suggesting that day-to-day price changes are not strongly dependent on the absolute price levels or trading volumes.

### 5. Feature Engineering

- **Feature Creation:**  
  A new feature 'daily return' was created using the `.pct_change()` method on the 'adj close' column to capture the daily percentage change in adjusted closing prices, providing valuable information for forecasting and analysis.

- **Feature Selection:**  
  The process involved analyzing various potential predictors, ultimately selecting 'daily return' and 'adj close' based on their significance and potential impact on model performance.

### 6. Model Development

- **Model Selection:**  
  Two models were selected for stock price prediction:
  1. **ARIMA Model:**
     - ARIMA stands for Auto-Regressive Integrated Moving Average.
     - The ARIMA model parameters used are p = 2, d = 1, and q = 2.
     - The Mean Square Error (MSE) of the ARIMA model predictions was approximately 101.79.
  2. **LSTM Model:**
     - Long short-term memory (LSTM) is a type of recurrent neural network (RNN) that can store information for long periods and use it for future calculations.
     - The model includes an LSTM layer with 128 units, another LSTM layer with 64 units, a dense layer with 25 units, and a final dense layer with 1 unit as the output layer.
     - The Mean Square Error (MSE) of the LSTM model predictions was approximately 36.43.

## 🚀 About Me
👋 Hi there! I'm Sinchana Chatterjee, an enthusiastic and determined B.Tech student with a fervent aspiration to excel as a Data Scientist and Data Analyst.


## Python Libraries

- pandas
- numpy
- sklearn
- matplotlib
- seaborn


## Authors

[@siniekoo19](https://github.com/siniekoo19)

## Acknowledgments

- Thanks to [kaggel](https://www.kaggle.com/) for providing the dataset used in this project.
- Special thanks to the open-source community for their invaluable contributions to the tools and libraries used in this project.

## Feedback

If you have any feedback, please reach out to me at csinchana19@gmail.com

