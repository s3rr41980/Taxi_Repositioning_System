# Taxi Repositioning System (TRS)
Week 6 Interim Project for Generation Singapore Jr. Data Engineering Programme (JDE07)

**One-line headline:** Designed a real-time ETL pipeline leveraging API data and PostgreSQL to optimise taxi fleet distribution in Singapore.

## Overview

The Taxi Repositioning System (TRS) is a **real-time micro-batch streaming ETL pipeline** that tracks live taxi availability, enriches it with **geospatial context**, and writes processed results into **PostgreSQL** for analytics and recommendations.

- **Data sources:** LTA Data Mall Taxi Availability API (live supply), Singapore geospatial reference data (planning areas / neighbourhood tagging).
- **Goal:** Identify **over-supplied** and **under-served** areas and provide **repositioning recommendations** to improve pickup times and reduce empty mileage.

## Key Features

- **Live Ingestion (Micro-batch):** Polls the API, timestamps records, and appends batches to a relational store.
- **Data Cleaning & Transformation:** Handles duplicates, nulls, and re-indexing; normalises tables; adds surrogate keys.
- **Geospatial Tagging:** Maps taxi coordinates to planning areas and points of interest (Haversine-based proximity).
- **PostgreSQL Schema:** Structured tables for taxis, places, and batch logs; idempotent DDL; foreign-key integrity.
- **Analytics & Visualisation:** SQL for aggregated supply patterns; Python/Matplotlib for quick charts and recommendation insights.

## Project Structure

