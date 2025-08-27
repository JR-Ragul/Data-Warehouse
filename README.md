# Data-Warehouse
This project builds a MySQL Data Warehouse using Bronze-Silver-Gold architecture. It ingests raw CRM &amp; ERP data, cleans and standardizes it, applies transformations, and creates star-schema-based analytical views for reporting, showcasing advanced SQL techniques and ETL design.

# MySQL Data Warehouse – Bronze, Silver, Gold Architecture

## Overview
This project demonstrates the design and implementation of a **Data Warehouse** using **MySQL**, structured around the **Medallion Architecture**:
- **Bronze Layer:** Raw data ingestion from CRM and ERP systems.
- **Silver Layer:** Cleaned and transformed datasets.
- **Gold Layer:** Analytics-ready views for BI and reporting.

The pipeline covers data cleaning, transformation, dimensional modeling, and analytical view creation.

---

## Features
- Multi-layer Data Warehouse (Bronze → Silver → Gold)
- Data cleansing using `REGEXP_REPLACE`, `TRIM`, and `CASE` expressions
- Deduplication with `ROW_NUMBER()` window functions
- Star schema modeling with **dimension** and **fact** tables
- Analytical views for reporting (dim_cust, dim_prd, facts_sls)

---

## Technologies Used
- **MySQL 8.0+**
- **SQL Features:** Window Functions, CASE Statements, Views, Joins
- **ETL Process:** Truncate & Load, Data Cleaning, Standardization

---

---

## How It Works
1. **Bronze Layer**
   - Loads raw CRM and ERP data from CSV files into staging tables.
   - Performs minimal validation (date correction, trimming).

2. **Silver Layer**
   - Cleans and standardizes data:
     - Removes invalid characters.
     - Maps coded values (e.g., gender `M`/`F` → `Male`/`Female`).
     - Fixes inconsistent country codes.
   - Deduplicates using `ROW_NUMBER()`.

3. **Gold Layer**
   - Creates final analytical views:
     - **dim_cust:** Customer Dimension.
     - **dim_prd:** Product Dimension.
     - **facts_sls:** Sales Fact Table.
   - Supports BI dashboards and analytical queries.

---


 

## Repository Structure

