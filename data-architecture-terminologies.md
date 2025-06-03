# Modern Data Terminologies & Architecture Cheat Sheet

A complete and beginner-friendly guide to understand key terms, tools, and workflows in modern data engineering.  
Whether you're a data analyst, engineer, scientist, or student – this cheat sheet simplifies the complex world of data systems.

---

## Introduction

The modern data stack is a collection of tools and technologies used to collect, store, process, and analyze data efficiently.  
This guide explains the core concepts and tools used in scalable data architecture.

---

## 1. Storage Systems

**Where and how data is stored before it's processed or analyzed.**

| Term             | Description                                                                                          | Tools/Examples                                       |
|------------------|------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| Database         | Stores structured data in tables (rows and columns). Used for real-time operations like insert, update, delete. | PostgreSQL, MySQL, MongoDB, Oracle DB               |
| Data Warehouse   | Stores large amounts of structured data, mainly for analysis. Optimized for complex queries and reports. | Snowflake, BigQuery, Redshift, Azure Synapse       |
| Data Lake        | Stores raw data of all types (structured, semi-structured, unstructured). Used for backups, ML, and logs. | AWS S3, Azure Data Lake, Google Cloud Storage, HDFS |
| Lakehouse        | Combines data lake flexibility with warehouse performance. Supports analytics and transactions.       | Databricks, Delta Lake, Apache Iceberg              |

---

## 2. Data Processing

**How data moves, changes, and gets ready for analysis.**

| Term             | Description                                                                                          | Tools/Examples                                       |
|------------------|------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| ETL              | Extract, Transform, Load – clean and format data before storing it in a warehouse.                  | Apache Airflow, Talend, Informatica, Python scripts  |
| ELT              | Extract, Load, Transform – load raw data first, then transform it inside the warehouse.             | dbt, BigQuery SQL, Snowflake SQL                     |
| CDC              | Change Data Capture – tracks changes in databases and updates target systems in real time.          | Debezium, Fivetran, StreamSets                       |
| Streaming        | Real-time data processing, useful for logs, events, and sensors.                                    | Apache Kafka, Apache Flink, AWS Kinesis              |
| Batch Processing | Runs data jobs on a schedule (daily, hourly). Used for reports, backups, etc.                       | Airflow, dbt, Apache NiFi                            |

---

## 3. Data Modeling

**Designing the structure of data for easier access, analysis, and performance.**

| Term             | Description                                                                                          | Tools/Examples                          |
|------------------|------------------------------------------------------------------------------------------------------|-----------------------------------------|
| Star Schema      | Simple structure with one central fact table linked to dimension tables. Easy to query.              | Snowflake, Redshift, Power BI           |
| Snowflake Schema | A more normalized version of star schema. Reduces data size, but queries are more complex.          | Traditional warehouses                  |
| Fact Table       | Stores numbers and metrics (like sales, clicks) linked to business activities.                      | Used in all data marts                  |
| Dimension Table  | Stores descriptive info (like customer names, product details). Adds meaning to facts.              | Used in BI and reporting                |
| Data Mart        | A smaller part of the warehouse focused on one area (like marketing or sales).                      | Built using dbt, SQL                    |

---

## 4. Analysis and Consumption

**Where end-users and analysts interact with the data to generate insights.**

| Term             | Description                                                                                          | Tools/Examples                           |
|------------------|------------------------------------------------------------------------------------------------------|------------------------------------------|
| BI Tools         | Used to create dashboards and reports for business users.                                            | Tableau, Power BI, Looker, Superset      |
| Data Exploration | Ad-hoc analysis done by analysts or scientists to find insights or problems.                        | Jupyter, DBeaver, Hex, Mode              |
| Semantic Layer   | Converts raw data into user-friendly logic for easier analysis.                                      | LookML, Cube.js                          |
| OLTP             | Handles real-time transactions like bookings and payments.                                           | MySQL, PostgreSQL, SQL Server            |
| OLAP             | Handles analytical queries on historical data with fast aggregations.                               | Snowflake, BigQuery, ClickHouse          |

---

## License

This cheat sheet is open for educational use.  
Feel free to contribute or use it in your own learning or projects.

---

### Created by Ashish Jangra — Data Science Mentor & Content Creator  
[GitHub: ashishjangra27](https://github.com/ashishjangra27)
