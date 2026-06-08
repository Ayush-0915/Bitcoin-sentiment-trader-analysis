# Bitcoin Sentiment Trader Analysis

## Executive Summary

This project investigates the relationship between Bitcoin market sentiment and trader performance using the Bitcoin Fear & Greed Index and historical trading data from Hyperliquid. The objective was to determine whether market sentiment influences profitability, win rates, trading activity, and position sizing behavior.

The analysis was conducted on 211,224 trades executed by 32 traders across 246 cryptocurrency assets. After merging sentiment data with trading activity, multiple statistical and exploratory analyses were performed.

Key findings indicate that Extreme Greed market conditions produced the highest average profitability and win rates, while Fear periods generated the highest cumulative profits and largest average trade sizes. Statistical testing confirmed that profitability differences across sentiment regimes are significant.

---

# 1. Introduction

Market sentiment is widely considered a major driver of cryptocurrency price movements. Traders often use sentiment indicators to assess risk and identify favorable market conditions.

This study explores whether Bitcoin market sentiment correlates with trading performance and whether sentiment can be used as a useful signal for strategy optimization and risk management.

---

# 2. Datasets

## Bitcoin Fear & Greed Index

The sentiment dataset contains:

- Date
- Sentiment Value
- Classification

Sentiment categories:

- Extreme Fear
- Fear
- Neutral
- Greed
- Extreme Greed

## Hyperliquid Historical Trader Data

The trading dataset contains:

- Account
- Coin
- Execution Price
- Trade Size
- Position Information
- Closed PnL
- Trade Timestamp

---

# 3. Data Preparation

The following preprocessing steps were performed:

1. Converted timestamp fields into datetime format.
2. Removed duplicate records.
3. Created a common trade date field.
4. Merged trading data with sentiment data.
5. Engineered additional features:
   - Win/Loss Indicator
   - Absolute PnL
   - Sentiment Labels

The final merged dataset contained 211,224 trades.

---

# 4. Exploratory Data Analysis

## Dataset Summary

| Metric             |   Value |
| ------------------ | ------: |
| Total Trades       | 211,224 |
| Total Traders      |      32 |
| Unique Coins       |     246 |
| Total Realized PnL | $10.30M |

---

## Win Rate Analysis

Win rates varied significantly across sentiment conditions.

| Sentiment     | Win Rate (%) |
| ------------- | -----------: |
| Extreme Fear  |        37.06 |
| Fear          |        42.08 |
| Neutral       |        39.70 |
| Greed         |        38.48 |
| Extreme Greed |        46.49 |

Extreme Greed periods exhibited the highest win rates while Extreme Fear periods showed the lowest.

---

## Average Profitability

| Sentiment     | Avg PnL |
| ------------- | ------: |
| Extreme Fear  |   34.54 |
| Fear          |   54.29 |
| Neutral       |   34.31 |
| Greed         |   42.74 |
| Extreme Greed |   67.89 |

Extreme Greed generated the highest average profit per trade.

---

## Total Profitability

| Sentiment     | Total PnL |
| ------------- | --------: |
| Extreme Fear  |   739,110 |
| Fear          | 3,357,155 |
| Neutral       | 1,292,921 |
| Greed         | 2,150,129 |
| Extreme Greed | 2,715,171 |

Fear periods generated the largest cumulative profits despite lower average profitability.

---

## Trade Size Analysis

| Sentiment     | Average Trade Size (USD) |
| ------------- | -----------------------: |
| Extreme Fear  |                 5,349.73 |
| Fear          |                 7,816.11 |
| Neutral       |                 4,782.73 |
| Greed         |                 5,736.88 |
| Extreme Greed |                 3,112.25 |

Traders deployed significantly larger capital during Fear periods.

---

# 5. Statistical Analysis

A Welch's T-Test was performed between Extreme Fear and Extreme Greed profit distributions.

Results:

- T Statistic = -3.85
- P Value = 0.000117

Since p < 0.05, the difference in profitability is statistically significant.

This confirms that market sentiment influences trader performance.

---

# 6. Correlation Analysis

A correlation analysis was conducted between trade size and profitability.

| Variables              | Correlation |
| ---------------------- | ----------: |
| Size USD vs Closed PnL |        0.12 |

The weak positive correlation indicates that larger trade sizes alone do not guarantee higher profitability.

---

# 7. Key Findings

### Finding 1

Extreme Greed conditions generated the highest average profitability and highest win rate.

### Finding 2

Fear periods generated the largest cumulative profits.

### Finding 3

Traders increased position sizes significantly during Fear conditions.

### Finding 4

Profitability differences across sentiment regimes are statistically significant.

### Finding 5

Trading profits are concentrated among a small number of highly profitable traders.

### Finding 6

Trade size has limited influence on profitability.

---

# 8. Recommendations

1. Incorporate sentiment indicators into risk management frameworks.
2. Monitor Extreme Greed conditions for favorable trading opportunities.
3. Evaluate contrarian strategies during Fear periods.
4. Track top-performing traders to identify successful behavioral patterns.
5. Avoid relying solely on larger position sizes to improve returns.

---

# 9. Conclusion

This analysis demonstrates a clear relationship between Bitcoin market sentiment and trader performance. Market sentiment significantly impacts profitability, trading behavior, and risk-taking patterns. The findings suggest that sentiment-based signals can be valuable tools for improving trading decisions and portfolio risk management.
