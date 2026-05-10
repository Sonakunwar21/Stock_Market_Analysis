<div align="center">

# 🚀 NASDAQ Stock Market Analysis

### Exploratory Data Analysis of Securities, ETFs & Financial Stability

<br>

![Python](https://img.shields.io/badge/Python-Data%20Analysis-blue?style=for-the-badge&logo=python)
![Pandas](https://img.shields.io/badge/Pandas-EDA-important?style=for-the-badge)
![Seaborn](https://img.shields.io/badge/Visualization-Seaborn-success?style=for-the-badge)
![Matplotlib](https://img.shields.io/badge/Plots-Matplotlib-orange?style=for-the-badge)
![Project](https://img.shields.io/badge/Project-Completed-brightgreen?style=for-the-badge)

<br>

### 📊 Understanding Modern Financial Market Structures Through Data

</div>

---

# 📌 Project Overview

This project performs Exploratory Data Analysis (EDA) on a NASDAQ stock market dataset to understand:

- Different types of securities traded in the market
- Distribution of exchanges and market categories
- Financial stability of companies
- ETF and non-ETF behavior
- Nasdaq-specific compliance indicators
- Relationships between market features

The analysis mainly focuses on understanding the structure of stock market securities rather than prediction or machine learning.

---

# 🛠️ Tech Stack

## Libraries Used

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
| Symbol | Unique stock/security ticker |
| Security Name | Name of company/security |
| Listing Exchange | Exchange where security is listed |
| Market Category | Nasdaq market tier/category |
| ETF | Whether security is ETF or not |
| Round Lot Size | Standard trading lot size |
| Financial Status | Financial/compliance condition |
| Nasdaq Traded | Whether tradable through Nasdaq system |
| Test Issue | Test or real tradable security |
| CQS Symbol | Secondary ticker identifier |
| NASDAQ Symbol | Nasdaq ticker symbol |
| NextShares | Special investment product indicator |

---

# 🧹 Handling Missing Values

## Financial Status

Missing values in the Financial Status column were replaced with **"N" (Normal)** because Nasdaq generally flags problematic companies explicitly using categories like D, E, or H. Therefore, missing values most likely indicate no financial issue.

---

## CQS Symbol

Missing values in the CQS Symbol column were filled using corresponding values from the Symbol column because both columns mostly represented the same ticker identifier.

After verification, the column became redundant and added little new information.

---

## Market Category

Blank values in the Market Category column were not treated as missing immediately.

- Q, G, and S categories apply mainly to regular Nasdaq-listed companies.
- Many securities in the dataset were ETFs, which do not belong to these categories.

Therefore:
- ETF securities with blank categories were labeled as **ETF**
- Remaining blanks were labeled as **Not Applicable**

This kept the dataset more realistic and meaningful.

---

# 📊 Univariate Analysis

## Financial Status Distribution

### Insights

- Most securities are financially stable
- Distressed securities are very rare
- Dataset is dominated by normal companies

---

## Listing Exchange Distribution

### Insights

- NASDAQ contains the largest number of securities
- Some exchanges contain only limited listings
- Multiple exchanges are present in the dataset

---

## Market Category Distribution

### Insights

- Many securities do not belong to standard Nasdaq categories
- Q category contains the largest number of companies
- Dataset includes both traditional and non-traditional securities

---

## ETF Distribution

### Insights

- Most securities are non-ETFs
- ETFs still represent a significant portion of the market
- Investment products are an important part of modern markets

---

## Round Lot Size Distribution

### Insights

- Most securities trade in standard lots of 100 shares
- Very few securities use lot sizes of 1 or 10
- Smaller lot sizes are rare but valid market cases

---

# 📊 Bivariate Analysis

## Listing Exchange vs Market Category

### Insights

- Q, G, and S categories appear mainly for Nasdaq-listed securities
- Other exchanges mostly have undefined market categories
- Market category system is strongly Nasdaq-specific

---

## Listing Exchange vs ETF

### Insights

- NYSE mainly contains regular company stocks
- NYSE Arca and Cboe contain many ETFs
- Different exchanges focus on different security types

---

## Financial Status vs ETF

### Insights

- Most ETFs are financially stable
- Distressed categories are mostly associated with regular companies
- ETFs rarely appear in risky financial categories

---

## Financial Status vs Market Category

### Insights

- Most companies across all categories are financially stable
- Distressed companies are mainly concentrated in Nasdaq categories
- Financial monitoring is more visible in Nasdaq-listed firms

---

## Listing Exchange vs Financial Status

### Insights

- Financial status information mainly appears for Nasdaq-listed securities
- Most securities across exchanges belong to normal category N
- Nasdaq seems to maintain stronger compliance tracking

---

# 📊 Multivariate Analysis

## Correlation Heatmap

### Insights

- Listing Exchange and Market Category are strongly related
- ETF shows moderate relationship with Market Category
- Financial Status is highly connected with Nasdaq categories
- Some features are redundant and highly correlated

---

# 🔍 Major Insights

- Most companies and securities are financially stable
- ETFs form a major part of the modern stock market
- Nasdaq contains companies, ETFs, and special investment products
- Smaller company categories generally show higher risk
- Financial Status feature appears Nasdaq-specific
- Most securities trade in standard lot sizes
- Different exchanges specialize in different types of securities
- Dataset captures both traditional stocks and non-traditional financial products

---

# ⚠️ Data Issues Noted

- Dataset lacks historical stock price information
- No sector or industry information available
- No market capitalization data
- Some features are highly redundant
- Financial Status mainly applies to Nasdaq-listed securities

---

# 🚀 Future Improvements

- Add historical stock price data
- Include sector and industry information
- Add market capitalization
- Perform time-series analysis
- Build predictive or risk-analysis models

---

# ✅ Final Conclusion

- This analysis shows that modern stock markets contain many different types of securities beyond regular company stocks.
- Most securities in the dataset are financially stable, while ETFs and other investment products also play an important role in the market ecosystem.
- The project also highlights Nasdaq’s structured market categorization and financial monitoring system.

---

</div>
# 📁 Project Structure

```text
Stock_Market_Analysis/
│
├── data/
│   └── stock_market_dataset.csv
│
├── notebooks/
│   └── stock_market_eda.ipynb
│
├── README.md
├── requirements.txt
└── .gitignore
