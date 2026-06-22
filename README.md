# Multi-Agent Financial Forecasting

## Overview

This project develops a **multi-agent financial forecasting system** for predicting daily SPY returns using a no-regret adaptive ensemble framework. The model combines predictions from multiple specialized agents and dynamically updates their weights using the **Hedge Algorithm** with **Fixed-Share mixing**, enabling robust performance under changing market conditions.

The system was developed as part of **Stamatics, IIT Kanpur** and focuses on improving risk-adjusted returns while adapting to non-stationary financial markets.

---

## Objective

Implement a **no-regret adaptive ensemble (Hedge + Fixed-Share)** for forecasting SPY returns over the period **2010–2024**, leveraging diverse predictive models and online learning techniques.

---

## Methodology

### Data Sources

* SPY (SPDR S&P 500 ETF) historical market data
* VIX (Volatility Index) data
* Engineered technical indicators and market features

### Agent Architecture

The forecasting framework consists of four specialized agents:

#### 1. OLS Agent

* Captures long-term market trends
* Uses linear regression on engineered financial features

#### 2. XGBoost Agent

* Learns nonlinear relationships
* Models momentum and volatility effects

#### 3. LSTM Agent

* Captures sequential market dependencies
* Processes time-series information using recurrent neural networks

#### 4. Technical Signal Agent

* Utilizes technical indicators for directional forecasting
* Provides complementary market signals

---

## Adaptive Ensemble Framework

### Hedge Algorithm

* Aggregates forecasts from all agents
* Assigns higher weights to better-performing agents
* Updates weights online after every trading day

### Fixed-Share Mixing

* Prevents over-reliance on a single expert
* Handles regime shifts and non-stationary market behavior
* Enables rapid adaptation during market transitions

---

## Training Pipeline

1. Collect SPY and VIX historical data
2. Generate technical and volatility features
3. Train individual forecasting agents
4. Generate daily predictions
5. Update ensemble weights using Hedge + Fixed-Share
6. Evaluate portfolio performance and forecasting accuracy

---

## Results

### Forecasting Performance

* Sharpe Ratio: **0.38**
* Uniform Ensemble Sharpe Ratio: **0.24**
* Performance Improvement: **+58%**

### Directional Accuracy

* Technical agents achieved approximately **50% directional accuracy**

### Portfolio Performance

* Reduced drawdowns across multiple market regimes
* Improved risk-adjusted returns through dynamic agent allocation
* Demonstrated robustness during periods of elevated volatility

---

## Technologies Used

* Python
* NumPy
* Pandas
* Scikit-Learn
* XGBoost
* TensorFlow / Keras
* Matplotlib
* Yahoo Finance API

---

## Key Contributions

* Developed a multi-agent forecasting framework for SPY return prediction.
* Implemented an online learning ensemble using Hedge and Fixed-Share algorithms.
* Backtested strategies across multiple market regimes from 2010–2024.
* Improved portfolio Sharpe ratio by 58% compared to a uniform ensemble baseline.
* Dynamically adapted agent weights to changing market conditions.

---

## Future Work

* Incorporate transformer-based forecasting models.
* Extend the framework to multi-asset portfolios.
* Integrate macroeconomic and alternative data sources.
* Explore reinforcement learning for portfolio allocation.

