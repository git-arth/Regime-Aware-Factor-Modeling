# Regime-Aware Factor Modeling: PCA & HMM Strategy
### [cite_start]Quantitative Research & Portfolio Optimization for GTSF ($2.6M Endowment) [cite: 19, 63]

[cite_start]This repository contains the end-to-end research, implementation, and backtesting of a multi-factor equity strategy developed for the **GTSF Investments Committee**[cite: 17, 62]. [cite_start]The model utilizes dimensionality reduction and state-space modeling to extract orthogonal alpha signals and dynamically manage risk across 15 years of daily market data[cite: 20, 64].

## Impact & Results
* [cite_start]**Risk-Adjusted Performance**: Achieved a **1.2 Sharpe Ratio** in long-term backtesting[cite: 21, 65].
* [cite_start]**Risk Mitigation**: Realized a **35% reduction in portfolio volatility** relative to the benchmark[cite: 21, 65].
* [cite_start]**Information Density**: Captured **>80% of systematic variance** through compressed factor signals[cite: 20, 64].
* [cite_start]**Institutional Context**: Strategically applied toward the management of a **$2.6M student-run endowment fund**[cite: 19, 63].

---

## Technical Implementation

### 1. Factor Extraction (PCA)
[cite_start]To address the "curse of dimensionality" and eliminate multi-collinearity across 11 US Sector ETFs, I utilized **Principal Component Analysis (PCA)**[cite: 20, 64]. [cite_start]This transformation compresses 15 years of daily returns into orthogonal principal components, ensuring alpha factors represent unique sources of risk[cite: 20, 64].

### 2. Regime Detection (HMM)
[cite_start]The strategy implements a **Hidden Markov Model (HMM)** to identify latent market states (e.g., High-Volatility Bear vs. Low-Volatility Bull)[cite: 21, 65]. [cite_start]The model dynamically reallocates capital based on the detected probability of the current regime, maximizing defensive stability during market dislocations[cite: 21, 65].

### 3. High-Performance Infrastructure
Research and model training were conducted using **GT's PACE cluster**, leveraging **distributed computing** and **Linux/Bash** environments to process large-scale historical datasets and perform intensive mathematical optimizations.

---

## Tech Stack & Tools
* [cite_start]**Languages**: Python (NumPy, pandas, SciPy, scikit-learn)[cite: 54, 55].
* [cite_start]**Quant Modeling**: Principal Component Analysis (PCA), Hidden Markov Models (HMM)[cite: 20, 21, 64, 65].
* **Data Visualization**: Matplotlib for equity curve and regime probability analysis.
* **Infrastructure**: Linux/Bash, HPC Clusters (SLURM), Git.

---

## Repository Structure
* `final-project-arth.ipynb`: Full implementation of the data pipeline, factor extraction, and backtesting logic.
* `gtsf_quant_final_project_report.pdf`: Comprehensive technical report detailing mathematical foundations and performance metrics.
* [cite_start]`data/`: Directory for historical ETF return series (15 years of daily data)[cite: 20, 64].

---

## Future Direction: IndexFlux
[cite_start]This framework serves as the foundation for **Project IndexFlux**, an ongoing initiative to develop predictive trading models for **S&P 500 rebalancing events** using high-frequency market data and liquidity arbitrage signals[cite: 32, 76, 79].

---
