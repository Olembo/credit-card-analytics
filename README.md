# 💳 Credit Card Analytics: Risk, Spend & Behavior

This project analyzes over **44,000+ credit card transactions** from **Dec 2023 to May 2024** across 8 countries. It showcases end-to-end analytics using **Python, SQL, and Tableau** to detect risk, track spend behavior, and deliver stakeholder-ready insights.

---

## 📁 Dataset Summary

The dataset includes:

- `transaction_id`, `customer_id`, `merchant`
- `date`, `amount`, `currency`, `category`, `country`
- `card_type`, `flagged`, `is_international`

Data quality issues included:
- Missing values in `amount`, `date`, and `category`
- Typos in `category` and `card_type`
- Mixed currencies requiring normalization

---

## 🧼 Data Cleaning (Python – pandas)

- Parsed `date` and fixed invalid formats
- Converted `amount` to float
- Cleaned and standardized `category`, `card_type`
- Converted `flagged` and `is_international` to Boolean
- Filled missing `category` as "Unknown"; dropped null `amount` and `date`
- Created `amount_usd` using assumed exchange rates

---

## 📊 Exploratory Analysis (Python)

**Key Metrics:**
- 💰 Total Spend: $1.3M  
- 💳 Avg. Transaction: $54.28  
- 🔍 Outliers (> $159.82): 2,223 transactions  
- 🌍 % International: 20.5%  
- 🚩 % Flagged: 0.7%  
- 🧑 Top Spender: Customer 1097 ($5,832)  
- 🏆 Most Used Card: AmEx (9,681 transactions)

**Business Insights:**
- Spending rose 17% from Feb to May 2024 — likely seasonal or campaign-driven
- AmEx users spent more than MasterCard or Visa users
- UK, USA, and Singapore drove the highest spend
- Customers with frequent high-value outliers identified for risk review

---

## 🗃️ SQL Analysis (SQLite)

Used structured queries to:
- Validate Python findings
- Create views for Tableau
- Answer stakeholder questions on:
  - Monthly volume by country
  - Spend by card type
  - Flagged and international usage patterns

---

## 📈 Tableau Dashboard

**Title:** _Credit Card Analytics, Flag & Behavior_

📌 **KPI Cards**
- Total Spend
- Avg. Transaction Size
- % International
- % Flagged
- Top Spender
- Most Used Card

📊 **Charts**
- Monthly Spend Trend (Line)
- Spend by Country & Month (Heatmap)
- Spend by Card Type (Bar)
- Spend by Category (Bar)
- Flagged Over Time (Bar)
- % International by Country (Stacked Bar)
- Outlier Detection (Box Plot)

🎛️ **Filters**
- Card Type, Country, Date Range, Flagged Status, Customer ID, Is International

---

## 🧠 Business Questions Answered

- Are flagged or risky transactions increasing?
- What card types and countries drive the most volume?
- Who are the top or unusual customers?
- Where can marketing optimize spend or target new segments?

---

## 🛠️ Tools Used

| Tool | Purpose |
|------|---------|
| **Python** | Data cleaning, wrangling, and EDA |
| **SQLite + SQL** | Structured queries and KPI tracking |
| **Tableau** | Interactive dashboard and storytelling |

---

## 📌 Outcome

- ✅ End-to-end project for portfolio
- ✅ Demonstrated SQL + Python + Tableau integration
- ✅ Clear insights & strong business communication

📁 _This project is part of a broader effort to build a data analytics portfolio aligned to roles in finance, marketing, or product analytics._

---

**Author**: Devin Richmond  
**Date**: July 21, 2025  
**Project**: _Credit Card Usage Trend & Anomaly Detection_
