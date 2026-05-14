# Applied Forecasting of Financial Data

A comparative forecasting study evaluating **statistical**, **machine learning**, and **deep learning** approaches for predicting stock prices within the energy sector.

This project explores how different forecasting methodologies perform across diverse stock behaviors, ranging from traditional oil majors to renewable energy companies.

---

## Project Overview

Forecasting financial time series is a fundamental challenge in quantitative finance due to volatility, nonlinear behavior, and external macroeconomic influences.

In this project, we compare three forecasting paradigms:

- **Statistical Time Series Models**
  - ARIMA
  - SARIMA

- **Machine Learning**
  - XGBoost with engineered time-series features

- **Deep Learning**
  - LSTM (Long Short-Term Memory Networks)

The objective was to evaluate which modeling approach performs best under different market conditions and stock characteristics.

---

## Stocks Analyzed

To capture a broad representation of the energy sector, five companies were selected:

| Ticker | Company | Category |
|--------|---------|----------|
| XOM | Exxon Mobil | Traditional Energy |
| CVX | Chevron | Traditional Energy |
| COP | ConocoPhillips | Upstream Exploration |
| BKR | Baker Hughes | Infrastructure / Services |
| RUN | Sunrun | Renewable Energy |

These selections provide exposure to:

- Traditional oil and gas producers
- Crude oil-sensitive upstream businesses
- Energy infrastructure and industrial services
- Renewable energy market behavior

---

## Methodology

### 1. Statistical Forecasting
#### ARIMA / SARIMA

Classical time series forecasting models designed to capture temporal autocorrelation.

**Approach:**
- Historical closing price modeling
- Stationarity transformation
- Trend/seasonality decomposition
- Parameter tuning

**Strengths:**
- Interpretable
- Strong statistical baseline
- Effective for structured trends

**Limitations:**
- Weak handling of nonlinear relationships
- Sensitive to volatility spikes

---

### 2. Machine Learning
#### XGBoost

Gradient boosting regression using engineered financial features.

**Feature Engineering Included:**
- Lagged closing prices
- High / low prices
- Open-close spread
- Daily returns
- Trading volume
- Moving averages

**Strengths:**
- Captures nonlinear relationships
- Strong predictive performance
- Built-in regularization reduces overfitting

**Limitations:**
- Feature engineering dependent
- Limited sequential memory

---

### 3. Deep Learning
#### LSTM

Recurrent neural network architecture built for sequential forecasting.

**Implementation:**
- Min-Max normalization
- Sliding 60-day input windows
- Dropout regularization
- Sequence-to-one forecasting

**Strengths:**
- Learns temporal dependencies
- Strong long-term pattern modeling
- Less manual feature engineering

**Limitations:**
- Computationally expensive
- Harder to interpret
- Sensitive to training setup

---

## Evaluation Metrics

Model performance was assessed using:

- **MSE** — Mean Squared Error
- **MAE** — Mean Absolute Error
- **RMSE** — Root Mean Squared Error
- **MAPE** — Mean Absolute Percentage Error

---

## Results Summary

### Best Performing Models by Stock

| Ticker | Best Model | Approx. MAPE |
|--------|------------|--------------|
| RUN | XGBoost | 4.31% |
| XOM | XGBoost / LSTM | ~3.0% |
| CVX | XGBoost | 0.88% |
| COP | XGBoost | 1.35% |
| BKR | LSTM | 4.02% |

### Key Findings

- **XGBoost delivered the strongest overall performance**
  - Most consistent forecasting accuracy
  - Excellent handling of nonlinear financial relationships

- **LSTM performed strongly on long-term trend forecasting**
  - Particularly effective for XOM and BKR

- **ARIMA / SARIMA provided useful baselines**
  - Interpretable models
  - Struggled during volatile market behavior

- **No single model dominated every stock**
  - Performance depended heavily on stock behavior and market structure

---

## Visual Results

Examples included in the project:

- Forecast vs actual comparison plots
- Model performance heatmaps
- Error distribution comparisons
- Time-series forecasting visualizations

---

## Tech Stack

**Languages**
- Python

**Libraries**
- pandas
- numpy
- matplotlib
- seaborn
- plotly
- scikit-learn
- statsmodels
- xgboost
- tensorflow 
- yfinance


---

## Authors

- Yahia Taraf
- Emirosman Murtazayev
- Liam Duke
- Sally Zhen
- Dorje Gurung
- Anis Tarafdar

---

## Academic Context

Final project for **MTH 5000 — Applied Forecasting**
