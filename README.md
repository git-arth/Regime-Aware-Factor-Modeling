# Regime-Aware Factor Modeling: PCA & HMM Strategy

This repository contains the end-to-end research, implementation, and backtesting of a multi-factor equity strategy developed for the GTSF Investments Committee Quant Mentorship. The model utilizes dimensionality reduction and state-space modeling to extract orthogonal alpha signals and dynamically manage risk across 15 years of daily market data.

## Impact & Results
**Risk-Adjusted Performance**: Achieved a **1.2 Sharpe Ratio** in long-term backtesting.
**Risk Mitigation**: Realized a **35% reduction in portfolio volatility** relative to the benchmark.
**Information Density**: Captured **>80% of systematic variance** through compressed factor signals.
**Institutional Context**: Strategically explores predictive trading model development to later be applied to **$2.6M student-run endowment fund**.

---

## Technical Implementation

### 1. Factor Extraction (PCA)
To address the "curse of dimensionality" and eliminate multi-collinearity across 11 US Sector ETFs, I utilized **Principal Component Analysis (PCA)**. This transformation compresses 15 years of daily returns into orthogonal principal components, ensuring alpha factors represent unique sources of risk.

### 2. Regime Detection (HMM)
The strategy implements a **Hidden Markov Model (HMM)** to identify latent market states (e.g., High-Volatility Bear vs. Low-Volatility Bull). The model dynamically reallocates capital based on the detected probability of the current regime, maximizing defensive stability during market dislocations.

---

## Tech Stack & Tools
**Languages**: Python (NumPy, pandas, SciPy, scikit-learn)
**Quantitative/Financial Modeling**: Principal Component Analysis (PCA), Hidden Markov Models (HMM)
**Data Visualization**: Matplotlib for equity curve and regime probability analysis.

---

## Repository Structure
* `final-project-arth.ipynb`: Full implementation of the data pipeline, factor extraction, and backtesting logic.
* `gtsf_quant_final_project_report.pdf`: Comprehensive technical report detailing mathematical foundations and performance metrics.
* `data/`: Directory for historical ETF return series (15 years of daily data).

---

## Future Direction: IndexFlux
This framework serves as the foundation for **Project IndexFlux**, an ongoing initiative to develop predictive trading models for **S&P 500 rebalancing events** using high-frequency market data and liquidity arbitrage signals.

---
