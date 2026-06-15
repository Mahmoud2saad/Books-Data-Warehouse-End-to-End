# 📚 Books Data Warehouse | End-to-End BI Solution

## 📖 Project Description

Gravity Books Data Warehouse is an end-to-end Business Intelligence solution designed to transform operational bookstore data into meaningful business insights.

The project demonstrates the complete Data Engineering and Business Intelligence lifecycle, including Data Warehouse modeling, ETL development, OLAP cube creation, and interactive dashboard reporting.

The solution extracts transactional data from a SQL Server OLTP database, processes it through SSIS ETL pipelines, stores it in a dimensional Data Warehouse, exposes analytical models through SSAS, and delivers actionable insights using Power BI dashboards.

---

# 🎯 Business Problem

Bookstore transactional databases are optimized for daily operations but are not suitable for analytical reporting.

This project addresses the following challenges:

- Lack of centralized reporting
- Slow analytical queries on transactional systems
- Difficulty tracking historical business changes
- Limited visibility into customer and sales performance
- Absence of decision-support analytics

The Data Warehouse provides a scalable and efficient platform for business reporting and strategic decision-making.

---

# 🏗️ Solution Architecture

```text
Source Database (OLTP)
          │
          ▼
    SSIS ETL Layer
          │
          ▼
 Data Warehouse (Snowflake Schema)
          │
          ▼
      SSAS Cube
          │
          ▼
   Power BI Dashboard
```

---

# 📊 Data Warehouse Design

The warehouse is designed using a Snowflake Schema to support analytical workloads while minimizing redundancy.

### Dimension Tables

- Dim Book
- Dim Author
- Dim Customer
- Dim Address
- Dim Date
- Dim Shipping Method
- Dim Order History

### Fact Tables

- Fact Sales

### Bridge Tables

- Book Author Bridge

---

# ⚙️ ETL Process

The ETL pipelines were developed using SQL Server Integration Services (SSIS).

### Extract
- Retrieve data from the Gravity Books OLTP database.

### Transform
- Data cleansing
- Data validation
- Surrogate key generation
- Business rule implementation
- Historical data processing

### Load
- Populate dimension tables
- Load fact tables
- Maintain referential integrity

---

# 🕒 Slowly Changing Dimensions (SCD)

The project implements Slowly Changing Dimensions (SCD) to preserve historical changes and support time-based analysis.

Benefits include:

- Historical customer tracking
- Address change management
- Business trend analysis over time
- Improved auditability

---

# 📈 OLAP & Analytics

SQL Server Analysis Services (SSAS) was used to create a multidimensional analytical model.

Features include:

- Aggregations
- Drill-down analysis
- Slice and Dice operations
- Fast query performance
- KPI calculations

---

# 📉 Power BI Reporting

The Power BI dashboard enables stakeholders to analyze:

- Sales Performance
- Revenue Trends
- Customer Behavior
- Best-Selling Books
- Shipping Analysis
- Order Trends
- Business KPIs

---

# 🛠️ Tools & Technologies

| Category | Technology |
|-----------|------------|
| Database | Microsoft SQL Server |
| Data Warehouse | SQL Server Data Warehouse |
| ETL | SQL Server Integration Services (SSIS) |
| OLAP | SQL Server Analysis Services (SSAS) |
| Reporting | Power BI |
| Data Modeling | Snowflake Schema |
| Query Language | T-SQL |
| Version Control | Git & GitHub |
| Development Environment | SQL Server Data Tools (SSDT) |
| Data Integration | Visual Studio |

---

# 📂 Repository Structure

```text
├── Documentation
│   ├── ERD-Source.jpg
│   └── DWH-Modelling.jpg
│
├── SSIS_Packages
│   └── ETL Packages
│
├── SSAS
│   └── Cube & Dimensions
│
├── PowerBI
│   └── Dashboard Reports
│
└── Source Database Scripts
```

---

# 🚀 Key Features

✅ End-to-End BI Solution

✅ Data Warehouse Implementation

✅ Snowflake Schema Design

✅ SSIS ETL Pipelines

✅ Slowly Changing Dimensions (SCD)

✅ SSAS Multidimensional Cube

✅ Power BI Dashboard Development

✅ Business KPI Analysis

---

# 📷 Project Documentation

### Source System ERD

![ERD](Documentation/ERD-Source.jpg)

### Data Warehouse Model

![DWH](Documentation/DWH-Modelling.jpg)

---

# 👨‍💻 Author

**Mahmoud Saad**

- Junior BI Developer

Connect with me on LinkedIn and GitHub for collaboration and feedback.
