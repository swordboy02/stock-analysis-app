# Stock Return Analysis (Exploratory ML)

This project is an exploratory machine learning and data analysis study focused on applying basic ML techniques to financial time-series data. Using historical daily stock prices for Nike (NKE), the project investigates whether commonly used statistical and technical features capture any consistent structure in short-term stock price movement.
Rather than assuming predictability, the goal is to understand how standard ML models behave when applied to noisy, real-world financial data and to document the limitations of such approaches.

---

## Overview

This project explores the following questions:
- How do daily stock returns and volatility behave over time?
- What patterns, if any, emerge from simple technical features such as returns, moving averages, and rolling volatility?
- How do basic classification models perform when tasked with predicting next-day stock direction, and what are their limitations?

The analysis is conducted in a Jupyter notebook and is intentionally scoped to a single stock to keep the investigation focused and interpretable.

---

## Dataset

- Source: Yahoo Finance via `yfinance` API
- Ticker: `NKE`
- Timeframe: January 2020 – January 2024
- Frequency: Daily stock prices

---

## Tools & Technologies

- **Language:** Python
- **Environment:** Jupyter Notebook
- **Libraries:** 
  - `pandas`, `numpy` – data manipulation
  - `matplotlib`, `seaborn` – visualizations
  - `scipy.stats.mstats` – winsorization for outlier treatment
  - `yfinance` – stock data scraping

---

## Feature Engineering and Analysis

The project focuses on interpretable, commonly used features, including:
- Daily returns and open-to-close returns
- Rolling volatility (20-day window)
- Simple Moving Average (SMA, 20-day window)
- Time-based features such as month and day of week

These features are used to explore price behavior and serve as inputs to simple classification models.

---

## Modeling Approach

A binary classification setup is used to label whether the stock’s closing price increases on the following trading day(This may change ahead as I work on the project and understand what are necessary takeaways when understanding stocks). Multiple baseline and non-linear models are evaluated to assess whether any short-term structure can be learned from the engineered features.
Model performance is analyzed critically, with attention to failure modes, noise, and the inherent difficulty of short-term stock prediction.

---

## Scope and Limitations

This project:
- Is exploratory in nature and not a trading strategy
- Does not attempt to beat the market or generate financial advice
- Uses a single stock and daily price data only

The intent is to study model behavior and assumptions rather than optimize predictive performance.

---

## ▶️ How to Run

1. Clone the repo:
   ```bash
   git clone https://github.com/swordboy02/stock-prediction.git
   cd stock-prediction
