# lahore-weather-pyspark-pipeline
Real-time OpenWeather API data ingestion pipeline built on Databricks using PySpark, Delta Lake, and Spark SQL.
# Real-Time OpenWeather Ingestion Pipeline (PySpark & Delta Lake)

An end-to-end data engineering pipeline built on Databricks using PySpark to ingest live weather metrics from the OpenWeather REST API, enrich raw JSON payloads with timestamps, and persist structured time-series data into a Delta Lake table.

## Architecture & Workflow
1. **API Ingestion:** Fetches real-time JSON payloads for Lahore via OpenWeather REST API using Python `requests`.
2. **PySpark Processing:** Constructs a structured PySpark DataFrame and enriches records with UTC ingestion timestamps (`current_timestamp()`).
3. **Delta Lake Storage:** Appends structured records directly to a managed Delta Lake table (`lahore_weather_bronze`).
4. **Data Verification:** Queries time-series records using Spark SQL ordered by execution timestamps.

## Tech Stack
* **Platform:** Databricks (Serverless Compute)
* **Processing:** PySpark / Apache Spark
* **Storage:** Delta Lake
* **Language:** Python, Spark SQL
* **API:** OpenWeather API
