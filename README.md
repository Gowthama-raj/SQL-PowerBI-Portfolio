# SQL-PowerBI-Portfolio
This repository contains my SQL + Power BI portfolio projects. It includes database schemas, SQL queries, datasets, and interactive dashboards. Each project focuses on solving real-world business problems such as sales analysis, banking transactions, customer churn, and stock market trends.
# E-commerce Sales Analysis (SQL + Power BI)

## 📌 Objective
Analyze sales data to understand revenue trends, top-selling products, and customer retention.

---

## 🗂️ Dataset
- **customers.csv** → Customer details (ID, name, region, join date)
- **products.csv** → Product catalog (ID, name, category, price)
- **orders.csv** → Order summary (order_id, customer_id, date, total)
- **order_items.csv** → Order details (line items, quantity, amount)

---

## ⚙️ Implementation
1. Created database schema in PostgreSQL.
2. Imported CSV files into SQL tables.
3. Wrote analytical queries (see `queries.sql`).
4. Connected SQL to Power BI.
5. Designed interactive dashboard.

---

## 📊 Key Queries
- **Monthly Revenue**
```sql
SELECT DATE_TRUNC('month', order_date) AS month,
       SUM(total_amount) AS monthly_revenue
FROM orders
GROUP BY month
ORDER BY month;
