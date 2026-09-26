# Portfolio Risk & Quantitative Reporting Engine

This repository is a modular quantitative finance project designed to transform market data into analyst-ready portfolio risk reports. It combines portfolio-level diagnostics, asset-level performance attribution, and conditional risk modeling into a single research-oriented framework.

The objective is not only to calculate financial metrics, but to build a reproducible reporting engine that helps investment and risk analysts understand:

- how a diversified portfolio performed,
- which assets drove return and risk,
- whether tail risk can be modeled and validated through conditional volatility models.

The project is structured as a three-part analytical engine. Each module answers a different investment or risk management question.

---

## 1. Project 1 — Portfolio Risk Report

**Core Question:**  
How did the portfolio behave from a risk, return, drawdown and diversification perspective?

This module provides a portfolio-level risk report focused on aggregate performance and market risk diagnostics. It evaluates the portfolio using historical returns, cumulative performance, rolling volatility, drawdown analysis, correlation structure, historical VaR, CVaR and benchmark sensitivity.

### Key Outputs

- Portfolio cumulative return
- Daily return behavior
- Rolling volatility
- Historical VaR and CVaR
- Maximum drawdown
- Sharpe, Sortino and Calmar ratios
- Beta and Jensen’s Alpha vs benchmark
- Correlation matrix
- Weekly asset contribution

### Key Insight

This module shows whether the portfolio delivered attractive risk-adjusted performance and whether diversification reduced downside exposure. It is the first layer of the engine because it answers the broad portfolio management question: **“Was the portfolio efficient, resilient and properly diversified?”**

---

## 2. Project 2 — Asset-Level Performance & Risk Tear Sheet

**Core Question:**  
Which assets explain the portfolio’s return, risk concentration and benchmark sensitivity?

This module generates an asset-level tear sheet for each portfolio constituent and the consolidated portfolio. It compares individual assets using return, volatility, beta, Jensen’s Alpha, Sharpe, Sortino, historical VaR, distribution diagnostics and selected fundamental indicators.

### Key Outputs

- Individual asset performance
- Asset-level beta vs SPY
- Jensen’s Alpha by asset
- Volatility and downside risk
- Historical VaR at 95% and 99%
- Return distribution diagnostics
- Basic fundamental indicators: price, P/E, EPS, target price and implied upside
- Portfolio vs individual asset comparison

### Key Insight

This module identifies which assets contributed most to performance and which ones introduced higher downside or systematic risk. It is useful for analysts who need to move from portfolio-level results into security-level interpretation. It answers: **“Which holdings created value, which holdings added risk, and how did each asset behave relative to the benchmark?”**

---

## 3. Project 3 — Conditional VaR & ARMA-GARCH Backtesting Framework

**Core Question:**  
Can portfolio and asset-level tail risk be modeled more dynamically using conditional volatility?

This module extends the analysis beyond static historical VaR by applying ARMA-GARCH models to weekly return series. It compares different innovation distributions, including Normal, Student-t and GED, selects the best specification using AIC, and validates VaR forecasts through Kupiec and Christoffersen backtesting tests.

### Key Outputs

- ADF stationarity test
- Ljung-Box autocorrelation test
- ARCH-LM heteroskedasticity test
- ARMA-GARCH model estimation
- Normal, Student-t and GED distribution comparison
- Conditional VaR estimation
- Kupiec unconditional coverage test
- Christoffersen conditional coverage test
- Residual diagnostic checks
- Weekly risk model report by asset and portfolio

### Key Insight

This module evaluates whether a conditional volatility framework improves risk measurement compared with static historical VaR. It is the most technical layer of the engine because it answers: **“Is the estimated tail risk statistically reliable, and does the model capture volatility dynamics adequately?”**

---

## Repository Logic

The three projects are connected as one analytical pipeline:

| Module | Analytical Role | Main Question |
|---|---|---|
| Project 1 | Portfolio-level diagnostics | How did the portfolio perform and how much risk did it take? |
| Project 2 | Asset-level attribution | Which assets drove return, risk and benchmark exposure? |
| Project 3 | Conditional risk modeling | Can tail risk be modeled and validated dynamically? |

Together, the projects form a complete quantitative reporting workflow:

1. Measure portfolio performance and risk.
2. Decompose results by asset.
3. Model conditional volatility and validate VaR forecasts.

---

## Methodological Scope

The framework uses market data from Yahoo Finance and applies standard techniques used in portfolio analytics and market risk management:

- Return calculation
- Risk-adjusted performance metrics
- Historical VaR and CVaR
- Rolling volatility
- Drawdown analysis
- CAPM beta and Jensen’s Alpha
- Correlation analysis
- ADF, Ljung-Box and ARCH-LM tests
- ARMA-GARCH modeling
- Conditional VaR
- Kupiec and Christoffersen backtesting

This repository is intended for educational, analytical and portfolio demonstration purposes. Results should be interpreted as model-based diagnostics, not as investment advice.

---

## Target Users

This project is designed for:

- investment analysts,
- risk analysts,
- portfolio management students,
- finance professionals learning Python-based reporting,
- recruiters or technical reviewers evaluating applied quantitative finance work.

The code is structured to be reproducible and customizable. Users can modify tickers, portfolio weights, benchmarks, date ranges, risk-free rate assumptions and reporting parameters.

---

## Main Value Proposition

This repository demonstrates the ability to connect financial theory, quantitative risk modeling and automated reporting in Python. It is designed to show not only coding ability, but also investment reasoning, risk awareness and the capacity to communicate results through institutional-style reports.

The final goal is to move from raw market prices to a structured analytical output that a finance team could use as a starting point for portfolio review, risk monitoring or investment discussion.
