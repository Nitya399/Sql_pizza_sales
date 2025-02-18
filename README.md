SQL Pizza Sales Analysis

Project Description

This project analyzes pizza sales data using SQL to derive insights into sales trends, customer preferences, and business performance. The dataset contains order details, pizza categories, and revenue data, and the analysis aims to optimize decision-making for better business outcomes.

Problem Statement

The goal of this project is to answer key business questions using SQL queries, such as:

What are the total sales revenue and order count?

Which pizza size and category generate the most revenue?

What are the top-selling and least-selling pizzas?

How does sales performance vary across different days and months?

What is the average order value, and how can pricing strategies be optimized?

Key SQL Queries & Insights

1️⃣ Total Sales Revenue and Order Count

SELECT COUNT(DISTINCT order_id) AS total_orders,
       SUM(total_price) AS total_revenue
FROM orders;

📌 Insight: The total revenue and order count provide a high-level overview of business performance.

2️⃣ Best-Selling Pizza Categories

SELECT category, SUM(quantity) AS total_quantity_sold
FROM pizzas
GROUP BY category
ORDER BY total_quantity_sold DESC;

📌 Insight: Identifying the best-performing categories helps in stock and marketing strategies.

3️⃣ Top 5 Best-Selling Pizzas

SELECT pizza_name, SUM(quantity) AS total_sold
FROM order_details
GROUP BY pizza_name
ORDER BY total_sold DESC
LIMIT 5;

📌 Insight: Knowing the top-sellers can help prioritize menu items and promotions.

4️⃣ Average Order Value (AOV)

SELECT AVG(total_price) AS average_order_value
FROM orders;

📌 Insight: The AOV helps in pricing strategies and discount planning.

5️⃣ Sales Performance by Month

SELECT MONTH(order_date) AS month, SUM(total_price) AS monthly_sales
FROM orders
GROUP BY MONTH(order_date)
ORDER BY month;

📌 Insight: Understanding seasonal trends can optimize marketing efforts.

Conclusions & Learnings

The most popular pizza categories drive a significant portion of sales, suggesting targeted marketing efforts for them.

Peak sales periods were identified, indicating when to run promotions or increase staff availability.

The Average Order Value (AOV) provides insights into customer spending behavior.

Least-selling pizzas might need adjustments in pricing or menu offerings.
