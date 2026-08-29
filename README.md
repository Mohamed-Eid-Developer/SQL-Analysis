# E-Commerce SQL Data Analysis Project 

Welcome to my first SQL data analysis project! This project focuses on cleaning, exploring, and analyzing an e-commerce transactional dataset using **SQL Server (T-SQL)**. 

---

## 📌 Project Overview
As an aspiring Data Analyst, this project represents my first practical step into real-world data handling. The main objectives were to:
1. **Explore and Clean the Data:** Handle missing values, filter out anomalies (such as negative quantities and zero unit prices), and manage cancellations.
2. **Business Insights & Exploratory Data Analysis (EDA):** Extract meaningful business metrics including top customers, total sales, geographic performance (best and worst-performing countries), and cancellation patterns.

---

## Tech Stack
* **Database Management System:** Microsoft SQL Server (T-SQL)
* **Key Concepts:** Data Cleaning (`DELETE`, `COALESCE`, `NULL` handling), Aggregations (`SUM`, `COUNT`), Grouping (`GROUP BY`), Sorting (`ORDER BY`), Subqueries, and Conditional Filtering (`LIKE`).

---

## 🔍 Step-by-Step Breakdown of the SQL Code

### Phase 1: Data Exploration & Cleaning
* **Checking for Nulls & Anomalies:** Inspected the dataset for missing descriptions, quantities, and customer IDs.
* **Handling Invalid Quantities & Prices:** 
  * Filtered and removed records where quantities were non-positive unless they represented legitimate cancellations (invoices starting with 'C').
  * Deleted rows with zero unit prices.
* **Managing Missing Customer IDs:** Explored the impact of `NULL` customer IDs and demonstrated how to handle them using `COALESCE` (labeling guests/unregistered users).

### Phase 2: Exploratory Data Analysis (Business Questions)
* **Top Customers:** Retrieved sample records to identify high-value customer interactions.
* **Total Sales Calculation:** Computed total sales per line item (`Quantity * UnitPrice`).
* **Geographic Performance:** 
  * Identified the country generating the **largest total sales**.
  * Identified the country with the **lowest total sales**.
* **Cancellation Analysis:** Counted total order cancellations (`InvoiceNo LIKE 'C%'`) and explored transactional details.

---

## Future Improvements & Next Steps
To take this project to the next level, I plan to:
1. **Create Permanent Cleaned Tables:** Instead of deleting data directly in production views, use staging tables or database views.
2. **RFM Analysis:** Implement Recency, Frequency, and Monetary analysis to segment customers.
3. **Time-Series Analysis:** Analyze sales trends by month, day of the week, and peak hours.
4. **Data Visualization:** Connect this database to Power BI or Tableau to build an interactive dashboard.

---
*Created with passion by a Data Analysis enthusiast!*
