## 📌 Project 1: Analyzing Facebook Ad Costs with SQL
**Description:**  
This project is the first assignment of the SQL module in the Data Analyst course I am taking from GoIT educational institution. The goal is to analyze Facebook Ads to determine the cost per click (CPC).  

## 📝 Project Overview
This SQL query analyzes Facebook advertising data to calculate the cost per click (CPC). The dataset contains daily spending and clicks for various ads.

**SQL techniques used:**  
- Filtering (`WHERE` clause)  
- Ordering (`ORDER BY`)  
- Basic calculations  

## 🔍 Key Steps in the Query:
1. Selected relevant columns: `ad_date`, `spend`, `clicks`, and calculated `CostPerClick (spend/clicks)`.
2. Filtered out records where the number of clicks is zero to avoid division errors.
3. Sorted the results in descending order based on `ad_date`.

### 🔍 Query:
```sql
SELECT ad_date, spend, clicks, spend/clicks AS CostPerClick
FROM facebook_ads_basic_daily
WHERE clicks > 0
ORDER BY ad_date DESC;
