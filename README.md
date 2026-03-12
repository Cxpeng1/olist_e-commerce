# Olist Marketplace Data Analysis

FLOW: RAW sqlite files -> db browser -> queries -> powerbi -> Dashboard -> Summary

## Business Questions

- Which states generate the most orders?

- Which cities have the highest number of customers?

- Are customers concentrated in specific regions?

- Which product categories are most popular?

- Which categories generate the highest order volume?

- Are certain categories associated with lower review scores?

- Which products may have quality issues based on customer reviews?

- How accurate are delivery time estimates?

- Are deliveries becoming faster or slower over time?

- Which orders take longer than the average monthly delivery time?

- Does delivery performance affect customer review scores?

## 1. Data Collection

The dataset used in this project is the **Olist E-commerce Dataset**, obtained from Kaggle. It contains all real transactional data from a Brazilian e-commerce marketplace.

The dataset consists of several related tables:

- `orders`
- `customers`
- `order_items`
- `products`
- `order_payments`
- `order_reviews`
- `sellers`

These tables represent the full lifecycle of an order, from purchase to delivery and customer feedback.

---

## 2. Data Storage

The raw CSV files were imported into a SQLite database using **DB Browser for SQLite**. Storing the data in a relational database allows efficient querying and analysis using SQL.

---

## 3. Exploratory Data Analysis (EDA)

### Descriptive Analysis

- Examined the structure of the Olist dataset by reviewing key tables such as `orders`, `customers`, `order_items`, `products`, and `order_payments`.
- Checked dataset size and identified the time range of orders using `order_purchase_timestamp`.
- Analyzed the distribution of `order_status` to understand the proportion of delivered, cancelled, and processing orders.
- Explored customer geographic distribution by analyzing `customer_state` and `customer_city`.
- Identified the most frequently purchased product categories.

### Visual Analysis

- Analyzed monthly order trends to observe marketplace growth over time.
- Examined the distribution of customers across different Brazilian states.
- Identified top-selling product categories based on order frequency.
- Analyzed review score distribution to understand customer satisfaction patterns.

### Statistical Analysis

- Calculated the difference between `estimated delivery date` and `actual delivery date` to measure delivery accuracy.
- Computed the average delivery difference by month to evaluate logistics performance.
- Identified orders where delivery time was worse than the monthly average to detect potential delivery delays.

---
