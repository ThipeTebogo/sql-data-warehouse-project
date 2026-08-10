
# SQL Data Warehouse Project

Building a modern data warehouse with SQL — covering the ETL process, data modeling, and analytics, with a Power BI dashboard layer on top.

## 📖 Overview

This project implements an end-to-end data warehouse using the **Medallion Architecture** (Bronze → Silver → Gold), taking raw source data through cleansing and transformation into a business-ready star schema, and finally into an interactive Power BI dashboard.

- **Bronze layer** – raw data loaded as-is from source files
- **Silver layer** – cleansed, standardized, and conformed data
- **Gold layer** – business-ready fact and dimension tables (star schema) for reporting
- **Dashboard layer** – Power BI report built on top of the Gold layer, with custom DAX measures and calculated columns

## 🗂️ Repository Structure

```
sql-data-warehouse-project/
│
├── Dashboard/            # Power BI dashboard file(s) and related assets
├── datasets/             # Raw source datasets used to populate the warehouse
├── docss/                # Project documentation (architecture, data catalog, naming conventions)
├── scripts/              # SQL scripts for the ETL pipeline (bronze / silver / gold layers)
├── tests/                # Data quality and validation scripts
├── Calculated Columns     # DAX calculated columns used in the Power BI model
├── Date Table              # DAX date/calendar table used for time-intelligence
├── Measures                # DAX measures powering the dashboard
├── LICENSE                # MIT License
└── README.md
```

## 🏗️ Data Architecture

The warehouse follows the Medallion Architecture:

1. **Bronze** – ingest raw data from source files into staging tables, no transformations.
2. **Silver** – clean, standardize, and normalize the data (deduplication, type fixes, business rules).
3. **Gold** – model the data into a star schema (fact and dimension tables) optimized for analytics.
4. **Dashboard** – Power BI connects to the Gold layer; DAX measures and calculated columns (see `Measures`, `Calculated Columns`, and `Date Table`) drive the report visuals.


## 🛠️ Tools & Skills Demonstrated

- SQL (T-SQL) for ETL and data transformation
- Data modeling (star schema, fact/dimension design)
- Data quality testing
- Power BI & DAX (measures, calculated columns, time intelligence)

## 📄 License

This project is licensed under the [MIT License](LICENSE) — you're free to use, modify, and share it with attribution.

## 🙋 About

Built by [ThipeTebogo](https://github.com/ThipeTebogo) as a portfolio project demonstrating data engineering and analytics skills, from raw data through to a finished BI dashboard.
