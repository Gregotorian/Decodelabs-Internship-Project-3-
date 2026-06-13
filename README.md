Project 3 – Sales Insights Using SQL in BigQuery
Overview

This project focuses on analyzing sales transaction data using SQL queries in Google BigQuery. The objective was to generate business insights from product sales data by calculating order volume, quantity sold, average unit price, and total revenue.

The analysis helps identify top-performing products and provides insights into sales performance based on completed deliveries.



The main goals of this project were to answer this question:

What was the  product sales performance?
What was the highest-performing products based on revenue?

Objective

Calculate total orders per product
Measure quantity sold
Determine average product pricing
The Compute total revenue generated

Technologies Used
Google BigQuery
SQL
Google Cloud Platform (GCP)
SQL Concepts Applied

The project demonstrates the use of:
SELECT
COUNT()
SUM()
AVG()
ROUND()
WHERE
GROUP BY
ORDER BY
LIMIT
SQL Query
-- Basic insights query for Project_3

SELECT
    Product,
    COUNT(OrderID) AS total_orders,
    SUM(Quantity) AS total_quantity_sold,
    ROUND(AVG(UnitPrice), 2) AS avg_unit_price,
    ROUND(SUM(TotalPrice), 2) AS total_revenue
FROM `data-analysis-495313.Decodelabs.Project_3`
WHERE OrderStatus = 'Delivered'
GROUP BY 1
ORDER BY total_revenue DESC
LIMIT 1000;

Key Insights:
| Product | Total Orders | Quantity Sold | Total Revenue |
| ------- | ------------ | ------------- | ------------- |
| Laptop  | 40           | 121           | 40,714.43     |
| Phone   | 38           | 101           | 40,345.41     |
| Printer | 29           | 88            | 38,054.73     |
| Monitor | 31           | 96            | 35,999.62     |


Observations
Laptops generated the highest revenue.
Phones recorded strong sales performance with high average pricing.
Printers and monitors also contributed significantly to overall revenue.
Delivered orders were filtered to focus only on completed transactions.
Business Value

This analysis can help businesses:

Identify best-selling products
Monitor sales performance
Improve inventory planning
Support pricing decisions
Track revenue generation
Improve operational reporting
Skills Demonstrated
SQL Query Writing
Data Aggregation
Business Analysis
Data Interpretation
Cloud-Based Analytics
BigQuery Usage
Future Improvements

Potential enhancements include:

Monthly sales trend analysis
Customer segmentation
Regional sales analysis
Profit margin analysis
Dashboard creation using Power BI or Tableau
Automated reporting pipelines
Author

Omotunde Oluwatimilehin Gregory

Aspiring Data Analyst | Accounting Graduate | Financial Analytics Enthusiast
