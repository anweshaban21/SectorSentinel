# SectorSentinel
# 📊 Sectoral Stock Analysis Across Bullish and Bearish Market Phases

This project analyzes the behavior of different Indian stock market sectors during **bullish** and **bearish** phases using time series forecasting and risk assessment models. It identifies which model combinations perform best in different market regimes and across various sectors.

---

## 📌 Objective

To compare the performance of multiple models (GARCH, LSTM, Beta) in predicting returns and assessing risk across sectors under different market conditions (bullish and bearish periods), and to determine the most suitable model combination per sector and regime.

---

## 🗂️ Datasets Used

- **Source:** [Yahoo Finance](https://finance.yahoo.com/)
- **Data Type:** Daily adjusted closing prices
- **Market Index:** NIFTY 50 (`^NSEI`) — used to identify bull/bear phases
- **Sectors & Representative Stocks:**

| Sector     | Stocks Used |
|------------|-------------|
| IT         | INFY.NS, TCS.NS, WIPRO.NS |
| Banking    | HDFCBANK.NS, ICICIBANK.NS, SBIN.NS |
| Pharma     | SUNPHARMA.NS, DRREDDY.NS, CIPLA.NS |
| FMCG       | HINDUNILVR.NS, ITC.NS, DABUR.NS |

---

## 📈 Market Regimes

**Bullish Periods:**
- `2016-03-01` to `2018-01-29`
- `2020-04-01` to `2021-10-01`
- `2022-07-01` to `2023-12-15`

**Bearish Periods:**
- `2015-01-01` to `2016-02-29`
- `2018-02-01` to `2020-03-31`
- `2022-01-01` to `2022-06-30`

---

## 🔧 Methodology

1. **Data Collection** using `yfinance`
2. **Market Regime Detection** (manual selection based on NIFTY trends)
3. **Model Implementation**:
   - GARCH
   - LSTM
   - Beta (CAPM-style risk model)
   - Hybrid combinations:
     - GARCH + Beta
     - LSTM + Beta
     - GARCH + LSTM
     - GARCH + LSTM + Beta
4. **Performance Metrics**:
   - Sharpe Ratio
   - Custom Risk Score
5. **Sector-wise Comparison** across regimes

---

## ✅ Key Results

- **LSTM + Beta**: Best performing model in **bullish** periods for **IT** and **Banking** sectors.
- **GARCH + Beta**: Most effective in **bearish** periods for **Pharma** and **FMCG** sectors.
- Model behavior varies significantly by both **sector** and **market regime**.

---

## 🛠️ Requirements

- Python 3.x
- `yfinance`
- `pandas`
- `numpy`
- `arch` (for GARCH)
- `keras` / `tensorflow` (for LSTM)
- `matplotlib` / `seaborn` (for plots)

Install dependencies:

```bash
pip install yfinance pandas numpy arch matplotlib seaborn tensorflow
