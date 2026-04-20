# Task-6
Sales trade analysis using aggregates 
Task 6: Sales Trend Analysis Using SQL Objective
Analyze monthly revenue and order volume using SQL aggregation functions.
Tools Used
SQL (MySQL / PostgreSQL / SQLite)
Dataset (CSV format)
 Dataset Description
The dataset online_sales.csv contains sales transaction data with the following columns:
order_id → Unique ID for each order
order_date → Date of the order
product_id → Product identifier
amount → Revenue generated from the order
Approach
Extracted year and month from order_date
Used SUM(amount) to calculate total monthly revenue
Used COUNT(DISTINCT order_id) to calculate order volume
Grouped data by year and month
Sorted results using ORDER BY
 SQL Query
SQL
SELECT 
    EXTRACT(YEAR FROM order_date) AS year,
    EXTRACT(MONTH FROM order_date) AS month,
    SUM(amount) AS total_revenue,
    COUNT(DISTINCT order_id) AS order_volume
FROM online_sales
GROUP BY year, month
ORDER BY year, month;
Output
Year
Month
Total Revenue
Order Volume
2024
1
550
2
2024
2
550
2
2024
3
1050
3
2024
4
1300
2
2024
5
750
2
2024
6
1450
2
Key Insights
Revenue shows an increasing trend from March to June
June recorded the highest revenue (1450)
Order volume remains relatively stable across months
 Repository Contents
online_sales.csv → Raw dataset
task6.sql → SQL query file
task6_output_screenshot.png → Output screenshot
README→ Project documentation
Learning Outcome
Learned how to use aggregate functions in SQL
Understood GROUP BY and ORDER BY operations
