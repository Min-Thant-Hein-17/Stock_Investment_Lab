# 04 — Sentiment Analysis

## Project Description

This project explores the relationship between financial news sentiment and stock price movements. The central hypothesis is simple but powerful: when the news about a company is overwhelmingly positive, its stock tends to rise — and vice versa. This project tests that hypothesis rigorously using Natural Language Processing (NLP) techniques applied to real financial news headlines.

Two sentiment models are implemented and compared: VADER, a fast rule-based model that requires no training, and FinBERT, a BERT-based transformer model pretrained specifically on financial text from Hugging Face. The sentiment scores are then merged with historical price data from `yfinance` to measure the actual correlation between news sentiment and next-day stock returns.

This project also connects naturally to Project 03 — the sentiment score can be used as an additional feature in the ML prediction pipeline, combining price signals with news signals for a more complete view of market dynamics.

---

## What This Project Does

- Scrapes financial news headlines using NewsAPI or Google News RSS feeds
- Cleans and preprocesses headline text for NLP analysis
- Scores each headline with VADER (rule-based, fast, no API needed)
- Scores each headline with FinBERT (transformer-based, finance-specific, highly accurate)
- Aggregates daily sentiment scores per stock ticker
- Merges sentiment data with stock price data by date
- Analyzes and visualizes the correlation between sentiment and next-day price returns
- Builds a Streamlit dashboard showing live news headlines with sentiment scores

---

## Key Questions Answered

- Does negative news sentiment predict a price drop the next trading day?
- Which model — VADER or FinBERT — is more accurate for financial headlines?
- Is sentiment a stronger signal for some stocks than others?
- How far in advance does sentiment predict price movement?

---

## Key Concepts Covered

- **NLP pipeline**: tokenization, text cleaning, sentiment classification
- **VADER**: lexicon-based sentiment analysis, compound score interpretation
- **FinBERT**: how pre-trained transformer models are fine-tuned for domain-specific text
- **Correlation analysis**: Pearson correlation between sentiment scores and returns
- **Lag analysis**: testing whether today's sentiment predicts tomorrow's price
- **Signal vs. noise**: understanding why sentiment alone is insufficient for trading

---

## Tech Stack

| Tool | Purpose |
|---|---|
| `requests` / `feedparser` | Scrape news headlines |
| `newsapi-python` | NewsAPI client (optional, free tier) |
| `vaderSentiment` | Rule-based sentiment scoring |
| `transformers` | Load and run FinBERT model |
| `yfinance` | Stock price data |
| `pandas` / `numpy` | Data merging and analysis |
| `plotly` | Sentiment and correlation charts |
| `streamlit` | Sentiment dashboard app |

---

## Project Structure

```
04_sentiment_analysis/
├── notebooks/
│   ├── 01_vader_sentiment.ipynb       # VADER scoring and analysis
│   ├── 02_finbert_sentiment.ipynb     # FinBERT scoring and comparison
│   └── 03_sentiment_vs_price.ipynb    # Correlation with stock returns
├── app.py                              # Streamlit sentiment dashboard
├── utils.py                            # Scraping and scoring helpers
└── README.md
```

---

## How to Run Locally

```bash
cd 04_sentiment_analysis

# Install transformer dependencies
pip install transformers torch vaderSentiment feedparser

# Run the dashboard
streamlit run app.py
```

---

## Live Demo

> Deployed on Streamlit Community Cloud
> Link: *(add your deployment URL here after deploying)*

---

## Dashboard Features

- Enter a stock ticker to fetch today's related news headlines
- Each headline displayed with sentiment label (Positive / Negative / Neutral) and score
- Sentiment trend chart over the past 30 days
- Correlation summary: sentiment vs. next-day return for selected stock
- Side-by-side comparison of VADER vs. FinBERT scores on the same headlines

---

## Sample Findings

- FinBERT consistently outperforms VADER on financial headlines due to its domain-specific training
- Negative sentiment shows a stronger and more reliable correlation with price drops than positive sentiment does with price rises (asymmetric effect)
- Correlation is strongest for mid-cap stocks where retail investor sentiment plays a larger role

---

## Connection to Project 03

The daily sentiment score produced here can be added as an extra feature column in the ML prediction pipeline (`03_ml_prediction`). When combined with technical indicators, sentiment features typically improve model accuracy by 2–5 percentage points — a meaningful gain in financial prediction tasks.
