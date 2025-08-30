# 🚕 Taxi Repositioning System (TRS)

Week 6 Interim Project for **Generation Singapore Jr. Data Engineering Programme (JDE07)**  
Designed a **real-time ETL pipeline** leveraging API data and PostgreSQL to optimise taxi fleet distribution in Singapore.

---

## 📌 Overview
The Taxi Repositioning System (TRS) is a **real-time micro-batch streaming ETL pipeline** that tracks live taxi availability, enriches it with **geospatial data**, and writes processed results into **PostgreSQL** for analytics and recommendations.

🎯 **Goal:** Identify **over-supplied** and **under-served** areas, then recommend repositioning strategies to improve pickup times and reduce empty mileage.

---

## 📊 Data Sources
- **LTA Data Mall API (Taxi Availability)** – live taxi locations across Singapore  
- **Kaggle Singapore City Geo-coordinates** – maps postal codes and planning areas for spatial tagging  

---

## 🛠 Tech Stack
- **Python:** Pandas, Matplotlib, Requests  
- **Database:** PostgreSQL + SQL  
- **ETL:** Micro-batch streaming pipeline  
- **Geospatial:** Haversine formula for proximity & spatial tagging  

---

## 🔄 Pipeline Workflow
1. Fetch live taxi data from LTA API  
2. Timestamp and batch records  
3. Clean & transform data (null handling, de-duplication, re-indexing)  
4. Map coordinates to Singapore planning areas (geospatial tagging + recommendations)  
5. Load structured data into PostgreSQL with relational schema  
6. Run SQL queries & visualisations for analytics and fleet optimisation  

---

## 🌟 Key Features
- **Live Ingestion (Micro-batch):** Automated API polling with batch appends  
- **Data Cleaning & Transformation:** Handles duplicates, nulls, re-indexing, and surrogate keys  
- **Geospatial Tagging:** Maps taxi coordinates to real-world neighbourhoods  
- **PostgreSQL Schema:** Relational tables with foreign-key integrity and idempotent DDL  
- **Analytics & Visualisation:** SQL queries and Python charts to reveal underserved vs oversupplied areas  

---

## 🚀 Outcomes (Projected)
- ✅ **15% faster pickups**  
- ✅ **8–12% more rides per hour**  
- ✅ **~10% fewer empty trips**  

---

## 🎓 Skills Demonstrated
Python (Pandas, Matplotlib), API Integration, ETL Pipelines, PostgreSQL, SQL Queries,  
Data Cleaning, Data Visualisation, Geospatial Analysis



