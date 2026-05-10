<div align="center">

# 📊 NASDAQ Stock Market Analysis & EDA

### Exploring Securities, ETFs, Financial Status & Exchange Structure Through Data Analysis

---

### 🛠️ Tech Stack

![Python](https://img.shields.io/badge/Python-3.11-blue)
![Pandas](https://img.shields.io/badge/Pandas-Data_Analysis-important)
![NumPy](https://img.shields.io/badge/NumPy-Computations-informational)
![Seaborn](https://img.shields.io/badge/Seaborn-Visualization-success)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Plotting-orange)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626)

---
# 📌 Project Overview

This project performs an in-depth **Exploratory Data Analysis (EDA)** on a Nasdaq stock market security dataset to understand:

- Market structure
- Security classifications
- ETF behavior
- Financial stability patterns
- Exchange-specific characteristics
- Nasdaq compliance indicators

The dataset contains traditional company stocks, ETFs, and specialized investment products listed across Nasdaq and related exchanges.

---

# 🛠️ Tech Stack

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Jupyter Notebook

---

# 📂 Dataset Features

| Feature | Description |
|---|---|
| Nasdaq Traded | Whether the security trades on Nasdaq |
| Symbol | Unique ticker symbol |
| Security Name | Full security/company name |
| Listing Exchange | Official listing exchange |
| Market Category | Nasdaq market tier classification |
| ETF | Indicates whether the security is an ETF |
| Round Lot Size | Standard trading lot size |
| Financial Status | Financial/compliance condition |
| CQS Symbol | Consolidated quotation symbol |
| NASDAQ Symbol | Nasdaq-specific ticker symbol |
| NextShares | Specialized investment product indicator |

---

# 🧹 Data Cleaning & Missing Value Handling

## Financial Status
- Missing values were replaced with `N`
- Nasdaq explicitly flags problematic securities (`D/E/H`)
- Missing values mostly implied normal status

---

## Market Category Handling

- Blank (`' '`) values were not treated as traditional missing values
- `Q`, `G`, and `S` categories apply mainly to regular Nasdaq-listed companies
- ETF-related blanks were labeled as `ETF`
- Remaining blanks were labeled as `Not Applicable`
- This preserved real-world market meaning and avoided incorrect labeling

---

## CQS Symbol Handling

- Missing values were filled using the `Symbol` column
- Since both columns were nearly identical, `CQS Symbol` was dropped later due to redundancy

---

# 📊 Univariate Analysis

## Financial Status Distribution


### Insights
- Most securities are financially stable
- Distressed securities are very rare

---

## Listing Exchange Distribution


### Insights
- Nasdaq contains the largest number of securities
- Some exchanges contain only limited listings

---

## Market Category Distribution

### Insights
- Many securities fall outside traditional Nasdaq categories
- Nasdaq contains both regular stocks and investment products

---

## ETF Distribution


### Insights
- Most securities are non-ETFs
- ETFs still represent a significant market segment

---

# 📈 Bivariate Analysis

## Listing Exchange vs ETF


### Insights
- NYSE Arca and Cboe are ETF-focused exchanges
- Nasdaq contains both regular stocks and ETFs

---

## Financial Status vs ETF


### Insights
- ETFs appear more financially stable
- Most ETFs fall under Financial Status `N`

---

## Listing Exchange vs Financial Status


### Insights
- Financial warning labels mainly appear in Nasdaq-listed securities
- Financial Status reflects Nasdaq-specific compliance monitoring

---

## Financial Status vs Market Category


### Insights
- Smaller companies show relatively higher financial risk
- Larger companies appear more stable

---

# 🔥 Multivariate Analysis

## Correlation Heatmap
- A correlation heatmap was used to understand relationships between different

### Key Observations
- Market Category strongly depends on Listing Exchange
- ETFs mostly fall outside traditional company categories
- `NASDAQ Symbol` and `Symbol` are nearly identical

---

# 💡 Major Insights

- Most securities are financially stable
- ETFs are generally more stable than regular company stocks
- Smaller companies show relatively higher financial risk
- Different exchanges specialize in different security types
- Nasdaq contains stocks, ETFs, and specialized investment products
- Financial Status mainly reflects Nasdaq’s internal monitoring system
- Most securities follow the standard 100-share trading structure

---

# ⚠️ Data Issues & Limitations

- No historical stock price data
- No date/time column
- No trading volume or market capitalization
- Some redundant features exist
- Financial Status is mainly Nasdaq-specific

---

# 🚀 Future Improvements

- Add historical stock price data
- Include market capitalization
- Add sector/industry information
- Perform time-series analysis
- Build predictive/risk-analysis models

---

# 📁 Project Structure

```text
NASDAQ-Stock-Market-EDA/
│
├── data/
│   └── nasdaq_dataset.csv
│
├── notebooks/
│   └── stock_market_eda.ipynb
│
├── README.md
├── requirements.txt
└── .gitignore
