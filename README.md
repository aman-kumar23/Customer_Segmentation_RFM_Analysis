# E-Commerce Customer Segmentation (RFM Analysis)

## 📌 Project Overview
This data analytics project focuses on segmenting e-commerce customers based on their purchasing behavior using **RFM (Recency, Frequency, Monetary)** analysis. By analyzing transactional data, this project identifies high-value customers, loyalists, and customers at risk of churning, providing actionable insights for targeted marketing strategies.

## 📊 Dataset
- **Source:** Online Retail Dataset (Kaggle/UCI Machine Learning Repository)
- **Size:** Initially contained over 540,000 transaction records.
- **Data Cleaning:** Removed missing `CustomerID` values, filtered out negative quantities (cancelled orders), and fixed datetime anomalies, resulting in a clean dataset of ~397,000 rows ready for analysis.

## 🛠️ Tech Stack
- **Language:** Python
- **Libraries:** Pandas, Datetime
- **Environment:** Jupyter Notebook

## ⚙️ Methodology
1. **Data Wrangling:** Cleaned data by handling null values and removing incorrect entries.
2. **Feature Engineering:** Calculated the `TotalAmount` spent per transaction.
3. **RFM Calculation:**
   - **Recency (R):** Days since the customer's last purchase.
   - **Frequency (F):** Total number of transactions per customer.
   - **Monetary (M):** Total amount spent by the customer.
4. **Scoring & Segmentation:** Grouped customers into quartiles (1-4) using `pd.qcut` for each metric and calculated a final aggregated `Total_Score`. 
5. **Business Labeling:** Assigned customers to strategic business tiers based on their overall scores.

## 📈 Results & Customer Segments
Based on the analysis of ~4,300 unique customers, they were successfully categorized into 5 distinct business segments:
- 🏆 **Champions (Score >= 11):** 839 customers - Our best, most loyal, and highest spending customers.
- 🥇 **Loyal Customers (Score 9-10):** 846 customers - Customers who buy consistently.
- 🎯 **Potential Loyalists (Score 7-8):** 914 customers - Recent customers with average purchase frequency.
- ⚠️ **Needs Attention (Score 5-6):** 980 customers - Customers whose recency and frequency are dropping.
- 🚨 **Lost / At Risk (Score <= 4):** 759 customers - Customers with the lowest recency, frequency, and monetary scores.

## 🚀 How to Use
1. Clone this repository to your local machine.
2. Ensure you have the `online_retail.csv` dataset in the same directory.
3. Open the Jupyter Notebook file.
4. Run all cells sequentially to view the data cleaning process and final RFM table generation.
   
