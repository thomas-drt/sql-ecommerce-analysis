E-Commerce Sales Analysis — SQL Discovery Project

1. Project Overview

This project is a SQL discovery and practice project focused on analyzing e-commerce sales data to extract business-oriented KPIs.

The main goal is to use SQL to transform raw transactional data into actionable insights related to revenue, customers, and products.
The project was developed step-by-step in a Jupyter Notebook using SQLite and Python (pandas).

⸻

2. Dataset Description

The dataset contains e-commerce transaction records, where:
	•	Each row represents one product sold on one invoice
	•	The data includes both customer and product information
	•	The dataset spans approximately one year of sales activity

Key columns used in the analysis:
	•	InvoiceNo
	•	InvoiceDate
	•	CustomerID
	•	StockCode
	•	Description
	•	Quantity
	•	UnitPrice
	•	Country

The dataset contains data quality issues such as cancellations, negative quantities, and missing customer IDs, which required explicit cleaning rules.

⸻

3. Data Cleaning & Business Rules

Before computing any KPI, the following business rules were applied:
	•	Excluded rows where Quantity <= 0 (returns or cancellations)
	•	Excluded rows where UnitPrice <= 0
	•	Excluded invoices with missing InvoiceNo
	•	Excluded transactions without a CustomerID

These filters ensure that all KPIs are based on real, completed sales only.

⸻

4. Key Business KPIs

The analysis focuses on core commercial indicators commonly used in retail analytics.

 Revenue Analysis
	•	Total revenue generated
	•	Revenue by country
	•	Revenue by customer (Top customers)

 Customer Analysis
	•	Number of orders per customer
	•	Average invoice value
	•	Last purchase date per customer (recency indicator)

 Product Analysis
	•	Best-selling products by quantity sold

All KPIs were computed using SQL aggregation functions (SUM, COUNT, AVG) and grouping logic aligned with the data granularity.

⸻

5. Tools & Technologies
	•	SQL (SQLite)
	•	Python
	•	pandas
	•	Jupyter Notebook

SQL queries were executed directly from Python using pandas.read_sql().

⸻

6. Challenges & Learnings

This project helped reinforce several important SQL concepts:
	•	Understanding data granularity before aggregation
	•	Applying business logic filters before computing KPIs
	•	Working with dates and timestamps
	•	Using GROUP BY correctly for customer-level and invoice-level metrics
	•	Discovering CTEs (Common Table Expressions) and when they simplify complex queries
	•	Recognizing how small SQL mistakes can significantly impact KPI results

⸻

7. Possible Improvements

This project could be extended with:
	•	Full RFM segmentation
	•	Customer retention and churn analysis
	•	Time-based revenue trends (monthly, weekly)
	•	Data visualization dashboards
	•	Migration to a production-level database (PostgreSQL)

⸻

8. Conclusion

This project provided hands-on experience with SQL applied to real business questions.
It emphasizes not only query writing, but also data validation, business logic, and analytical thinking, which are essential skills for data analytics roles.