# Fama–French Three-Factor Model  
### Empirical Asset Pricing with U.S. Stocks

## Overview

This project empirically evaluates the Fama–French Three-Factor Model using a diversified set of U.S. large-cap equities. The analysis compares the explanatory power of the traditional Capital Asset Pricing Model (CAPM) with the Fama–French three-factor framework using monthly return data.

The objective is to assess whether size (SMB) and value (HML) factors provide additional explanatory power beyond market risk and to examine whether abnormal returns (alpha) persist after controlling for systematic risk factors.

---

## Research Objectives

- Estimate CAPM and Fama–French three-factor models for individual stocks  
- Examine the statistical significance of estimated alphas  
- Compare model explanatory power across specifications  
- Analyze market, size, and value exposures across firms  

---

## Data

The analysis uses monthly data from 2010 to 2026:

- **Stock returns:** Adjusted closing prices downloaded via `yfinance`
- **Risk-free rate and factors:** Fama–French Research Factors (Mkt−RF, SMB, HML, RF) from the Kenneth French Data Library

All returns are expressed in monthly frequency and factor data are converted from percentages to decimal form.

---

## Methodology

Two models are estimated using Ordinary Least Squares (OLS):

### 1. CAPM

R_i - R_f = α + β_MKT (MKT - RF) + ε

### 2. Fama–French Three-Factor Model

R_i - R_f = α + β_MKT MKT + β_SMB SMB + β_HML HML + ε

Model performance is evaluated using:

- Adjusted R²  
- Estimated alphas and their p-values  
- Factor loadings (β coefficients)  

---

## Key Findings

- The Fama–French model consistently achieves higher adjusted R² values than the CAPM, indicating improved explanatory power.
- Market betas vary meaningfully across firms, reflecting differences in systematic risk.
- SMB loadings show that most firms exhibit large-cap characteristics, while certain high-growth firms (e.g., Tesla) display small-cap–like return dynamics.
- HML loadings distinguish growth-oriented firms from value-oriented companies.
- Estimated alphas are generally not statistically significant, suggesting that abnormal returns largely disappear after accounting for systematic risk factors.

Overall, the findings are consistent with the central insights of modern empirical asset pricing.

---

## Project Structure
```
fama-french-factor-models/
│
├── data/
│   ├── raw/  
│   └── processed/  
│
├── notebooks/
│   └── fama_french_3factor_stocks_monthly.ipynb
│
├── README.md
├── requirements.txt
└── .gitignore
```
---

## Tools Used

- Python  
- pandas  
- numpy  
- statsmodels  
- matplotlib  
- yfinance  
- pandas-datareader  

---

## Author

Saman Zare