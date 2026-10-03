# FinOps & Infrastructure Telemetry Pipeline

## Overview
This project demonstrates an end-to-end enterprise Data Engineering pipeline using a Medallion Architecture (Bronze, Silver, Gold). It processes cloud infrastructure billing telemetry (FinOps data) to monitor, visualize, and optimize compute costs. 

## Architecture
* **Databricks:** Core compute and orchestration engine.
* **PySpark:** Used for distributed data transformations and memory-optimized joins.
* **Medallion Layers:**
  * `00_Hello_Lakehouse_Bronze`: Raw data ingestion and change data capture.
  * `01_Hello_Lakehouse_Silver`: Data cleansing, schema enforcement, and deduplication.
  * `02_Hello_Lakehouse_Gold`: Business-level aggregations ready for reporting.
  * `03_Hello_Lakehouse_Vizualization`: Final data presentation and BI integration.

## Key Technical Highlights
* Utilized Delta Lake format for ACID transactions and time travel.
* Implemented memory-optimized Spark configurations to handle complex joins without schema data loss.
