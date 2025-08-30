# Taxi Repositioning System (TRS)
Week 6 Interim Project for Generation Singapore Jr. Data Engineering Programme (JDE07).  
Designed a real-time ETL pipeline leveraging API data and PostgreSQL to optimise taxi fleet distribution in Singapore.

## Overview

The Taxi Repositioning System (TRS) is a **real-time micro-batch streaming ETL pipeline** that tracks live taxi availability, enriched with **geospatial data**, and writes processed results into **PostgreSQL** for analytics and recommendations.

**Goal:** Identify **over-supplied** and **under-served** areas and provide **repositioning recommendations** to improve pickup times and reduce empty mileage.

## Data Sources
- **LTA Data Mall API (Taxi Availability)** – live taxi locations across Singapore  
- **Kaggle Singapore City Geo-coordinates** – maps postal codes and planning areas for geospatial tagging  

## Tech Stack
- Python (Pandas, Matplotlib, Requests)  
- PostgreSQL + SQL  
- ETL (micro-batch streaming)  
- Geospatial analysis (Haversine)  

## Pipeline Workflow
1. Fetch live taxi data from LTA API  
2. Timestamp and batch the records  
3. Clean and transform data (null handling, de-duplication, re-indexing)  
4. Live mapping of available taxis and recommendation to Singapore places (geospatial tagging)  
5. Load into PostgreSQL with relational schema  
6. Run SQL queries & visualisations for analysis and recommendations  

## Key Features
- **Live Ingestion (Micro-batch):** Calls the API, timestamps records, and appends batches to a relational store.
- **Data Cleaning & Transformation:** Handles duplicates, nulls, and re-indexing; normalises tables; adds surrogate keys.
- **Geospatial Tagging:** Maps taxi coordinates to planning areas and points of interest (Haversine-based proximity).
- **PostgreSQL Schema:** Structured tables for taxis, places, and batch logs; idempotent DDL; foreign-key integrity.
- **Analytics & Visualisation:** SQL for aggregated supply patterns; Python/Matplotlib for quick charts and recommendation insights.


