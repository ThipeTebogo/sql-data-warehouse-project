# sql-data-warehouse-project

**Project Overview**
This project demonstrates a complete data analytics pipeline, showcasing industry best practices in:
	**Data Warehousing: **Dimensional modeling, ETL processes, and star schema design
  **Data Analysis:** SQL queries for business insights and performance metrics
	**Data Visualization:** Interactive Power BI dashboard with DAX measures and calculated columns

The solution transforms raw operational data into actionable business intelligence, enabling stakeholders to make data-driven decisions.

🏗️ **Architecture**
Raw Data Sources → Data Warehouse (Star Schema) → Power BI Dashboard → Insights


**Layer	**								**Technology**														**	Purpose**
Data Warehouse						SQL (Star Schema)													Dimensional modeling with fact and dimension tables
Data Processing						SQL Queries, ETL													Data cleaning, transformation, and loading
Analytics Layer						DAX Measures, Calculated Columns					Business metrics and KPI calculations
Visualization							Power BI Desktop													Interactive dashboards and reports

🗃️ **Data Warehouse Design**

📐 **Schema Architecture**
The data warehouse follows a star schema design for optimal query performance and intuitive analysis:

┌─────────────────┐
│   dim_customer  │
├─────────────────┤
│ customer_key    │─────┐
│ customer_name   │     │
│ region          │     │
└─────────────────┘     │
                        ▼
┌─────────────────┐ ┌─────────────────┐ ┌─────────────────┐
│   dim_product   │ │   fact_sales    │ │   dim_date      │
├─────────────────┤ ├─────────────────┤ ├─────────────────┤
│ product_key     │─────┤ order_key      │─────┤ date_key        │
│ product_name    │ │ customer_key    │ │ full_date       │
│ category        │ │ product_key     │ │ year            │
│ unit_price      │ │ order_date_key  │ │ quarter         │
└─────────────────┘ │ ship_date_key   │ │ month           │
                    │ due_date_key     │ └─────────────────┘
                    │ sales_amount     │
                    │ quantity         │
                    └─────────────────┘


📁 **Key Tables**
**fact_sales:** Transactional data including sales amounts, quantities, and date keys
**dim_customer:** Customer demographics and segmentation attributes
**dim_product: **Product details, categories, and pricing information
**dim_date:** Date dimension for time-based analysis (supports fiscal calendar)

📈 **Power BI Dashboard & Analytics**
**Sales Performance:** Total revenue, order volume, average order value
**Delivery Analytics:** On-time delivery rate, late deliveries analysis, shipping performance
**Time Intelligence: **Year-over-Year growth, Month-over-Month trends, rolling averages
**Customer Insights:** Customer segmentation, repeat purchase rate, regional performance

🛠️ **Technical Implementation**
**Tools & Technologies**

**Database:** SQL Server / PostgreSQL (data warehouse)
**Data Modeling: **Star Schema design, dimensional modeling
**ETL:** SQL queries for data extraction and transformation
**DAX: **Calculated measures and columns in Power BI
**Visualization: **Power BI Desktop, custom visuals

📦 data-warehouse-project/
├─ 📁 data-warehouse/
│  ├─ 📄 schema-diagram.png
│  ├─ 📄 table-definitions.sql
│  └─ 📄 etl-process.sql
├─ 📁 dax-measures/
│  ├─ 📄 sales-measures.md
│  ├─ 📄 delivery-analytics.md
│  └─ 📄 time-intelligence.md
├─ 📁 dashboard-screenshots/
│  ├─ 📸 01-sales-overview.png
│  ├─ 📸 02-delivery-analysis.png
│  ├─ 📸 03-customer-insights.png
│  └─ 📸 04-product-performance.png
├─ 📁 powerbi-files/
│  └─ 📄 sales-dashboard.pbix
└─ 📄 README.md




