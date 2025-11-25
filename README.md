# News Sentiment Stock Prediction

Predicting stock price movement using financial news sentiment analysis.
This project combines EDA, natural language processing (NLP) sentiment analysis, stock technical indicators, and correlation analysis to explore how news affects stock prices.

---

## Table of Contents

1. [Project Overview](#project-overview)
2. [Business Objective](#business-objective)
3. [Data](#data)
4. [Project Structure](#project-structure)
5. [Tasks](#tasks)
6. [Technical Indicators](#technical-indicators)
7. [Sentiment Analysis](#sentiment-analysis)
8. [Correlation Analysis](#correlation-analysis)
9. [Visualization](#visualization)
10. [Setup Instructions](#setup-instructions)
11. [References](#references)

---

## Project Overview

This project analyzes financial news headlines and stock price data to determine the relationship between news sentiment and stock price movement.
It simulates real-world financial analytics tasks, including EDA, time-series analysis, technical indicator computation, and sentiment-based correlation studies.

---

## Business Objective

Nova Financial Solutions aims to enhance predictive analytics capabilities to improve financial forecasting accuracy and operational efficiency.
As a data analyst, your goal is to:

* Perform sentiment analysis on financial news headlines.
* Quantify correlations between sentiment and stock price movements.
* Suggest actionable insights for predictive trading strategies.

---

## Data

**Datasets used:**

1. **Financial News Dataset (FNSPID)**

   * `headline`: News article title
   * `url`: Link to article
   * `publisher`: Source of the article
   * `date`: Publication date and time (UTC-4)
   * `stock`: Ticker symbol (e.g., AAPL)

2. **Stock Price Data**

   * Open, High, Low, Close, Adjusted Close, Volume
   * Daily time series downloaded from Yahoo Finance (`yfinance`)

---

## Project Structure

```
├── .github/
│   └── workflows/
├── notebooks/
│   └── EDA_and_Analysis.ipynb
├── scripts/
│   └── __init__.py
├── src/
│   └── __init__.py
├── tests/
│   └── __init__.py
├── data/
│   ├── raw_analyst_ratings.csv
│   └── yfinance_data/
├── .gitignore
├── requirements.txt
└── README.md
```

---

## Tasks

### Task 1: Git and GitHub Setup

* Repository setup and environment configuration.
* Basic EDA: headline length, publisher activity, article frequency over time, keyword extraction.

### Task 2: Stock Price Technical Indicators

* Load stock price data.
* Compute technical indicators using TA-Lib:

  * Moving Averages (MA 20, MA 50)
  * Relative Strength Index (RSI 14)
  * MACD (12,26,9)
* Visualize price and indicator trends.

### Task 3: Correlation Between News and Stock Movement

* Align news and stock datasets by date.
* Compute sentiment for each headline using TextBlob.
* Aggregate daily sentiment and compute daily stock returns.
* Calculate Pearson correlation between average daily sentiment and stock returns.
* Visualize sentiment vs. returns.

---

## Technical Indicators

* **Moving Averages (MA):** Identify trend directions.
* **Relative Strength Index (RSI):** Measure momentum and overbought/oversold conditions.
* **MACD:** Track trend strength and momentum.

---

## Sentiment Analysis

* NLP sentiment scoring using **TextBlob**.
* Polarity ranges from -1 (negative) to +1 (positive).
* Average sentiment calculated for days with multiple news articles.

---

## Correlation Analysis

* Daily returns calculated as percentage change in closing prices.
* Pearson correlation coefficient used to quantify sentiment-stock price relationship.
* Scatter plots visualize the relationship between daily sentiment and stock returns.

---

## Visualization

* Time series plots: stock price with moving averages.
* RSI and MACD plots for trend analysis.
* Scatter plots for sentiment vs. daily returns.
* Heatmaps and bar plots for publisher and keyword distributions.

---

## Setup Instructions

1. Clone repository:

   ```bash
   git clone https://github.com/MAYSHLMAY/news-sentiment-stock-prediction.git
   ```
2. Install dependencies:

   ```bash
   pip install -r requirements.txt
   ```
3. Run notebooks or scripts from the `notebooks/` or `src/` directories.

---

## References

* [yfinance Documentation](https://pypi.org/project/yfinance/)
* [TA-Lib Python](https://github.com/ta-lib/ta-lib-python)
* [TextBlob](https://textblob.readthedocs.io/en/dev/)
* [Financial News and Stock Analysis Concepts](https://www.investopedia.com/)
