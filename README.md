# Stock_Investment_Lab
Stock_Investment_Lab is the collections of my sequential projects on the stock investment and analysis topic. 


###########################

Stock Investment Analysis using Claude: 
https://www.instagram.com/p/DZiOZ6_DHRp/?img_index=8


#########################

# Three main parts 

1. EDA analysis project
2. TIme-Series Analysis Project
3. ML stock prediction Project

##############################

# Stock_Investment_Lab

**Stock_Investment_Lab** is a collection of four sequential data science projects built around stock market analysis and investment decision-making. Each project builds on the previous one — starting from raw data exploration, moving through statistical forecasting, machine learning prediction, and finally NLP-powered sentiment analysis on financial news.

The goal of this lab is to apply real-world data science techniques to a domain that is both practically meaningful and analytically rich: the stock market.

---

## Projects

| Folder | Project | Key Techniques | Deployment |
|---|---|---|---|
| `01_eda_dashboard/` | EDA + Dashboard | Pandas, Plotly, Streamlit | Streamlit Cloud |
| `02_time_series/` | Time Series Forecasting | ARIMA, Prophet | Notebooks only |
| `03_ml_prediction/` | ML Prediction App | XGBoost, LSTM, SHAP | Hugging Face Spaces |
| `04_sentiment_analysis/` | Sentiment Analysis | FinBERT, VADER, NLP | Streamlit Cloud |

---

## Stocks Covered

| Ticker | Company |
|---|---|
| `KO` | Coca-Cola |
| `PEP` | PepsiCo |
| `AMZN` | Amazon |
| `NVDA` | NVIDIA |
| `AAPL` | Apple |
| `^GSPC` | S&P 500 Index |

---

## Tech Stack

- **Data**: yfinance, pandas, numpy
- **Visualization**: matplotlib, seaborn, plotly
- **Machine Learning**: scikit-learn, XGBoost, TensorFlow/Keras
- **NLP**: Hugging Face Transformers (FinBERT), VADER
- **Web Apps**: Streamlit
- **Version Control**: Git + GitHub

---

## Setup

```bash
# Clone the repository
git clone https://github.com/Min-Thant-Hein-17/Stock_Investment_Lab.git
cd Stock_Investment_Lab

# Create a virtual environment
python -m venv venv
source venv/bin/activate        # Mac/Linux
venv\Scripts\activate           # Windows

# Install dependencies
pip install -r requirements.txt
```

---

## Repository Structure

```
Stock_Investment_Lab/
├── 01_eda_dashboard/       # EDA notebooks + Streamlit dashboard
├── 02_time_series/         # ARIMA and Prophet forecasting notebooks
├── 03_ml_prediction/       # ML pipeline + prediction web app
├── 04_sentiment_analysis/  # News sentiment + correlation analysis
├── data/
│   ├── raw/                # Downloaded CSV files (gitignored)
│   └── processed/          # Cleaned and feature-engineered data
├── requirements.txt
├── .gitignore
└── README.md
```

---

## Disclaimer

This project is built for **educational and portfolio purposes only**. Nothing in this repository constitutes financial advice. Stock market predictions are inherently uncertain, and no model in this lab should be used to make real investment decisions.

---

*Built by [Min-Thant-Hein-17](https://github.com/Min-Thant-Hein-17)*
