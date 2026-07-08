# 03 — ML Prediction App

## Project Description

This project builds a full machine learning pipeline to predict next-day stock price direction — whether a stock's closing price will go up or down tomorrow. It goes beyond simple modeling by incorporating technical indicator features, explainability through SHAP values, and a deployed web application where users can input any stock ticker and receive a real-time prediction.

Two models are implemented: XGBoost, a powerful gradient boosting classifier that serves as the primary model, and an optional LSTM (Long Short-Term Memory) neural network that captures sequential patterns in price data. The focus is on building a production-quality pipeline: clean feature engineering, rigorous evaluation, and a user-friendly deployed app.

---

## What This Project Does

- Engineers a rich feature set from raw price data: lag features, RSI, MACD, Bollinger Bands, rolling statistics
- Frames the problem as binary classification: will price go up (1) or down (0) tomorrow?
- Trains and evaluates an XGBoost classifier with time-series-aware cross-validation
- Optionally trains an LSTM neural network for sequence-based prediction
- Uses SHAP (SHapley Additive exPlanations) to explain which features drive each prediction
- Deploys a Streamlit web app where users enter a ticker and get a live prediction with confidence score and explanation chart

---

## Key Concepts Covered

- **Feature engineering for financial data**: how to turn raw prices into meaningful signals
- **Technical indicators**: RSI (momentum), MACD (trend), Bollinger Bands (volatility)
- **XGBoost**: how gradient boosting works and why it performs well on tabular data
- **LSTM networks**: how recurrent neural networks handle sequential time-series input
- **SHAP values**: model interpretability — making black-box models explainable
- **Time-series cross-validation**: why standard k-fold cross-validation fails on time data

---

## Tech Stack

| Tool | Purpose |
|---|---|
| `yfinance` | Fetch live and historical stock data |
| `pandas` / `numpy` | Feature engineering and data prep |
| `scikit-learn` | Preprocessing, evaluation metrics |
| `xgboost` | Gradient boosting classifier |
| `tensorflow` / `keras` | LSTM neural network (optional) |
| `shap` | Model explainability and feature importance |
| `plotly` | Interactive prediction charts |
| `streamlit` | Web application framework |

---

## Project Structure

```
03_ml_prediction/
├── notebooks/
│   ├── 01_feature_engineering.ipynb   # Build and analyze features
│   ├── 02_xgboost_model.ipynb         # Train, evaluate, SHAP analysis
│   └── 03_lstm_model.ipynb            # LSTM model (optional advanced)
├── models/
│   └── xgboost_model.pkl              # Saved trained model
├── app.py                              # Streamlit prediction app
├── utils.py                            # Feature engineering functions
└── README.md
```

---

## How to Run Locally

```bash
cd 03_ml_prediction
streamlit run app.py
```

---

## Live Demo

> Deployed on Hugging Face Spaces
> Link: *(add your deployment URL here after deploying)*

---

## App Features

- Enter any valid stock ticker (e.g. KO, AAPL, TSLA)
- Select prediction horizon (next day)
- View prediction: UP or DOWN with confidence percentage
- View SHAP waterfall chart explaining which features influenced the prediction
- View recent price chart with technical indicators overlaid

---

## Model Performance

| Metric | XGBoost | LSTM |
|---|---|---|
| Accuracy | *(fill in after training)* | *(fill in after training)* |
| Precision | *(fill in after training)* | *(fill in after training)* |
| Recall | *(fill in after training)* | *(fill in after training)* |
| F1 Score | *(fill in after training)* | *(fill in after training)* |

---

## Disclaimer

This model is built for educational purposes only. A prediction accuracy above 55% on financial data is considered meaningful in research settings, but this should never be used to make real trading decisions.
