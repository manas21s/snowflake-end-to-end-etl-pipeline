# 🚀 End-to-End Snowflake ETL Pipeline (Production-Grade)

## 📌 Overview
This project demonstrates a **fully automated, production-grade ETL pipeline** built entirely inside Snowflake using:

- Snowpipe (Auto ingestion)
- Streams (CDC - Change Data Capture)
- Tasks (Automation)
- Star Schema (Fact + Dimension)
- SCD Type 2 (Historical tracking)
- AWS S3 integration

---

## 🏗️ Architecture

![Architecture](architecture/architecture_diagram.png)

---

## 🔄 Pipeline Flow

1. Data uploaded to AWS S3
2. Snowpipe auto-ingests into RAW layer
3. Streams track changes (CDC)
4. Tasks automatically trigger transformations
5. Data is loaded into:
   - Dimension tables (SCD Type 2)
   - Fact table
6. Analytics View is updated in real-time
7. BI tools consume final view

---

## 🧱 Data Model

### ⭐ Dimension Tables
- `dim_customer` (SCD Type 2)
- `dim_product` (SCD Type 2)

### ⭐ Fact Table
- `fact_orders`

---

## ⚙️ Technologies Used

- Snowflake
- AWS S3
- Snowpipe
- Streams & Tasks
- SQL

---

## 🔥 Key Features

✅ Real-time data ingestion  
✅ Change Data Capture (CDC)  
✅ Automated ETL (no manual intervention)  
✅ Star schema design  
✅ SCD Type 2 implementation  
✅ BI-ready views  
✅ Monitoring and observability  

---

## 📊 Final Output

**Analytics View:**

```
analytics.sales_dashboard
```

This view provides:
- Sales by city
- Sales by product category
- Total orders
- Revenue

---

## 📈 Monitoring

Pipeline monitoring is available via:

```
analytics.pipeline_monitor
```

---

## 🚀 How to Run

1. Create Snowflake warehouse, database, schemas
2. Setup AWS S3 integration
3. Upload CSV files to S3
4. Run SQL scripts in order:

```
01_setup.sql
02_raw_tables.sql
03_stage_pipe.sql
04_streams.sql
05_dimensions_scd.sql
06_fact_table.sql
07_tasks.sql
08_views.sql
09_monitoring.sql
```

5. Start tasks

---

## 🧠 Learnings

- Designing production ETL pipelines
- Implementing CDC with Streams
- Managing historical data (SCD Type 2)
- Building scalable data models
- Automating workflows using Tasks

---

## 👨‍💻 Author

Manas Shukla

---
