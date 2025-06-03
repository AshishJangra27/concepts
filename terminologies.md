# 🚀 Modern Data Terminologies & Architecture Cheat Sheet

A complete guide to understanding key terms, tools, and flows in modern data engineering. Whether you're a data analyst, engineer, scientist, or student — this repo simplifies the complex world of data systems.

---

## 📘 Introduction

The modern data stack is a combination of technologies that allow businesses to ingest, store, transform, and analyze data efficiently. This cheat sheet covers key terminologies and toolsets that form the foundation of any scalable data architecture.

---

## 🗄️ 1. Storage Systems

| 🏷 Term         | 📖 Description                                                                                                                                 | 🔧 Tools/Examples                                      |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| **Database**    | Stores structured data in rows & columns. Optimized for real-time transactions like CRUD operations.                                            | PostgreSQL, MySQL, MongoDB, Oracle DB                  |
| **Data Warehouse** | Stores structured, historical data for analytical queries. Uses columnar storage and optimized for OLAP workloads.                        | Snowflake, BigQuery, Redshift, Azure Synapse           |
| **Data Lake**   | Stores raw data (structured, semi-structured, and unstructured). Ideal for logs, backups, media, and machine learning inputs.                 | AWS S3, Azure Data Lake, Google Cloud Storage, HDFS    |
| **Lakehouse**   | Combines flexibility of Data Lakes with the structure & performance of Warehouses. Enables ACID compliance and analytics on the same layer.   | Databricks, Delta Lake, Apache Iceberg                 |

---

## 🔁 2. Data Processing

| 🏷 Term         | 📖 Description                                                                                                                                 | 🔧 Tools/Examples                                      |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| **ETL**         | Extract → Transform → Load. Clean and reshape data before loading it into the warehouse.                                                       | Apache Airflow, Talend, Informatica, Python scripts    |
| **ELT**         | Extract → Load → Transform. Load raw data first, then use SQL inside the warehouse to transform.                                               | dbt, BigQuery SQL, Snowflake SQL                      |
| **CDC**         | Change Data Capture. Tracks changes in source DBs (inserts, updates, deletes) and syncs them to the target system in real time.                | Debezium, Fivetran, StreamSets                         |
| **Streaming**   | Real-time data ingestion and processing for logs, sensors, events, etc.                                                                        | Apache Kafka, Apache Flink, AWS Kinesis                |
| **Batch Processing** | Scheduled execution of jobs. Common for daily reports, aggregations, and backups.                                                     | Airflow, dbt, Apache NiFi                              |

---

## 🧠 3. Data Modeling

| 🏷 Term            | 📖 Description                                                                                                                              | 🔧 Tools/Examples                         |
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------|
| **Star Schema**     | A central fact table connected to multiple dimension tables. Flat and optimized for BI tools.                                             | Snowflake, Redshift, Power BI            |
| **Snowflake Schema**| A normalized variant of the star schema that saves space but increases query complexity.                                                  | Traditional data warehouses              |
| **Fact Table**      | Stores quantitative metrics (e.g., revenue, clicks) linked to business activities.                                                       | Used across all data marts               |
| **Dimension Table** | Describes business entities (e.g., customers, products). Adds context to the facts.                                                      | Used in BI and analytics modeling        |
| **Data Mart**       | A subject-focused part of the data warehouse used by individual departments (e.g., marketing, sales).                                     | Built with dbt, SQL transformations      |

---

## 📊 4. Analysis & Consumption

| 🏷 Term            | 📖 Description                                                                                                                       | 🔧 Tools/Examples                                 |
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| **BI Tools**        | Visualize KPIs, trends, and reports with dashboards accessible to business stakeholders.                                            | Tableau, Power BI, Looker, Superset              |
| **Data Exploration**| Ad hoc querying and profiling done by analysts or scientists. Often used to uncover insights or anomalies.                          | Jupyter, DBeaver, Hex, Mode                       |
| **Semantic Layer**  | Translates raw SQL into business-friendly logic for self-service analytics.                                                        | LookML (Looker), Cube.js                          |
| **OLTP**            | Handles real-time transactional workloads like bookings, payments, and updates.                                                    | MySQL, PostgreSQL, SQL Server                    |
| **OLAP**            | Designed for slicing/dicing historical data with fast aggregations and filtering.                                                  | Snowflake, BigQuery, ClickHouse                  |

---

## 📎 License

This cheat sheet is open-source and maintained for educational use.  
Feel free to contribute or reference it in your own projects.

---

### 👨‍💻 Created by [Ashish Jangra](https://github.com/ashishjangra27) — Data Science Mentor & Creator
