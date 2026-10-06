# Databricks CRM & ERP Data Engineering Pipeline

An end-to-end data engineering project built using **Databricks, PySpark, Spark SQL, Delta Lake, and Unity Catalog**.

The project implements a **Bronze → Silver → Gold Medallion Architecture** to ingest, transform, integrate, and prepare CRM and ERP data for analytics and reporting.

---

## Project Overview

This project demonstrates the development of a complete data engineering pipeline in Databricks, starting from raw CRM and ERP source data and progressing through multiple transformation layers to produce business-ready datasets.

The pipeline includes data ingestion, cleaning, standardization, transformation, integration, and workflow orchestration using **Databricks Jobs**.

---

## Architecture

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
