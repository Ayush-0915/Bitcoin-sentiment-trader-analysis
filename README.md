# Bitcoin Sentiment Trader Analysis

## Overview

This project analyzes the relationship between Bitcoin market sentiment and trader performance using historical trading activity from Hyperliquid and the Bitcoin Fear & Greed Index.

The objective is to determine how different market sentiment conditions influence trading profitability, win rates, position sizing behavior, and overall market performance.

---

## Dataset Description

### 1. Bitcoin Fear & Greed Index

Features:

* Date
* Classification (Extreme Fear, Fear, Neutral, Greed, Extreme Greed)
* Sentiment Value

### 2. Hyperliquid Historical Trading Data

Features:

* Account
* Coin
* Execution Price
* Size Tokens
* Size USD
* Side
* Timestamp
* Closed PnL
* Trade ID
* Transaction Hash
* Position Information

---

## Project Objectives

* Merge trader activity with market sentiment data.
* Analyze trader performance under different sentiment conditions.
* Measure profitability, win rates, and trade sizing behavior.
* Identify statistically significant relationships.
* Generate actionable trading insights.

---

## Data Preprocessing

The following preprocessing steps were performed:

1. Data cleaning and validation.
2. Date conversion and timestamp standardization.
3. Duplicate removal.
4. Feature engineering:

   * Win/Loss indicator
   * Absolute PnL
   * Trade date extraction
5. Dataset merging using trade dates.

---

## Exploratory Data Analysis

### Key Metrics Analyzed

* Win Rate by Sentiment
* Average Profit per Trade
* Total Profit by Sentiment
* Trade Count by Sentiment
* Average Trade Size
* Top Performing Traders
* Most Profitable Coins
* Correlation Analysis

---

## Statistical Testing

A Welch's T-Test was performed to compare profitability between Extreme Fear and Extreme Greed market conditions.

### Results

* T Statistic: -3.85
* P Value: 0.000117

Result:

The profitability difference between Extreme Fear and Extreme Greed periods is statistically significant (p < 0.05).

---

## Key Findings

### 1. Extreme Greed Produced the Highest Average Profitability

* Average PnL: $67.89
* Win Rate: 46.49%

### 2. Fear Generated the Highest Total Profit

* Total PnL: $3.36M

### 3. Traders Took Larger Positions During Fear

* Average Trade Size: $7,816

This suggests traders may adopt contrarian strategies during fearful market conditions.

### 4. Market Sentiment Significantly Influences Performance

Statistical testing confirmed a significant profitability difference between sentiment regimes.

### 5. Profitability Is Concentrated Among a Small Number of Traders

A few traders contributed a substantial portion of total profits.

### 6. Weak Correlation Between Trade Size and Profitability

Correlation between trade size and realized profit:

* Correlation Coefficient: 0.12

This indicates that larger positions alone do not guarantee higher profitability.

---

## Visualizations

The project includes:

* Win Rate by Sentiment
* Average PnL by Sentiment
* Total PnL by Sentiment
* Profit Distribution Boxplot
* Trade Count by Sentiment
* Average Trade Size by Sentiment
* Top 10 Traders by Profit
* Correlation Heatmap

---

## Project Structure

```text
bitcoin-sentiment-trader-analysis/
│
├── data/
│   ├── historical_data.csv
│   ├── fear_greed_index.csv
│   └── merged_trader_sentiment_data.csv
│
├── images/
│   ├── win_rate_by_sentiment.png
│   ├── average_pnl_by_sentiment.png
│   ├── total_pnl_by_sentiment.png
│   ├── trade_count_by_sentiment.png
│   ├── trade_size_by_sentiment.png
│   ├── top_10_traders.png
│   ├── profit_distribution_boxplot.png
│   └── correlation_heatmap.png
│
├── notebooks/
│   └── analysis.ipynb
│
├── reports/
│
├── README.md
├── requirements.txt
└── .gitignore
```

---

## Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* SciPy
* Jupyter Notebook

---

## Conclusion

The analysis demonstrates that market sentiment has a measurable impact on trading performance. Extreme Greed conditions generate the highest average profitability, while Fear conditions generate the highest cumulative profits and larger trade sizes. These findings suggest that sentiment indicators can be valuable inputs for risk management and trading strategy optimization.
