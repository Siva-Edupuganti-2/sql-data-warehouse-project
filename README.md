# 🏭 SQL Data Warehouse Project

> Building a modern data warehouse with SQL Server, including ETL processes, data modelling, and analytics.

---

## 📌 Project Overview

This project implements a full **layered data warehouse** using SQL Server, following industry-standard data engineering practices. Raw transactional data is ingested, cleaned, and transformed across three distinct layers — ultimately producing a reliable, query-ready analytical layer for business reporting and KPIs.

---

## 🏗️ Architecture — Medallion Layers

```
Raw Source Data
      ↓
 [Bronze Layer]  → Raw ingestion, no transformations
      ↓
 [Silver Layer]  → Cleaned, standardised, validated data
      ↓
  [Gold Layer]   → Business-ready fact & dimension tables
```

| Layer  | Purpose                                  |
|--------|------------------------------------------|
| Bronze | Load raw source data as-is into SQL Server |
| Silver | Clean, deduplicate, and standardise data |
| Gold   | Model data into star schema for analytics |

---

## 📁 Repository Structure

```
sql-data-warehouse-project/
│
├── scripts/
│   ├── init_database.sql          # Database initialisation
│   ├── bronze/
│   │   ├── ddl_bronze.sql         # Bronze layer table definitions
│   │   └── proc_load_bronze.sql   # Stored procedure to load raw data
│   ├── silver/
│   │   ├── ddl_silver.sql         # Silver layer table definitions
│   │   └── proc_load_silver.sql   # Stored procedure to clean & transform
│   └── gold/
│       └── ddl_gold.sql           # Gold layer views & fact/dimension tables
│
├── datasets/                      # Source data files
├── docs/                          # Architecture diagrams & documentation
└── tests/
    └── quality_checks_gold.sql    # Data quality validation scripts
```

---

## 🔄 ETL Pipeline

1. **Extract** — Raw data loaded into the Bronze layer via `proc_load_bronze.sql`
2. **Transform** — Data cleaned, standardised, and validated in the Silver layer via `proc_load_silver.sql`
3. **Load** — Business-ready tables and views created in the Gold layer via `ddl_gold.sql`

---

## 🛠️ Tech Stack

- **Database:** Microsoft SQL Server
- **Language:** T-SQL
- **Concepts:** ETL, Data Modelling, Star Schema, Stored Procedures, Data Quality Checks

---

## 🚀 How to Run

1. Clone this repository
2. Open SQL Server Management Studio (SSMS)
3. Run `scripts/init_database.sql` to set up the database
4. Execute `scripts/bronze/ddl_bronze.sql` then `proc_load_bronze.sql`
5. Execute `scripts/silver/ddl_silver.sql` then `proc_load_silver.sql`
6. Execute `scripts/gold/ddl_gold.sql` to create analytical views
7. Run `tests/quality_checks_gold.sql` to validate data integrity

---

## 📊 Key Features

- ✅ Layered Medallion Architecture (Bronze → Silver → Gold)
- ✅ Reusable stored procedures for automated data loading
- ✅ Data quality checks to ensure reliable outputs
- ✅ Star schema design for efficient analytical querying
- ✅ Modular, well-organised SQL scripts

---

## 👤 Author

**Sri Siva Satya Venkat Edupuganti**  
📧 sivaedupuganti28@gmail.com  
🔗 [LinkedIn](https://www.linkedin.com/in/)
