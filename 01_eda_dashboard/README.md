# 01 — EDA + Dashboard

## Project Description

This project is the foundation of the Stock Investment Lab. Before building any predictive model, it is essential to understand the data deeply — its shape, patterns, relationships, and quirks. This project performs a full Exploratory Data Analysis (EDA) on five major stocks (Coca-Cola, PepsiCo, Amazon, NVIDIA, and Apple) alongside the S&P 500 index, then presents the findings through a live interactive dashboard built with Streamlit and Plotly.

The dashboard allows anyone — regardless of technical background — to explore stock performance, compare companies side by side, and examine key financial metrics through interactive charts and filters.

---

## What This Project Does

- Downloads historical OHLCV (Open, High, Low, Close, Volume) data using `yfinance`
- Cleans and preprocesses the data: handles missing values, checks for anomalies, and ensures correct data types
- Engineers features including daily returns, Simple Moving Averages (SMA-20, SMA-50), Exponential Moving Average (EMA-20), and rolling 30-day volatility
- Produces a correlation matrix to identify which stocks move together
- Analyzes trading volume patterns over time
- Visualizes all findings in a Streamlit dashboard with interactive Plotly charts

---

## Key Questions Answered

- Which stock delivered the highest return over the past 5 years?
- Which stock is the most volatile?
- How correlated are individual stocks with the S&P 500?
- Are there seasonal patterns in trading volume?
- What do moving averages reveal about trend momentum?

---

## Tech Stack

| Tool | Purpose |
|---|---|
| `yfinance` | Download stock price data |
| `pandas` | Data manipulation and cleaning |
| `numpy` | Numerical calculations |
| `matplotlib` / `seaborn` | Static analysis charts |
| `plotly` | Interactive charts in dashboard |
| `streamlit` | Web dashboard framework |

---

## Project Structure

```
01_eda_dashboard/
├── notebooks/
│   └── 01_eda_analysis.ipynb      # Full EDA with markdown explanations
├── app.py                          # Streamlit dashboard entry point
├── utils.py                        # Data fetching and helper functions
└── README.md
```

---

## How to Run Locally

```bash
cd 01_eda_dashboard
streamlit run app.py
```

---

## Live Demo

> Deployed on Streamlit Community Cloud
> Link: *(add your deployment URL here after deploying)*

---

## Sample Findings

- NVIDIA showed the highest return among selected stocks over the 2019–2024 period
- Coca-Cola and PepsiCo are highly correlated (r > 0.85) — they tend to move together
- All selected stocks show strong positive correlation with the S&P 500
- Trading volume spikes are frequently observed around earnings announcement dates
