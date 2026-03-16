# Portfolio-Optimization-Mini-Project
# Portfolio Optimization using Modern Portfolio Theory

## Overview

This project implements **portfolio optimization using Modern Portfolio Theory (MPT)** to determine the optimal allocation of assets that maximizes expected return for a given level of risk.

The project constructs portfolios using historical market data and evaluates them using standard financial metrics such as **expected return, volatility, and Sharpe ratio**. Both **long-only** and **long–short** portfolio strategies are implemented within the Mean–Variance Optimization (MVO) framework.

---

## Assets Used

The portfolio includes assets across multiple markets to demonstrate diversification.

| Asset Class      | Asset                                        |
| ---------------- | -------------------------------------------- |
| Equities         | NVDA, JNJ, PG                                |
| Commodities      | Gold (GC=F), Crude Oil (CL=F), Copper (HG=F) |
| Cryptocurrencies | BTC, ETH, SOL                                |

The **risk-free rate** is approximated using the **US 3-Month Treasury Bill (^IRX)**.

---

## Data Source

Historical price data is obtained from **Yahoo Finance** using the `yfinance` Python library.

Example data range used:

2021-01-01 → 2023-12-31

---

## Methodology

### 1. Data Collection

Historical daily closing prices are downloaded for each asset using `yfinance`.

### 2. Return Calculation

Daily asset returns are calculated and used to compute expected returns.

Annualized expected return:

Mean Daily Return × 252

### 3. Covariance Matrix

The covariance matrix measures how asset returns move relative to each other.

Annualized covariance:

Covariance × 252

### 4. Mean–Variance Optimization (MVO)

Using Modern Portfolio Theory, portfolios are optimized to maximize the **Sharpe Ratio**.

The project implements:

* **Long-Only Portfolios**

  * All weights ≥ 0
  * Fully invested portfolio

* **Long–Short Portfolios**

  * Allows negative weights
  * Enables taking short positions in assets

### 5. Portfolio Metrics

For each portfolio the following metrics are computed:

* Expected Portfolio Return
* Portfolio Volatility
* Sharpe Ratio

---

## Technologies Used

* Python
* NumPy
* Pandas
* SciPy
* yfinance
* Matplotlib
* Seaborn
* Jupyter Notebook

---

## Project Structure

portfolio-optimization/

├── portfolio_optimization_project.ipynb
└── README.md

---

## Key Concepts Demonstrated

* Modern Portfolio Theory
* Mean–Variance Optimization
* Long-Only Portfolio Construction
* Long–Short Portfolio Strategies
* Portfolio Risk and Return Analysis
* Sharpe Ratio Optimization
* Financial Data Analysis in Python

---

## Future Improvements

* **Portfolio Rebalancing Framework**
  Implement periodic portfolio rebalancing (e.g., monthly or quarterly) to maintain target allocations and evaluate performance over time for both **long-only** and **long–short strategies**.

* **Black–Litterman Model Implementation**
  Extend the project by implementing a **Black–Litterman portfolio optimization model** that incorporates investor views while maintaining the optimization framework used in the current MVO implementation.

---

## How to Run

1. Clone the repository

git clone https://github.com/yourusername/portfolio-optimization.git

2. Install dependencies

pip install pandas numpy yfinance matplotlib seaborn scipy

3. Run the notebook

jupyter notebook portfolio_optimization_project.ipynb

---
Please give your opinions and criticisms if any. I will work on this project soon again and i will update this readme also. I am having fun learning about finance and using python to learn it. It is very cool. I want to learn and make more cool things like this. Bye bye!

Sanka Skandhanuj

GitHub: https://github.com/OmegaRuby111


