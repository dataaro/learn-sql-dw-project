# 🏗️ Modern Data Warehouse Construction with SQL Server

An end-to-end Modern Data Warehouse solution built with **Microsoft SQL Server** and **T-SQL**, covering raw data ingestion, multi-tier ETL pipelines (Bronze, Silver, Gold), dimensional data modeling, data quality testing, and analytics.

---

## 📌 Project Overview

This repository demonstrates the complete lifecycle of building an enterprise-grade Data Warehouse using **SQL Server** and **T-SQL**:
- **ETL Processes:** Extracting raw data, transforming datasets across data layers, and loading conformed data marts.
- **Data Modeling:** Implementing dimensional modeling (Star Schema / Snowflake Schema) with Fact and Dimension tables for business reporting.
- **Data Quality & Analytics:** Automated testing scripts to ensure data integrity, referential consistency, and analytical query optimization.

---

## 📁 Repository Structure

```text
learn-sql-dw-project/
│
├── Datasets/              # Raw data files and source datasets
├── docs/                  # Architecture diagrams, data dictionary, and project documentation
├── scripts/               # T-SQL scripts organized by data warehouse layers
│   ├── bronze_layer/      # Ingestion & staging scripts (Raw Data)
│   ├── silver_layer/      # Cleansing, transformation, and business rule enforcement
│   └── gold_layer/        # Data modeling (Fact & Dimension tables / Data Marts)
├── tests/                 # Data validation, consistency, and quality check scripts
├── LICENSE                # MIT License
└── README.md              # Project documentation
```

---

## 🏗️ Data Warehouse Architecture (Medallion Pattern)

The Data Warehouse architecture follows the multi-tiered **Medallion Architecture**:

1. **🥉 Bronze Layer (Staging / Raw):**
   - Direct ingestion of source datasets into staging tables without structural alterations.
   - Full load or incremental loads from source systems.

2. **🥈 Silver Layer (Cleansing & Conforming):**
   - Data cleaning, standardizing data types, handling missing values, and deduplication.
   - Enforcement of business logic and data normalization.

3. **🥇 Gold Layer (Analytics / Data Marts):**
   - Star Schema design featuring Fact and Dimension tables.
   - Optimized with indexes and views ready for Business Intelligence (BI) and reporting tools (Power BI, Tableau, Excel).

---

## 🛠️ Tech Stack & Prerequisites

- **Database Engine:** Microsoft SQL Server
- **Query Language:** T-SQL (100%)
- **Tools:** SQL Server Management Studio (SSMS) / Azure Data Studio
- **Version Control:** Git & GitHub

---

## 🚀 Getting Started

### 1. Prerequisites
Ensure you have **SQL Server** and **SSMS** or **Azure Data Studio** installed on your machine.

### 2. Clone the Repository
```bash
git clone https://github.com/dataaro/learn-sql-dw-project.git
cd learn-sql-dw-project
```

### 3. Execution Sequence
To deploy the Data Warehouse, execute the T-SQL scripts in the following order:

1. **Database & Schema Creation:** Set up the database environment.
2. **Bronze Layer:** Run scripts in `scripts/bronze_layer/` to populate raw staging tables.
3. **Silver Layer:** Run scripts in `scripts/silver_layer/` to transform and clean data.
4. **Gold Layer:** Run scripts in `scripts/gold_layer/` to construct Fact and Dimension tables.
5. **Quality Testing:** Run scripts in `tests/` to validate row counts, uniqueness, and key constraints.

---

## 🧪 Data Quality & Validation

Data integrity is validated using scripts in the `tests/` directory:
- Uniqueness checks on primary keys.
- Referential integrity validation between Fact and Dimension tables.
- Null value checks and column boundary constraints.

---

## 📜 License & Author

- **Author:** [Arouna Alaho](https://github.com/dataaro) (`dataaro`)
- **License:** Distributed under the [MIT License](LICENSE).
