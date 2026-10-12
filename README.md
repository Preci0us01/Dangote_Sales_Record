# 📊 Dangote Sales Record 2023
## Table of contents
- [Project Overview](#project-overview)
- [Data Sources](#data-source)
- [Tools](#tools)
- [Data Cleaning](#data-cleaning)
- [Exploratory Data Analysis](#exploratory-data-analysis)
- [Data Analysis](#data-analysis)
- [Results/findings](#resultsfindings)
- [Recommendations](#recommendations)
- [Limitations](#limitations)
- [References](#references)
  


## Project Overview

The **Dangote Cement Record 2023** report provides a high-level and granular operational analysis of sales performance, production costs, regional distribution, and delivery logistics across Nigeria. It tracks core 
financial  growth, evaluates product and regional market penetration, monitor payment preferences, and identifies key order fulfilment bottlenecks.


## Data Source

The dataset is gotten from **Kaggle**.

## Tools
- **Excel:** - Initial data inspection [Download here](https://microsoft.com)
- **Power Query:** - Data cleaning,ETL, and transformation.
- **SQL Server:** - Advanced data Analysis and querying [Download here](https://mysqlserver.com)
- **PowerBI:** - DAX measures, dynamic visuals, and report development.


### Data Cleaning

In the initial data preparation phase, we performed the following tasks:
1. Data loading and Inspection
2. Handling missing values
3. Correcting wrong data types
4. Data Cleaning and formatting



### Exploratory Data Analysis

EDA  involved exploring the sales data to answer key questions, such as:

1. Total revenue & profit  generated in 2023.
2. The best preforming state in term of revenue generation.Da
3. Revenue generation across the different regions.
4. Daily trend by Sales
5. Which mode of payment do our customers refer?


### Data Analysis


Include some interesting code/feature worked with
``` sql
-- MONTHLY TREND BY SALES FILTER BY PRODUCT TYPE
SELECT
	MONTHNAME(date) AS Month,
    SUM(total_sales_n) AS Total_sales
FROM DANG
WHERE product_type ='clinker'
GROUP BY MONTHNAME(date)
ORDER BY Total_sales DESC;
```


### Results/Findings

- Sales are split across three primary product types: **Bagged Cement**(₦27.73M),**Clinker**(₦26.34M) and **Bulk Cement**(₦19.54M)
- The **South South** region leads with ₦14.16M, followed by North Central (₦12.74M), North East(₦11.95M), North West(₦12.98M),South East(₦11.7M), and South West(₦10.1M).
- Transactions are evenly distributed across payment options, led by Credit(134), Cash(128),POS(121 and bank transfer (117))
- Yobe is highlighted as the best-performing state in terms of high revenue generated
- Daily tramsaction volumes fluctuate significantly throughout the month, showing sharp peaks around %,12 and 20, with significant dips in between.
- Out of the tracked orders,176 are cancelled, 169 are delivered, 148 are pending and 7 were blank and i converted to to unspecified.


### Recommendations


1. Reallocate promotional efforts and key account manager to underperforming areas like South West to balance regional growth.

2. Focus bulk sales efforts on large-scale infrastructure and commercial constructionprojects, while bundling bagged cement products for local retail distributors.
3. Audit dispatch routes and optimize fleet logistics to reduce lead times and shift pending orders into completed sales faster .
4. Tighten credit terms or incentivize digital payment(POS and Bank transfer) via small prompt-payment discounts to accelerate cash conversion cycles and reduce bad debt exposure.


### Limitations
1. They were missing values in the delivery status which i input "unspecified".
2. Improper data type in the date column.
3. Some missing values in the unit which i corrected using calculated column in power query


### References
- Kaggle Sales dataset [download here](https://www.kaggle.com)
- Applied Frameworks : Utilizes Power Query for ETL data cleaning pipeline, and DAX Measures
- SQl for business




