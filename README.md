# Databricks CRM & ERP Data Engineering Pipeline

An end-to-end data engineering project built using **Databricks, PySpark, Spark SQL, Delta Lake, and Unity Catalog**.

The project implements a **Bronze → Silver → Gold Medallion Architecture** to ingest, transform, integrate, and prepare CRM and ERP data for analytics and reporting.

---

## Project Overview

This project demonstrates the development of a complete data engineering pipeline in Databricks, starting from raw CRM and ERP source data and progressing through multiple transformation layers to produce business-ready datasets.

The pipeline includes data ingestion, cleaning, standardization, transformation, integration, and workflow orchestration using **Databricks Jobs**.

---

# 🗄️ Medallion Architecture

The project follows the **Medallion Architecture** to progressively improve data quality and usability.

| Layer | Purpose |
|-------|---------|
| 🥉 **Bronze** | Raw source data |
| 🥈 **Silver** | Cleaned and standardized data |
| 🥇 **Gold** | Business-ready analytical data |

```text
              CRM / ERP Source Data
                       │
                       ▼
                ┌────────────┐
                │   BRONZE   │
                │ Raw Data   │
                └─────┬──────┘
                      │
                      ▼
                ┌────────────┐
                │   SILVER   │
                │ Cleaned &  │
                │ Standardized
                └─────┬──────┘
                      │
                      ▼
                ┌────────────┐
                │    GOLD    │
                │ Business-  │
                │ Ready Data │
                └─────┬──────┘
                      │
                ┌─────┴─────┐
                ▼           ▼
            Analytics    Reporting

```
## 🛠️ Technologies Used

| Technology | Purpose |
|------------|---------|
| **Databricks** | Data processing and pipeline orchestration |
| **PySpark** | Data transformation and processing |
| **Spark SQL** | SQL-based data transformations |
| **Delta Lake** | Reliable data storage and table management |
| **Unity Catalog** | Data organization and governance |
| **Python** | Data engineering and transformation logic |
| **SQL** | Data transformation and analytical queries |

---

## 📂 Data Sources

The project processes data from **CRM and ERP systems**, covering different business domains such as:

- Customers
- Products
- Product Categories
- Sales
- Orders
- Customer Information
- Product Information

The raw datasets are ingested into the Bronze layer and progressively transformed through the Silver and Gold layers.

---

# 🥉 Bronze Layer

The Bronze layer stores the raw source data with minimal transformation.

### Key Operations

- Ingest raw CRM and ERP datasets
- Preserve source data
- Handle initial schema requirements
- Store data as Delta tables
- Organize datasets using Unity Catalog

The Bronze layer acts as the foundation for all downstream transformations.

---

# 🥈 Silver Layer

The Silver layer contains cleaned and standardized datasets.

### Transformations Performed

- Remove duplicate records
- Handle missing values
- Convert data types
- Parse and standardize dates
- Standardize column names
- Normalize identifiers across source systems
- Clean inconsistent source values
- Apply source-specific transformation rules

The goal of the Silver layer is to produce reliable and reusable datasets for downstream processing.

---

# 🥇 Gold Layer

The Gold layer contains curated, business-ready datasets designed for analytics and reporting.

### Key Transformations

- Integrate CRM and ERP datasets
- Join data from multiple sources
- Apply business rules
- Use conditional transformations
- Apply window functions
- Implement fallback logic
- Create analytical datasets
- Produce customer, product, and sales-related datasets

Both **PySpark and Spark SQL** were used to implement Gold-layer transformations.

       ▼
   🥇 Gold
       │
       ▼
Analytics & Reporting
