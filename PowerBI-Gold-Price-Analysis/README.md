# 📊 Historical Gold Price Analysis (1995-2026)

## 📖 Overview
This project is an end-to-end Microsoft Power BI data analytics solution designed to analyze over 30 years of historical gold prices. The objective of this dashboard is to move beyond standard reporting by utilizing advanced DAX time-intelligence functions and rarely used AI-driven visuals to uncover deep market trends and volatility.

## 🗄️ Dataset
* **Source:** Kaggle (Historical Gold Prices)
* **Timeframe:** 1995 – 2026
* **Key Metrics:** Date, Average Closing Price (USD)

## 🛠️ Technical Highlights & Process

### 1. Data Transformation & ETL (Power Query)
* Extracted raw CSV data and loaded it into Power BI.
* Cleaned and formatted data types for accurate time-series analysis.
* **Feature Engineering:** Extracted `Year`, `Quarter`, and `Month Name` from the primary Date column to enable multi-level drill-down capabilities.

### 2. Data Modeling & DAX Calculations
Created custom measures to analyze price ranges and smooth out market volatility:
* `Avg Gold Price` = `AVERAGE('gold_prices'[Gold_Price_USD])`
* `Max Gold Price` = `MAX('gold_prices'[Gold_Price_USD])`
* `Min Gold Price` = `MIN('gold_prices'[Gold_Price_USD])`
* `12-Month Moving Average` = Utilized advanced DAX (`CALCULATE` and `DATESINPERIOD`) to calculate a dynamic trailing 12-month average, providing a clearer view of the long-term price trend against daily fluctuations.

### 3. Data Visualization & UI
Focused on implementing advanced and rarely used visuals to enhance data storytelling:
* **Decomposition Tree (AI Visual):** Allows users to interactively break down the average price from the Year level down to specific Quarters and Months.
* **Ribbon Chart:** Visualizes rank and value shifts in gold prices across different quarters year-over-year.
* **Gauge Chart:** Anchors the current average price against the all-time historical high and low boundaries.
* **Line Chart (Trend Analysis):** Plots the raw chronological price alongside the calculated 12-Month Moving Average.

## 📸 Dashboard Preview
<img width="1918" height="843" alt="Screenshot 2026-04-18 111323" src="https://github.com/user-attachments/assets/01249f51-0c76-42a8-be9f-1df1a18210a0" />


## 🚀 How to Use
1. Download the `Historical_Price_Assignment.pbix` file from this repository.
2. Open it using **Microsoft Power BI Desktop**.
3. Interact with the Decomposition Tree and Ribbon chart to explore the historical data.

---
*Developed by Mohammed Aslam A.*
