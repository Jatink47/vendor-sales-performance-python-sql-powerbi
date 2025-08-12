## Vendor Performance Analysis – Retail Inventory & Sales

Analyzing vendor efficiency and profitability to support strategic purchasing and inventory decisions using SQL, Python, and Power BI.


## 📑 Table of Contents
1. [Overview](#overview)
2. [Business Problem](#business-problem)
3. [Dataset](#dataset)
4. [Tools & Technologies](#tools--technologies)
5. [Project Structure](#project-structure)
6. [Data Cleaning & Preparation](#data-cleaning--preparation)
7. [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)
8. [Research Questions & Key Findings](#research-questions--key-findings)
9. [Dashboard](#dashboard)
10. [Final Recommendations](#final-recommendations)

## Overview 
This project evaluates vendor performance and retail inventory dynamics to drive strategic insights for purchasing, pricing, and inventory optimization. A complete data pipeline was built using SQL for ETL, Python for analysis and hypothesis testing, and Power BI for visualization.

## Business Problem
Effective inventory and sales management are critical in the retail sector. This project aims to:

1. Identify underperforming brands needing pricing or promotional adjustments
2 .Determine vendor contributions to sales and profits
3. Analyze the cost-benefit of bulk purchasing
4. Investigate inventory turnover inefficiencies
5. Statistically validate differences in vendor profitability

## Dataset
- Multiple CSV files  (sales, vendors, inventory) located in [data](https://github.com/Jatink47/vendor-sales-performance-python-sql-powerbi/tree/main/data)
- Summary table created from ingested data and used for analysis

## Tools & Technologies
- SQL (Common Table Expressions, Joins, Filtering)
- Python (Pandas, Matplotlib, Seaborn, SciPy)
- Power BI (Interactive Visualizations)

## Data Cleaning & Preparation
Removed transactions with:
- Gross Profit ≤ 0
- Profit Margin ≤ 0
- Sales Quantity = 0
- Created summary tables with vendor-level metrics  
- Converted data types, handled outliers, merged lookup tables

## Exploratory Data Analysis (EDA)
**Negative or Zero Values Detected:**

- **Gross Profit:** Min -3175391.01 (loss-making sales)
- **Profit Margin:** Min -∞ (sales at zero or below cost)
- **Unsold Inventory:** Indicating slow-moving stock

**Outliers Identified:**
- High Freight Costs (up to 257K)
- Large Purchase/Actual Prices
**Correlation Analysis:**

- Weak between Purchase Price & Profit
- Strong between Purchase Qty & Sales Qty (0.999)
- Negative between Profit Margin & Sales Price (-0.01)

## Research Questions & Key Findings
1. **Brands for Promotions:** 198 brands with low sales but high profit margins
2. **Top Vendors:** Top 10 vendors = 65.69% of purchases → risk of over-reliance
3. **Bulk Purchasing Impact:** 72% cost savings per unit in large orders

## Dashboard
- Power BI Dashboard shows:
- Vendor-wise Sales and Margins
- Inventory Turnover
- Bulk Purchase Savings
- Performance Heatmaps

  
5. **Inventory Turnover:** $2.71M worth of unsold inventory
6. **Vendor Profitability:**
- **High Vendors:** Mean Margin = 31.17%
- **Low Vendors**: Mean Margin = 41.55%
6. **Hypothesis Testing:** Statistically significant difference in profit margins → distinct vendor strategies
