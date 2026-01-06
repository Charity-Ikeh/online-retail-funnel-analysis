# Online Retail Funnel Analysis (Power BI)

## Project Overview

This project analyses an online retail dataset to understand customer behaviour across the sales funnel. The analysis focuses on how customers convert into orders and revenue, using Power BI and DAX to produce clear and actionable metrics.

The project answers the following business questions:

- How many unique customers placed orders?
- How many orders were generated?
- What is the total revenue?
- What is the average order value?
- Is there evidence of repeat purchasing behaviour?

## Key Funnel Metrics

| Metric | Value |
|------|------|
| Total Customers | 179 |
| Total Orders | 248 |
| Total Revenue | £91,037.72 |
| Average Order Value (AOV) | £367.09 |

## Insights

The number of orders exceeds the number of customers, indicating that some customers placed multiple orders.

The average order value is relatively high, suggesting that revenue is driven by higher value transactions rather than large order volumes.

The funnel structure highlights opportunities to improve customer retention and increase customer lifetime value.

These metrics provide a clear overview of acquisition, conversion, and revenue performance.

## Tools and Techniques

- Power BI Desktop  
- DAX for calculated measures  
- DISTINCTCOUNT for customer and order calculations  
- DIVIDE for average order value calculation  
- KPI card visualisations  
- Data aggregation and modelling  

## DAX Measures

```DAX
Total Customers =
DISTINCTCOUNT(Online_Retail_eda_clean_Data[CustomerID])

Total Orders =
DISTINCTCOUNT(Online_Retail_eda_clean_Data[InvoiceNo])

Total Revenue =
SUM(Online_Retail_eda_clean_Data[Revenue])

AOV =
DIVIDE(
    SUM(Online_Retail_eda_clean_Data[Revenue]),
    DISTINCTCOUNT(Online_Retail_eda_clean_Data[InvoiceNo])
)

Files Included

Online_Retail_Funnel_Analysis.pbix

Cleaned dataset

README.md
