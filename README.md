# ecommerce-customer-churn-sql-analysis
E-Commerce Customer Churn Analysis using MySQL

# E-Commerce Customer Churn Analysis Using MySQL

## 📌 Project Overview

This project analyzes customer churn in an e-commerce business using MySQL.

The objective is to identify customer churn patterns and understand customer behavior based on tenure, payment methods, order categories, complaints, satisfaction scores, coupon usage, order count, and other customer attributes.

---

## 🛠️ Tools Used

- MySQL
- MySQL Workbench
- SQL

---

## 📊 Dataset

The dataset contains customer-level information including:

- Customer ID
- Churn
- Tenure
- Preferred Login Device
- City Tier
- Warehouse to Home Distance
- Preferred Payment Mode
- Gender
- Hours Spent on App
- Number of Devices Registered
- Preferred Order Category
- Satisfaction Score
- Marital Status
- Number of Addresses
- Complaints
- Order Amount Hike
- Coupon Used
- Order Count
- Days Since Last Order
- Cashback Amount

---

## 🧹 Data Cleaning

The following data-cleaning operations were performed:

- Handled missing values using mean imputation
- Handled categorical missing values using mode imputation
- Removed rows where WarehouseToHome was greater than 100
- Standardized login device values
- Standardized order category values
- Standardized payment mode values

---

## 🔄 Data Transformation

The following transformations were performed:

- Renamed `PreferedOrderCat` to `PreferredOrderCat`
- Renamed `HourSpendOnApp` to `HoursSpentOnApp`
- Created `ComplaintReceived`
- Created `ChurnStatus`
- Removed the original `Churn` and `Complain` columns

---

## 🔍 SQL Analysis

The project includes analysis of:

1. Churned and active customers
2. Average tenure of churned customers
3. Total cashback received by churned customers
4. Customer complaints
5. City tier analysis
6. Preferred payment modes
7. Order category analysis
8. Coupon usage
9. Satisfaction scores
10. Warehouse-to-home distance
11. Customer order behavior
12. Customer returns
13. Customer return and churn analysis using JOINs

---

## 📈 Key Results

- Total customers after cleaning: **5,628**
- Churned customers: **948**
- Active customers: **4,680**
- Churned customers who complained: **53%**
- City Tier 3 had the highest number of churned Laptop & Accessory customers
- Debit Card was the most preferred payment mode among active customers
- Far Distance had the highest number of churned customers
- Laptop & Accessory was the most common order category among customers using more than 5 coupons

---

## 💡 SQL Concepts Used

- SELECT
- WHERE
- GROUP BY
- HAVING
- ORDER BY
- LIMIT
- Aggregate Functions
- CASE
- Subqueries
- JOIN
- CREATE TABLE
- INSERT
- UPDATE
- DELETE
- Data Cleaning
- Data Transformation

---

## 📦 Customer Returns Analysis

A separate `customer_returns` table was created containing:

- Return ID
- Customer ID
- Return Date
- Refund Amount

The return data was joined with customer information to identify customers who:

- Made a return
- Were churned
- Had received complaints

---

## ⚠️ Data Note

For one analysis question, the project required customers with an OrderCount greater than 500 and an average tenure of 10 months.

No matching customers were found in the dataset because the available OrderCount values did not contain customers with more than 500 orders.

No value was invented for this analysis.

---

## 🎯 Project Objective

This project demonstrates practical SQL skills for cleaning, transforming, analyzing, and extracting business insights from e-commerce customer data.
