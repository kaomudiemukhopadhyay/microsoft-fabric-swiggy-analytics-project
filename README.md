# 🚀 Swiggy End-to-End Data Analytics Project using Microsoft Fabric

## 📌 Business Problem

Swiggy generates massive amounts of operational data including orders, restaurants, ratings, dishes, and customer interactions.

The objective of this project is to build a scalable end-to-end analytics solution using Microsoft Fabric to:

- Store raw datasets
- Process and optimize data
- Build analytical models
- Generate business insights
- Create interactive dashboards

---

# 🔥 Key Highlights

- Built an end-to-end analytics pipeline using Microsoft Fabric
- Implemented Delta Lake architecture
- Designed Star Schema data model
- Automated data movement using Fabric Pipelines
- Performed SQL-based business analytics
- Created Power BI dashboards for business insights

---

# 🏗️ Solution Architecture

```text
CSV Files
   ↓
Lakehouse
   ↓
Delta Tables
   ↓
OneLake
   ↓
Pipeline
   ↓
Warehouse
   ↓
Semantic Model
   ↓
SQL Analytics
   ↓
Power BI Dashboard
```

---

# ⚙️ Technology Stack

| Layer | Technology |
|---|---|
| Data Storage | Microsoft Fabric Lakehouse |
| Storage Format | Delta Lake |
| Storage Layer | OneLake |
| ETL | Fabric Pipelines |
| Data Warehouse | Microsoft Fabric Warehouse |
| Semantic Layer | Power BI Semantic Model |
| Query Language | SQL |
| Visualization | Power BI |

---

# 📂 Dataset Used

The project uses Swiggy food delivery datasets containing:

- Orders
- Restaurants
- Ratings
- Dishes
- Locations

## Dataset Files

- dim_date.csv
- dim_dish.csv
- dim_location.csv
- dim_restaurant.csv
- fact_orders.csv

---

# 🟢 Project Workflow

## 1️⃣ Data Ingestion

- Uploaded raw CSV datasets into Microsoft Fabric Lakehouse
- Centralized data storage for scalable analytics

---

## 2️⃣ Delta Table Conversion

- Converted CSV files into Delta tables
- Generated parquet files and transaction logs internally

### Benefits

- Optimized Storage
- Faster Query Performance
- ACID Transactions
- Scalable Analytics

---

## 3️⃣ OneLake Integration

Used OneLake as the centralized storage layer across Fabric services.

### Benefits

- Unified Storage Architecture
- Shared Access Across Services
- Reduced Data Duplication
- Improved Scalability

---

## 4️⃣ Pipeline Development

Created Fabric Data Pipelines to automate data movement.

### Pipeline Flow

```text
Lakehouse → OneLake → Warehouse
```

### Activity Used

- Copy Data Activity

---

## 5️⃣ Data Warehouse Modeling

Implemented Star Schema architecture inside Microsoft Fabric Warehouse.

### Schema Created

```text
swiggy_project
```

### Dimension Tables

- dim_date
- dim_dish
- dim_location
- dim_restaurant

### Fact Table

- fact_orders

### Benefits of Star Schema

- Faster Query Performance
- Better Reporting Structure
- Improved Analytical Efficiency

---

## 6️⃣ Semantic Model

Created a Power BI Semantic Model on top of the Warehouse for business reporting and dashboard integration.

### Purpose

- Centralized business metrics
- Data relationships
- KPI calculations
- Power BI integration

---

## 7️⃣ SQL Analytics

Performed SQL analysis using joins, aggregations, and KPI calculations.

### SQL Operations Used

- SELECT
- JOIN
- COUNT
- SUM
- AVG
- GROUP BY

### Data Validation Performed

- Checked missing values
- Removed duplicate records
- Validated order amounts
- Verified referential integrity
- Standardized data formats

---

## 8️⃣ Power BI Dashboard Development

Built interactive Power BI dashboards for business reporting and insights.

### Dashboard Features

- KPI Cards
- Revenue Analysis
- Restaurant Performance
- Order Trends
- Rating Analysis

---

# 📊 Business KPIs

The following KPIs were generated:

- Total Revenue
- Total Orders
- Average Order Value
- Average Rating
- Rating Count

---

# 📈 Dashboard Insights

- Top Performing Restaurants
- Revenue Trends
- Customer Ordering Patterns
- Rating Distribution
- Order Volume Analysis

---

# 🧪 Sample SQL Query

SELECT * from swiggy_project.dim_date
SELECT count(*) from swiggy_project.dim_date

SELECT * from swiggy_project.dim_dish
SELECT count(*) from swiggy_project.dim_dish

SELECT * from swiggy_project.dim_location
SELECT count(*) from swiggy_project.dim_location

SELECT * from swiggy_project.dim_restaurant
SELECT count(*) from swiggy_project.dim_restaurant

SELECT * from swiggy_project.fact_orders
SELECT COUNT(*) from swiggy_project.fact_orders

ALTER TABLE swiggy_project.dim_date
add order_date_new DATE

UPDATE swiggy_project.dim_date
SET order_date_new = TRY_CONVERT(date,order_date,5)

select * from swiggy_project.dim_date
WHERE order_date_new is null
```

# 🧠 Important Concepts Implemented

## Lakehouse

Used for scalable storage and processing of structured and semi-structured data using Delta Lake format.

---

## Delta Lake

Provided:

- ACID Transactions
- Optimized Storage
- Reliability
- Faster Queries

---

## OneLake

Centralized storage layer across Microsoft Fabric workloads.

---

## Warehouse

Used for reporting-ready structured analytics and SQL querying.

---

# 🔄 End-to-End Data Flow

```text
CSV Files
   ↓
Fabric Lakehouse
   ↓
Delta Tables
   ↓
OneLake
   ↓
Fabric Pipeline
   ↓
Fabric Warehouse
   ↓
Semantic Model
   ↓
SQL Analytics
   ↓
Power BI Dashboard
```

---

# 📸 Project Screenshots

## Fabric Workspace Overview

Complete Microsoft Fabric workspace containing Lakehouse, Pipelines, Warehouse, Semantic Model, and Power BI assets.

<img width="1827" height="830" alt="image" src="https://github.com/user-attachments/assets/3daa9c3a-0484-4d20-9004-c0b9a256cdbc" />

---

## Lakehouse Tables

Raw CSV datasets converted into Delta tables inside Fabric Lakehouse.

<img width="1803" height="907" alt="image" src="https://github.com/user-attachments/assets/a61fff5b-e7b6-4a79-a35a-705ea279c31e" />

---

## Delta Tables

Delta table structure showing parquet files and transaction logs (_delta_log).

<img width="1842" height="942" alt="image" src="https://github.com/user-attachments/assets/bdc0adae-4f5a-4520-9ab5-21a299f08d47" />

---

## Pipeline

Fabric pipeline used for automated data movement from Lakehouse to Warehouse.

<img width="1800" height="912" alt="image" src="https://github.com/user-attachments/assets/2f9e7335-62df-4ff3-b5b9-490f364973c9" />

---

## Warehouse

Structured analytical warehouse implementing Star Schema architecture.

<img width="1847" height="861" alt="image" src="https://github.com/user-attachments/assets/3eed16de-d7b2-413d-8296-593a6fb988bb" />

---

## SQL Analytics

SQL queries used for KPI generation and business analysis.

<img width="1755" height="713" alt="image" src="https://github.com/user-attachments/assets/099bfe23-0a81-4e1c-a2e6-7d70942fe9e1" />

---

## Power BI Dashboard

Interactive Power BI dashboard for business insights and KPI visualization.

<img width="1428" height="868" alt="image" src="https://github.com/user-attachments/assets/308fe5ae-e0f0-41f2-b136-2173a4fb9c68" />

---

# 📁 Repository Structure

```text
📦 Swiggy-Fabric-Analytics-Project
 ┣ 📂 datasets
 ┣ 📂 screenshots
 ┣ 📂 sql_queries
 ┣ 📂 powerbi
 ┣ 📂 architecture_diagram
 ┣ 📜 README.md
```

---

# 🚀 Future Improvements

- Implement Medallion Architecture
- Incremental Data Loading
- Real-Time Streaming Analytics
- Advanced Power BI Dashboards
- Machine Learning Integration
- Data Validation Pipelines

---

# 🎯 Key Learnings

- Microsoft Fabric Architecture
- Lakehouse vs Warehouse
- Delta Lake Concepts
- OneLake Storage
- Data Pipelines
- SQL Analytics
- Star Schema Modeling
- Power BI Dashboarding
- ACID Transactions

---

# ✅ Project Outcome

Successfully built a modern end-to-end analytics solution using Microsoft Fabric integrating:

- Lakehouse
- Delta Tables
- OneLake
- Fabric Pipelines
- Data Warehouse
- Semantic Model
- SQL Analytics
- Power BI

The project demonstrates scalable cloud-based analytics architecture and business intelligence implementation.

---

# 🧠 Conclusion

This project demonstrates how Microsoft Fabric can be used as a unified analytics platform for data ingestion, storage, transformation, warehousing, SQL analytics, and visualization.

The solution provides scalable, optimized, and reliable analytics architecture using Delta Lake and OneLake within the Microsoft Fabric ecosystem.

---

# 📌 GitHub Topics

```text
microsoft-fabric
power-bi
sql
data-engineering
data-analytics
lakehouse
datawarehouse
delta-lake
onelake
business-intelligence
fabric-pipeline
```
