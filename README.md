# sql-data-analytics-portfolio-project

 📌 Project Overview

This project demonstrates practical SQL data analytics skills using **Microsoft SQL Server (MSSQL)**. It focuses on analysing sales performance, customer behaviour, product performance and business trends using SQL queries.

The project uses a structured data model consisting of customer, product and sales tables to generate meaningful business insights and analytical reports.

The primary objective is to transform raw sales data into valuable insights that support data-driven business decisions.

## 🛠️ Technologies & Tools

- Microsoft SQL Server (MSSQL)
- SQL Server Management Studio (SSMS)
- SQL (Structured Query Language)

## 🗄️ Database Structure

The project uses the following tables from the `gold` schema:

| Table Name | Description |
|---|---|
| `gold.dim_customers` | Contains customer-related information. |
| `gold.dim_products` | Contains product details and classifications. |
| `gold.fact_sales` | Contains sales transactions and order information. |

### Database Schema

The database follows a dimensional data model consisting of fact and dimension tables.

- **Fact Table:** `gold.fact_sales`
- **Dimension Tables:** `gold.dim_customers`, `gold.dim_products`

## 📊 SQL Analysis & Business Questions

The project covers the following analytical areas:

### 1. Change Over Time Analysis

**Business Question:** How does sales performance change over time?

Analysis includes:
- Yearly sales performance.
- Monthly sales trends.
- Total number of customers over time.
- Total quantity sold.
- Total sales amount.

**SQL Concepts Used:**
- YEAR()
- MONTH()
- SUM()
- COUNT(DISTINCT)
- GROUP BY
- ORDER BY

### 2. Cumulative Analysis

**Business Question:** What is the cumulative sales performance over time?

Analysis includes:
- Total sales per time period.
- Running total of sales.
- Moving average of product prices.

**SQL Concepts Used:**
- Common Table Expressions (CTEs)
- Window Functions
- SUM() OVER()
- AVG() OVER()
- DATETRUNC()

### 3. Performance Analysis

**Business Question:** How do individual products perform compared with their historical average and previous-year sales?

Analysis includes:
- Yearly product sales.
- Average sales performance by product.
- Comparison against average sales.
- Year-over-Year (YoY) sales comparison.
- Identification of increasing and decreasing sales trends.

**SQL Concepts Used:**
- CTEs
- LEFT JOIN
- AVG() OVER()
- LAG()
- CASE WHEN
- PARTITION BY
- ORDER BY

### 4. Part-to-Whole Analysis

**Business Question:** Which product categories contribute the most to overall sales?

Analysis includes:
- Total sales by product category.
- Overall sales calculation.
- Percentage contribution of each category.
- Ranking categories based on sales contribution.

**SQL Concepts Used:**
- CTEs
- SUM()
- Window Functions
- CAST()
- ROUND()
- CONCAT()

### 5. Data Segmentation

**Business Questions:**

**A. Product Cost Segmentation**

Products are divided into four cost categories:

- Below 100
- 100–500
- 500–1000
- Above 1000

The analysis identifies the total number of products in each cost range.

**B. Customer Segmentation**

Customers are classified into three segments based on their spending and relationship duration:

| Segment | Criteria |
|---|---|
| VIP | At least 12 months of history and spending above 5000 |
| Regular | At least 12 months of history and spending of 5000 or less |
| New | Customer lifespan of less than 12 months |

The analysis calculates the total number of customers in each segment.

**SQL Concepts Used:**
- CASE WHEN
- DATEDIFF()
- MIN()
- MAX()
- SUM()
- COUNT()
- GROUP BY

## 📑 6. Reporting & Analytical Views

The project creates two analytical SQL views to simplify reporting and provide valuable business metrics.

### A. Customer Report – `gold.report_customers`

**Purpose:** Consolidates customer information, purchasing behavior and customer-level KPIs.

Key features:

- Customer name and demographic information.
- Customer age groups.
- Customer segmentation (VIP, Regular, New).
- Total orders.
- Total sales.
- Total quantity purchased.
- Total unique products purchased.
- Customer lifespan.
- Recency (months since last order).
- Average Order Value (AOV).
- Average Monthly Spend.

### B. Product Report – `gold.report_products`

**Purpose:** Consolidates product information, sales performance and product-level KPIs.

Key features:

- Product name and category.
- Product subcategory and cost.
- Product performance segmentation.
- Total orders.
- Total customers.
- Total sales.
- Total quantity sold.
- Average selling price.
- Product lifespan.
- Recency in months.
- Average Order Revenue (AOR).
- Average Monthly Revenue.

**SQL Concepts Used:**
- CREATE VIEW
- Common Table Expressions (CTEs)
- Multiple JOINs
- Aggregate Functions
- CASE WHEN
- DATEDIFF()
- NULLIF()
- GETDATE()

## 🧠 Key SQL Skills Demonstrated

This project demonstrates practical knowledge of the following SQL concepts:

| Category | SQL Concepts |
|---|---|
| Data Retrieval | SELECT, DISTINCT |
| Filtering | WHERE, IS NOT NULL |
| Aggregation | SUM(), AVG(), COUNT(), MIN(), MAX() |
| Data Grouping | GROUP BY, ORDER BY |
| Joins | LEFT JOIN |
| Conditional Logic | CASE WHEN |
| Date Functions | YEAR(), MONTH(), DATEDIFF(), DATETRUNC() |
| Window Functions | SUM() OVER(), AVG() OVER(), LAG() |
| CTEs | WITH clause |
| Data Conversion | CAST(), ROUND() |
| String Functions | CONCAT() |
| Database Objects | CREATE VIEW, DROP VIEW |
| Advanced Functions | NULLIF(), GETDATE() |

## 📂 Project Structure

```text
SQL-Data-Analytics-Portfolio/
│
├── README.md
│
├── SQL-Scripts/
│   ├── 01_Change_Over_Time_Analysis.sql
│   ├── 02_Cumulative_Analysis.sql
│   ├── 03_Performance_Analysis.sql
│   ├── 04_Part_to_Whole_Analysis.sql
│   ├── 05_Data_Segmentation.sql
│   └── 06_Reporting.sql
│
└── Screenshots/
    └── Query_Results/
```

## 🎯 Project Objectives

- Develop practical SQL querying skills.
- Analyze sales trends and business performance.
- Understand customer purchasing behavior.
- Identify high-performing products and categories.
- Perform customer and product segmentation.
- Create reusable SQL reporting views.
- Apply advanced SQL concepts to business analytics problems.

## 🚀 Learning Outcomes

Through this project, I gained practical experience in:

1. Writing complex SQL queries for business analysis.
2. Using CTEs to organise complex analytical queries.
3. Applying window functions for cumulative and comparative analysis.
4. Performing customer and product segmentation.
5. Calculating important business KPIs.
6. Creating SQL views for analytical reporting.
7. Translating business questions into SQL-based solutions.

## 👨‍💻 Author

**Vishal Shankar Jadhav**

Aspiring Data Analyst | SQL | Python | Power BI | Tableau | Machine Learning

---

⭐ If you find this project useful, feel free to explore the SQL scripts and share your feedback!
