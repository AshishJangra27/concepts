# 📦 Data Terminologies Cheat Sheet

---

## 🗄️ Storage Systems

| Term             | Description                                                                                          | Tools/Examples                                          |
|------------------|------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| **Database**      | A system that stores structured data in tables using rows and columns, optimized for real-time inserts, updates, and deletions. Ideal for transactional systems like login/auth, orders, or payments. | PostgreSQL, MySQL, Oracle DB, MongoDB                   |
| **Data Warehouse**| A specialized system for storing large volumes of historical, structured, and semi-structured data used in reporting, dashboards, and analytical queries. Uses columnar storage for faster aggregations. | Snowflake, BigQuery, Redshift, Azure Synapse            |
| **Data Lake**     | A centralized storage that holds raw data in its native format—structured, semi-structured, or unstructured. Ideal for storing logs, clickstream, audio, video, and backups at low cost. | AWS S3, Azure Data Lake Storage, Google Cloud Storage, HDFS |
| **Lakehouse**     | A hybrid architecture that combines the scalability of Data Lakes with the ACID compliance and query performance of Data Warehouses. Enables analytics and machine learning on the same storage. | Databricks, Delta Lake, Apache Iceberg                  |

---

## 🔁 Data Processing

| Term             | Description                                                                                       | Tools/Examples                                         |
|------------------|---------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| **ETL**           | Extract → Transform → Load. Data is extracted from sources, transformed in staging layers, then loaded into a warehouse. Often used in traditional BI pipelines. | Apache Airflow, Talend, Informatica, Python scripts    |
| **ELT**           | Extract → Load → Transform. Data is first loaded into the warehouse and transformed inside it using SQL. Suitable for cloud-native pipelines. | dbt, Snowflake SQL, BigQuery SQL                       |
| **CDC**           | Change Data Capture. Monitors and captures changes in source databases (inserts, updates, deletes) to sync them in real-time to target systems. | Debezium, Fivetran, StreamSets                         |
| **Streaming**     | Continuous ingestion and processing of real-time event/data streams with low latency. Used for real-time dashboards, alerts, and ML pipelines. | Apache Kafka, Apache Flink, AWS Kinesis                |
| **Batch Processing** | Processing data at scheduled intervals (e.g., hourly, nightly). Suitable for large, periodic jobs like report generation or backups. | Airflow, dbt, Apache NiFi                              |

---

## 🧠 Data Modeling

| Term               | Description                                                                                           | Tools/Examples                         |
|--------------------|-------------------------------------------------------------------------------------------------------|----------------------------------------|
| **Star Schema**     | A denormalized model where a central fact table is connected to multiple dimension tables. Simplifies querying and is optimized for OLAP systems. | Used in Snowflake, Redshift, Power BI  |
| **Snowflake Schema**| A normalized version of star schema where dimensions are split into sub-dimensions. Saves storage but adds complexity to queries. | Used in traditional warehouses          |
| **Fact Table**      | Stores quantitative, measurable business metrics (e.g., sales, revenue, clicks) and keys to dimensions. | Part of warehouse schemas              |
| **Dimension Table** | Stores descriptive context related to business entities (e.g., customer, product, region) and connects to fact tables. | Used across all data marts and models  |
| **Data Mart**       | A focused, subject-specific subset of the data warehouse designed for departmental analysis (e.g., marketing, finance, sales). | Built using dbt, SQL, or warehouse tools |

---

## 📊 Analysis & Consumption

| Term               | Description                                                                                         | Tools/Examples                                |
|--------------------|-----------------------------------------------------------------------------------------------------|------------------------------------------------|
| **BI Tools**        | Business Intelligence platforms used for visualizing data, building dashboards, and sharing insights with stakeholders. | Tableau, Power BI, Looker, Superset            |
| **Data Exploration**| The process of interactively querying and inspecting data to find patterns, anomalies, or trends. Used in research and ad hoc analysis. | Jupyter, DBeaver, Hex, Mode                    |
| **Semantic Layer**  | A translation layer that maps complex SQL logic into business-friendly terms, enabling self-service analytics. | LookML (Looker), Cube.js                       |
| **OLTP**            | Online Transaction Processing systems optimized for high-speed, real-time reads/writes and used in operational databases. | MySQL, PostgreSQL, SQL Server                  |
| **OLAP**            | Online Analytical Processing systems designed for complex aggregations and analytical workloads across large datasets. | Snowflake, BigQuery, ClickHouse                |

