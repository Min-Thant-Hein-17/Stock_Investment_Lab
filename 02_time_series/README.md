# 02 — Time Series Forecasting

## Project Description

This project applies classical statistical time series models to forecast future stock prices. Unlike machine learning models that rely on many engineered features, time series models work directly with the price sequence itself — learning the underlying trend, seasonality, and autocorrelation structure of the data.

Two models are implemented and compared: ARIMA (AutoRegressive Integrated Moving Average), a foundational statistical method, and Prophet, an open-source forecasting library developed by Meta that handles trend and seasonality automatically. The project focuses not just on producing forecasts, but on understanding *why* each model behaves the way it does and critically evaluating its limitations.

---

## What This Project Does

- Tests for stationarity using the Augmented Dickey-Fuller (ADF) test
- Applies differencing and log transforms to make the price series stationary
- Uses ACF and PACF plots to identify optimal ARIMA parameters (p, d, q)
- Fits and evaluates an ARIMA model on a held-out test set
- Fits a Prophet model with automatic trend and seasonality decomposition
- Compares both models using MAE, RMSE, and MAPE evaluation metrics
- Produces forecast plots with confidence intervals

---

## Key Concepts Covered

- **Stationarity**: why raw stock prices are non-stationary and how to fix it
- **Autocorrelation**: how past prices influence future prices
- **Train/test split for time series**: why random shuffling is forbidden
- **Overfitting vs. underfitting** in forecasting contexts
- **Confidence intervals**: what they tell us about forecast uncertainty

---

## Tech Stack

| Tool | Purpose |
|---|---|
| `yfinance` | Download stock price data |
| `pandas` / `numpy` | Data handling and transforms |
| `statsmodels` | ARIMA model and statistical tests |
| `prophet` | Facebook Prophet forecasting model |
| `matplotlib` | Forecast and diagnostic plots |
| `scikit-learn` | Evaluation metrics (MAE, RMSE) |

---

## Project Structure

```
02_time_series/
├── notebooks/
│   ├── 01_arima_forecasting.ipynb     # ARIMA model walkthrough
│   └── 02_prophet_forecasting.ipynb   # Prophet model walkthrough
└── README.md
```

---

## How to Run

```bash
# Install dependencies
pip install statsmodels prophet scikit-learn

# Open notebooks
jupyter notebook notebooks/01_arima_forecasting.ipynb
```

---

## Important Note on Stock Forecasting

Time series models capture historical patterns — they cannot predict unexpected events (earnings surprises, geopolitical news, market crashes). The forecast errors on stock data are intentionally high; the value of this project lies in understanding the *methodology*, not in producing a profitable trading signal.

---

## Model Comparison Results

| Metric | ARIMA | Prophet |
|---|---|---|
| MAE | *(fill in after running)* | *(fill in after running)* |
| RMSE | *(fill in after running)* | *(fill in after running)* |
| MAPE | *(fill in after running)* | *(fill in after running)* |

> Results will vary depending on the stock ticker and time period selected.
