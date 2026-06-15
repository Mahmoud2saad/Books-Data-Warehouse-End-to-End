# 📚 Books Data Warehouse | End-to-End Business Intelligence Solution

## Overview

Gravity Books Data Warehouse is an end-to-end Data Engineering and Business Intelligence project that transforms transactional bookstore data into a centralized analytical platform for reporting and decision-making.

The solution follows modern Data Warehouse principles by integrating data modeling, ETL development, dimensional design, OLAP analytics, and interactive dashboards into a single enterprise-ready architecture.

The project was developed using Microsoft SQL Server, SSIS, SSAS, and Power BI.

---

## Business Problem

Operational databases are optimized for transaction processing but are not designed for analytical workloads.

As data volume grows, business users face challenges such as:

* Slow reporting performance
* Limited historical analysis
* Data redundancy across reports
* Lack of centralized KPIs
* Difficulty analyzing sales trends and customer behavior

This project addresses these challenges by implementing a dimensional Data Warehouse optimized for analytics and business intelligence.

---

## Solution Architecture

```text
OLTP Source Database
          │
          ▼
     STAGING LAYER
          │
          ▼
      SSIS ETL
          │
          ▼
   DATA WAREHOUSE
          │
          ▼
       SSAS Cube
          │
          ▼
   Power BI Dashboard
```

---

## Data Warehouse Architecture

The warehouse is designed using a Snowflake Schema to support scalable analytics while maintaining data integrity and reducing redundancy.

### Fact Table

* Fact_Sales

### Dimension Tables

* Dim_Books
* Dim_Author
* Dim_Customer
* Dim_Address
* Dim_Order_History
* Dim_Shipping_Method

### Bridge Table

* Bridge_Book_Author

---

## Data Modeling

### Source ERD

The source system contains normalized transactional entities related to:

* Books
* Authors
* Customers
* Orders
* Shipping
* Addresses

### Dimensional Model

The Data Warehouse redesigns the source system into an analytical schema optimized for reporting and OLAP operations.

---

## ETL Pipeline (SSIS)

SQL Server Integration Services (SSIS) is used to build the ETL workflow.

### Extraction

Data is extracted from the operational database.

### Transformation

Transformations include:

* Data cleansing
* Data validation
* Surrogate key generation
* Data type standardization
* Lookup transformations
* Business rule implementation

### Loading

Processed data is loaded into:

* Dimension Tables
* Fact Table
* Bridge Table

while maintaining referential integrity.

---

## SSIS Packages

The ETL solution consists of dedicated packages for each business entity:

| Package                  | Purpose                        |
| ------------------------ | ------------------------------ |
| STG.dtsx                 | Populate staging layer         |
| books_dim.dtsx           | Load Book Dimension            |
| author_dim.dtsx          | Load Author Dimension          |
| customer_dim.dtsx        | Load Customer Dimension        |
| address_dim.dtsx         | Load Address Dimension         |
| order_history_dim.dtsx   | Load Order History Dimension   |
| shipping_method_dim.dtsx | Load Shipping Method Dimension |
| book_author_bridge.dtsx  | Load Bridge Table              |
| sales_fact.dtsx          | Load Fact Sales                |

---

## Analytical Layer (SSAS)

SQL Server Analysis Services (SSAS) provides an analytical semantic model that enables:

* Fast aggregations
* KPI calculations
* Drill-down analysis
* Slice and Dice operations
* Multidimensional reporting

The model serves as the analytical engine for business intelligence reporting.

---

## Dashboard & Reporting

Power BI dashboards provide insights into:

### Sales Analysis

* Revenue Trends
* Order Volume
* Sales Performance

### Customer Analysis

* Customer Purchasing Behavior
* Top Customers
* Customer Growth

### Product Analysis

* Best Selling Books
* Author Performance
* Product Distribution

### Operational Analysis

* Shipping Performance
* Order Fulfillment Trends

---

## Technologies Used

| Category        | Technology                             |
| --------------- | -------------------------------------- |
| Database        | SQL Server                             |
| Data Warehouse  | SQL Server Data Warehouse              |
| ETL             | SQL Server Integration Services (SSIS) |
| Analytics       | SQL Server Analysis Services (SSAS)    |
| Reporting       | Power BI                               |
| Query Language  | T-SQL                                  |
| Data Modeling   | Snowflake Schema                       |
| Development     | Visual Studio / SSDT                   |
| Version Control | Git & GitHub                           |

---

## Repository Structure

```text
├── Data_Modeling
│   ├── ERD.png
│   └── SCHEMA.png
│
├── SQL Scripts
│
├── SSIS_Packages
│   └── books_DWH
│       ├── STG.dtsx
│       ├── books_dim.dtsx
│       ├── author_dim.dtsx
│       ├── customer_dim.dtsx
│       ├── address_dim.dtsx
│       ├── order_history_dim.dtsx
│       ├── shipping_method_dim.dtsx
│       ├── book_author_bridge.dtsx
│       └── sales_fact.dtsx
│
├── SSAS
│   └── gravity_books_measures
│
└── PowerBI
    ├── Gravity_books.pbix
    └── Dashboard.png
```

---

## Key Data Engineering Concepts Demonstrated

* Data Warehouse Design
* Dimensional Modeling
* Snowflake Schema
* ETL Development
* Staging Layer Architecture
* Fact & Dimension Modeling
* Bridge Tables
* Data Integration
* OLAP Analytics
* Semantic Modeling
* BI Reporting

---

## Future Enhancements

* Incremental Loading
* Change Data Capture (CDC)
* Slowly Changing Dimensions (SCD)
* Data Quality Framework
* Automated Deployment Pipeline
* Cloud Migration (Azure Data Factory / Fabric)

---

## Author

Mahmoud Saad

Computer Science Graduate | Data Engineer | Data Scientist | Kaggle Expert

Passionate about building scalable Data Engineering and Business Intelligence solutions that transform raw data into actionable insights.
