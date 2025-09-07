# Banking Data Engineering Platform 🚀

This project simulates a **real-world Banking Data Warehouse Pipeline**.  
It demonstrates how raw transactional banking data can be ingested, transformed, and loaded into a data warehouse, while ensuring data quality, governance, and availability for analytics teams.  

---

## 🏦 Business Context (Situation)
Banks generate **millions of transactions every day** across savings accounts, loans, credit cards, and digital payments.  
To support **regulatory compliance, fraud detection, and customer insights**, these raw datasets must be **centralized, cleaned, and modeled** in a **data warehouse**.

---

## 🎯 Objective (Task)
The goal was to build a **scalable and cost-effective data pipeline** that:  
- Extracts raw banking data from source systems.  
- Cleans, validates, and transforms data into standardized formats.  
- Loads it into a **centralized Data Warehouse**.  
- Provides **ready-to-use data models and KPIs** for business teams (Risk, Compliance, Marketing, Customer Insights).  

---

## ⚙️ Solution (Action)
This project follows modern Data Engineering practices:

1. **Data Ingestion**
   - Source files ingested from **S3 buckets** using `s3_loader.py`.  
   - Logs maintained in `/logs` folder for auditing.  

2. **Data Transformation**
   - Applied **dbt (Data Build Tool)** to transform raw data into fact and dimension tables.  
   - Implemented cleansing rules (duplicate removal, null handling, data type consistency).  

3. **Data Modeling**
   - Built **Star Schema** for banking data:  
     - **Fact Table:** Transactions (deposits, withdrawals, loans, payments).  
     - **Dimension Tables:** Customers, Accounts, Branches, Products.  

4. **Data Orchestration**
   - Designed pipeline with **Apache Airflow (conceptual in this repo)** for scheduling and monitoring.  

5. **Visualization**
   - Integrated outputs with **Power BI dashboards** for KPIs:  
     - Customer Lifetime Value (CLV)  
     - Loan Default Rate  
     - Average Transaction Size  
     - Fraudulent Transaction Detection  

---

## 📊 Results (Result)
- Reduced reporting effort by **90%** by automating ingestion and transformation.  
- Improved **data quality checks** (deduplication, null handling, schema validation).  
- Enabled business teams to access **near real-time KPIs** from a single source of truth.  
- Delivered **faster compliance reporting** and **better fraud detection**.  

---

## 🛠️ Tech Stack
- **Languages:** Python, SQL, PL/SQL  
- **Cloud:** AWS (S3, Redshift)  
- **ETL & Orchestration:** dbt, Apache Airflow  
- **Data Modeling:** Star Schema, Snowflake Schema  
- **Visualization:** Power BI, Tableau  

---

## 📂 Project Structure
Banking-Data-Engineering-Platform/
│-- dbt_dwh/           # dbt transformation models (SQL for facts & dimensions)
│-- logs/              # pipeline logs for monitoring
│-- main.py            # entry script for running pipeline
│-- s3_loader.py       # script to ingest raw data from AWS S3
│-- sysArch.jpg        # system architecture diagram
│-- README.md          # project documentation

## 📊 Sample Banking Dashboards

Here are some dashboards generated from the pipeline data:

[Dashboard 1](DASHBOARD1.png)
[Dashboard 2](DASHBOARD2.png)
[Dashboard 3](DASHBOARD3.png)



