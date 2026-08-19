# Swiggy-Sales-Analysis
# 🍔 Swiggy Sales Analysis

## 📌 Project Overview

This project focuses on analyzing Swiggy food delivery data to identify key business insights related to orders, revenue, restaurants, food categories, dishes, locations, customer spending, and ratings.

The project includes **data cleaning, validation, dimensional modelling using a Star Schema, SQL analysis, and KPI development** to create a reliable foundation for business reporting and decision-making.

## 🎯 Business Objectives

* Analyze overall order and revenue performance
* Identify top-performing cities and states
* Analyze restaurant and category performance
* Identify the most ordered dishes
* Understand customer spending patterns
* Analyze dish rating distribution
* Identify monthly, quarterly, and yearly order trends
* Build a structured data model for efficient analytics

## 🛠️ Tools & Technologies

* **SQL Server**
* **SQL**
* **GitHub**
* **Data Cleaning & Validation**
* **Dimensional Modelling**
* **Star Schema**

## 🧹 Data Cleaning & Validation

The raw `swiggy_data` table contains food delivery records across states, cities, restaurants, categories, and dishes.

The following data-quality checks were performed:

* Null value identification
* Blank/empty string detection
* Duplicate row detection
* Duplicate removal using `ROW_NUMBER()`
* Validation of business-critical columns

### Business-Critical Columns

* State
* City
* Order_Date
* Restaurant_Name
* Location
* Category
* Dish_Name
* Price_INR
* Rating
* Rating_Count

## ⭐ Data Modelling – Star Schema

A Star Schema was created to organize the data efficiently for analytical queries and reporting.

### Dimension Tables

| Table            | Description                |
| ---------------- | -------------------------- |
| `dim_date`       | Year, Month, Quarter, Week |
| `dim_location`   | State, City, Location      |
| `dim_restaurant` | Restaurant Name            |
| `dim_category`   | Cuisine / Category         |
| `dim_dish`       | Dish Name                  |

### Fact Table

`fact_swiggy_orders`

Contains:

* Price_INR
* Rating
* Rating_Count
* Foreign keys connected to the dimension tables

## 📊 Key KPIs

The project calculates the following core KPIs:

* **Total Orders**
* **Total Revenue (INR Million)**
* **Average Dish Price**
* **Average Rating**

## 🔍 Business Analysis

### 📅 Date-Based Analysis

* Monthly order trends
* Quarterly order trends
* Year-wise growth
* Day-of-week order patterns

### 📍 Location Analysis

* Top 10 cities by order volume
* Revenue contribution by state

### 🍽️ Food Performance

* Top 10 restaurants by orders
* Top food categories
* Most ordered dishes
* Cuisine performance based on orders and average rating

### 💰 Customer Spending Analysis

Orders are categorized into spending buckets:

* Under ₹100
* ₹100–₹199
* ₹200–₹299
* ₹300–₹499
* ₹500+

The distribution of orders across these spending ranges is analyzed to understand customer spending behavior.

### ⭐ Ratings Analysis

Dish ratings are analyzed across the **1–5 rating scale** to understand rating distribution and food quality patterns.

## 📁 Project Structure

```text
Swiggy-Sales-Analysis/
│
├── README.md
├── Business Requirements/
│   └── Business Requirements.docx
│
├── SQL/
│   ├── Data Cleaning.sql
│   ├── Star Schema.sql
│   ├── KPI Analysis.sql
│   └── Business Analysis.sql
│
└── ERD/
    └── Star Schema ERD.png
```

## 💡 Key Learning Outcomes

Through this project, I practiced:

* SQL data cleaning
* Duplicate detection and removal
* Data validation
* Database normalization concepts
* Star Schema design
* Fact and dimension table creation
* KPI development
* Business-oriented SQL analysis
* Converting raw data into actionable business insights

## 👨‍💻 Author

**Danish Alam**

MBA – Business Analytics & Data Analytics
