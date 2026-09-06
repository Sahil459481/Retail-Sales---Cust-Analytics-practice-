# Retail Sales & Customer Analytics 🛒

## Project Overview
This project simulates a real-world scenario for an emerging direct-to-consumer (D2C) clothing retailer. The goal was to transform raw transactional data into actionable business intelligence for the Marketing, Inventory, and Finance teams. 

**Database System:** Oracle SQL

## Business Problems Solved
In this project, I answered five critical business questions using SQL:

1. **CRM Audit (Data Cleaning):** Identified users missing email addresses using `IS NULL` so the support team can follow up.
2. **Reporting Layer Cleanliness:** Sanitized the customer directory for BI dashboards by substituting missing data with readable text using `COALESCE()`.
3. **Merchandising Performance:** Ranked product categories by total revenue using `INNER JOIN`, `SUM()`, and `GROUP BY` to inform inventory restocking.
4. **Financial Trend Analysis:** Calculated validated monthly recurring revenue (excluding cancelled orders) using the `TRUNC()` date function.
5. **Order Segmentation:** Segmented orders into 'High Value' and 'Standard' tiers for logistics packaging using Common Table Expressions (`WITH`) and `CASE WHEN` logic.

## Schema Design
The database consists of four normalized tables:
* **customers:** Stores user profiles and registration dates.
* **products:** Contains catalog items, categories, and pricing.
* **orders:** Header table tracking transaction dates and fulfillment status.
* **order_items:** Line-item table bridging orders and products, tracking quantity and historical unit prices.

## Core SQL Skills Demonstrated
* Data Definition Language (DDL) with Oracle `IDENTITY` columns.
* Data Manipulation Language (DML).
* Advanced filtering and NULL handling.
* Aggregations and Date Truncation.
* Common Table Expressions (CTEs) and Conditional Logic (`CASE WHEN`).

## How to Run
1. Execute `01_database_setup.sql` in Oracle SQL Developer or Oracle APEX to create the schema and populate the sample data.
2. Run `02_business_queries.sql` to generate the analytical reports.
