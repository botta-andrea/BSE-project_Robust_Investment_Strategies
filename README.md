# Constructing Robust Investment Strategies: Regularization Techniques and CVaR Optimization
BSE Summer School - Advanced Portfolio Management: Technical Project

# Constructing Robust Investment Strategies: Regularization Techniques and CVaR Optimization

This repository contains the code and analysis for a quantitative portfolio management project focused on constructing optimal long-term investment strategies for a private wealth client. 

## Overview
The project explores different asset allocation frameworks utilizing a universe of highly liquid ETFs representing major asset classes (Equities, Bonds, Commodities, Precious Metals, Real Estate, and Money Market). The goal is to balance expected returns with strict downside risk management.

## Methodologies Applied
* **Mean-Variance Optimization:** Classic Markowitz efficient frontier construction, both unconstrained and constrained (e.g., minimum 20% allocation in fixed income/money market, no short-selling).
* **VaR-Constrained Optimization:** Downside risk management utilizing Conditional Value-at-Risk (CVaR) minimization, imposing a strict 1-month 3% VaR limit at a 99% confidence level. Risk is estimated using both parametric (multivariate normal) and non-parametric (empirical bootstrap) scenarios.
* **Estimation Risk & Ridge Regularization:** Application of Cross Validation and L2 penalty (Ridge regression) to expected returns and covariance matrices to mitigate estimation risk, prevent over-concentration (e.g., in Gold), and generate more stable, robust weights.

## Repository Structure
* `AndreaBotta_Evaluation.ipynb`: The main Jupyter Notebook containing all the data downloading, exploratory data analysis, optimization algorithms, and output visualizations.
* `Project_Report.pdf`: A clean, code-free technical report summarizing the findings, correlation matrices, and efficient frontiers.

## Data Source
Historical financial data (monthly returns over an 18-year period) is downloaded dynamically via the `yfinance` API.

## Requirements
To run the notebook locally, you need the following Python libraries:
* `numpy`
* `pandas`
* `matplotlib`
* `seaborn`
* `scipy`
* `cvxpy`
* `yfinance`

## Usage
Clone the repository and run the Jupyter Notebook to replicate the optimization algorithms and generate the efficient frontier plots.
