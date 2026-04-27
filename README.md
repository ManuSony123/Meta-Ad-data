# Meta-Ad-data
Meta Ad data sales PowerBI dasahboard
# 🛍️ Retail Sales Analytics – End-to-End Data Analyst Project

## 📌 Project Overview

This project focuses on building a complete data analytics solution for a retail business to analyze sales performance, customer behavior, and product trends.

The solution includes data cleaning, transformation, data modeling (star schema), advanced SQL analysis, and an interactive Power BI dashboard to deliver actionable business insights.

---

## 🎯 Business Problem

Retail businesses often struggle with:

* Lack of visibility into sales trends
* Identifying high-value customers
* Understanding product performance
* Regional sales inconsistencies

This project aims to solve these challenges by building a structured analytics system.

---

## 🏗️ Architecture

Raw Data (CSV)
→ Staging Layer (SQL Tables)
→ Data Cleaning & Transformation
→ Data Warehouse (Star Schema)
→ Power BI Dashboard

Meta_Ad.pbix
├── DataModel              ← Compressed data model (tables, measures, relationships)
├── Report/
│   ├── Layout             ← All page layouts and visual configurations
│   ├── LinguisticSchema   ← Q&A natural language schema
│   └── StaticResources/
│       ├── SharedResources/
│       │   └── BaseThemes/CY24SU10.json   ← Power BI theme file
│       └── RegisteredResources/
│           ├── Meta logos (PNG)
│           ├── Facebook logo (PNG)
│           ├── Instagram icon (PNG)
│           ├── WhatsApp icon (PNG)
│           └── Threads icon (PNG)
├── Settings               ← Report-level settings
├── Metadata               ← Report metadata
└── Version                ← Power BI format version
---

## 🧱 Data Model

### ⭐ Fact Table

* Fact_Sales

  * Sales Amount
  * Quantity
  * Unit Price

### 📦 Dimension Tables

* Dim_Customer (Customer ID, Country)
* Dim_Product (Stock Code, Description)
* Dim_Date (Date, Month, Year)

---

## ⚙️ ETL Process

* Loaded raw retail dataset into staging tables
* Performed data cleaning:

  * Removed null customer records
  * Removed negative quantities (returns)
  * Filtered invalid pricing
* Transformed data:

  * Created derived columns (Total Sales = Quantity × Price)
* Built star schema model
* Loaded fact and dimension tables using SQL joins

---

## 🔍 SQL Analysis

Performed advanced SQL analysis including:

* Customer spending analysis
* Monthly revenue trends
* Product performance ranking
* Repeat vs new customer identification

### Example:

```sql
SELECT 
    customer_id,
    SUM(total_sales) AS total_spent
FROM fact_sales
GROUP BY customer_id
ORDER BY total_spent DESC;
```

---

## 📊 Power BI Dashboard

The dashboard provides:

### 🔹 Executive Overview

* Total Sales
* Total Profit
* Total Orders

### 🔹 Customer Insights

* Top customers
* Customer segmentation
* Repeat vs new customers

### 🔹 Product Analysis

* Top-selling products
* Low-performing products

### 🔹 Regional Analysis

* Sales by country
* Profit distribution

---

## 💡 Key Insights

* A small percentage of customers contribute to the majority of revenue
* Certain products generate high sales but low profit
* Sales show seasonal trends across months
* Some regions underperform compared to others

---

## 🧰 Tools & Technologies

* SQL (MySQL / Oracle)
* Power BI
* Excel
* Python (optional ETL support)

---

## 🚀 Key Skills Demonstrated

* Data Cleaning & Transformation
* Data Modeling (Star Schema)
* ETL Pipeline Design
* Advanced SQL (Aggregations, Joins)
* Business Analysis
* Data Visualization

---

## 🧑‍💼 Author

**Manohar Marepally**
Data Analyst | ETL Developer
📧 [marepallymanohar@gmail.com](mailto:marepallymanohar@gmail.com)
🔗 LinkedIn: https://linkedin.com/in/manohar-marepally

---

## 📌 Future Enhancements

* Implement Slowly Changing Dimensions (SCD Type 2)
* Add customer segmentation using advanced analytics
* Automate ETL pipeline using Python

---
