# Databricks CRM & ERP Data Engineering Pipeline

An end-to-end data engineering pipeline built using **Azure Databricks**, **PySpark**, **Spark SQL**, and **Delta Lake** to transform raw CRM and ERP data into clean, business-ready datasets.

The project follows the **Medallion Architecture (Bronze → Silver → Gold)** and uses **Unity Catalog** for data organization and governance.

---

## 🏗️ Architecture

```text
                CRM / ERP Source Data
                         │
                         ▼
                  ┌─────────────┐
                  │   BRONZE    │
                  │ Raw Data    │
                  └──────┬──────┘
                         │
                         ▼
                  ┌─────────────┐
                  │   SILVER    │
                  │ Cleaned &   │
                  │ Standardized│
                  └──────┬──────┘
                         │
                         ▼
                  ┌─────────────┐
                  │    GOLD     │
                  │ Business-   │
                  │ Ready Data  │
                  └─────────────┘
                         │
              ┌──────────┴──────────┐
              ▼                     ▼
          Analytics             Reporting
