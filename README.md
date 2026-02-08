# PL/SQL Window Functions Assignment – INSY 8311

**Student:** Yves Shapu  
**Student ID:** 27844  
**Course:** Database Development with PL/SQL (INSY 8311)  
**Instructor:** Eric Maniraguha  
**Submission Date:** February 2026

## Business Problem Definition

**Business Context:**  
TechMart – a mid-sized electronics retail chain operating in multiple regions, sales department, consumer electronics industry.

**Data Challenge:**  
The company struggles with uneven sales performance across products and regions, inconsistent customer loyalty, and difficulty identifying underperforming items and inactive customers.  
This makes inventory planning, targeted promotions, and customer retention strategies inefficient.

**Expected Outcome:**  
Obtain clear insights to prioritize high-value customers, optimize stock levels, and design region/product-specific marketing actions.

## Success Criteria (5 measurable goals using window functions)

1. Identify top 5 customers by total revenue → `RANK()`
2. Calculate running (cumulative) monthly sales totals → `SUM() OVER()`
3. Compute month-over-month sales growth percentage → `LAG()`
4. Segment customers into 4 quartiles based on revenue → `NTILE(4)`
5. Calculate three-month moving average of sales → `AVG() OVER()`

## Database Schema

### Tables
- `customers` (customer_id PK, name, region)
- `products` (product_id PK, name, category, price)
- `sales` (sale_id PK, customer_id FK, product_id FK, sale_date, quantity, total_amount)

### ER Diagram (text representation)
![image alt](https://github.com/RwabukumbaYvesShapu/plsql_window_functions_27844_Yves/blob/298a391ee5f44cf538dc441c42c440a28985fa7c/er-digram.png)
