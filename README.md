# Payday-Anomaly-Pre-COVID-vs-Post-COVID-Market-Behavior
Data Visualization using Python
## Google Colab
This project is designed in Google Colab.

Google colab link: *[https://drive.google.com/file/d/1zI5B0p1Fb0zSYdH8I6aTJOwbuzMF4TRa/view?usp=sharing](https://drive.google.com/file/d/1rI1Lx1je8XDdEgNM7OADhj6W95Mvgfr0/view?usp=sharing)*
---

## Project Overview
This project investigates the **Payday Anomaly**, a documented market phenomenon where stock returns exhibit abnormal patterns around common payroll dates. Building on the research by Aixin Ma and William R. Pratt, this analysis examines whether the anomaly persists and how it has changed **before and after COVID-19**.

Using historical price data for **QQQ (NASDAQ-100 ETF)**, the project analyzes calendar-based return patterns, payday-relative return behavior, weekday effects, volatility, and long-term cumulative performance.

The goal is to combine **financial data analysis**, **feature engineering**, and **clear visualization** to evaluate whether structural economic changes have altered established market inefficiencies.

---

## Academic Reference
- Ma, Aixin & Pratt, William R.  
  *“Payday Anomaly”*  
  SSRN: https://papers.ssrn.com/sol3/papers.cfm?abstract_id=3257064

---

## Data Source
- **Asset**: QQQ (NASDAQ-100 ETF)
- **Price Data**: Yahoo Finance (via `yfinance`)
- **Timeframe**: 1999-03-10 to 2025-04-10
- **Frequency**: Daily trading data

---

## Tools & Technologies
- Python  
- Pandas  
- NumPy  
- Matplotlib  
- Seaborn  
- yfinance  
- Jupyter Notebook (Google Colab compatible)

---

## Data Preparation & Feature Engineering

### Returns
- Daily returns calculated using percentage change of the closing price.

### Calendar Features
- Day of month (1–31)
- Day of week (Monday–Friday)

### Period Classification
- **Pre-COVID**: Dates before March 1, 2020
- **Post-COVID**: Dates on or after March 1, 2020

### Payday Identification
Paydays are defined as:
- The **16th of the month** (mid-month payday)
- The **last trading day of the month** (month-end payday)

A binary indicator flags payday observations.

### T-X Index (Relative to Payday)
For each identified payday, business-day offsets are assigned:
- **T-2, T-1, T+0, T+1, T+2**

This allows analysis of return behavior immediately before and after payday events.

---

## Visualizations & Analysis

### 1. Average Returns by Calendar Day
- Grouped bar chart comparing **Pre-COVID vs Post-COVID**
- Highlights key anomaly days (Day 1 and Day 16)

**Insight**:  
Calendar-based return patterns persist, but the magnitude and consistency of anomalies differ across periods.

---

### 2. Average Returns by T-X Index (Payday Effect)
- Bar chart showing mean returns from **T-2 to T+2**
- Direct comparison between Pre-COVID and Post-COVID periods
- Annotated differences between periods

**Insight**:  
Market reactions around payday events appear to have shifted post-COVID, suggesting changes in liquidity, automation, or investor behavior.

---

### 3. Average Returns by Weekday
- Monday–Friday comparison across periods
- Highlights changes in classic weekday effects

**Insight**:  
Differences between Pre-COVID and Post-COVID weekday returns indicate evolving trading patterns and sentiment.

---

### 4. Volatility Around Payday (Standard Deviation)
- Standard deviation of returns by T-index
- Compared across periods

**Insight**:  
Post-COVID volatility around payday events suggests increased uncertainty, even when average returns are positive.

---

### 5. Cumulative Returns Over Time
- Line chart of compounded returns
- Separate curves for Pre-COVID and Post-COVID periods

**Insight**:  
Short-term anomalies contribute to long-term performance differences, but broader market structure ultimately dominates cumulative returns.

---

## Key Findings
- Payday-related return anomalies are visible in historical QQQ data
- The strength and timing of the anomaly changed after COVID-19
- Volatility around payday increased in the Post-COVID period
- Calendar effects remain relevant but are not static over time
- Structural economic shifts likely influence market inefficiencies

---

## Implications
- Investors should be cautious when relying on historical calendar anomalies
- Behavioral and liquidity-driven effects evolve with economic structure
- Market efficiency is dynamic rather than absolute

---

## How to Run (Google Colab)
This project is designed to be run in Google Colab.

Steps:
1. Open the notebook file
2. Run all cells from top to bottom
3. All data is downloaded programmatically using `yfinance`

---

## Author
**Dalia Do**
