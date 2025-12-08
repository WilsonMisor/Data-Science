# Project 3: Modern Analytics Engineering Showcase

## Overview

This project is a focused analytics engineering example inside my data science portfolio.  
It shows how I use dbt and SQL to turn raw tables into clean, tested, and documented marts that are ready for dashboards.  

There is no complex ML here on purpose.  
The goal is clarity, reliability, and a strong semantic layer.  

---

## Business questions

The models focus on three ideas

* Sales trends by product, channel, and date  
* Marketing spend and effectiveness by platform and period  
* Support activity and resolution outcomes by customer and issue type  

---

## Data

Sample data sets

* Sales table with transaction level data  
* Marketing table with campaign level spend  
* Support table with tickets, priorities, and resolution dates  

These are small but structured to feel similar to real business tables.  

---

## Architecture

High level flow

* Raw CSV files in a data folder  
* Python ingestion script loads them into Postgres  
* dbt staging models apply naming, typing, and light cleaning  
* dbt intermediate models join and enrich across domains  
* dbt marts expose clean tables for dashboards and self service queries  
* Optional Airflow DAG schedules regular dbt builds  

The same pattern can later point to a cloud warehouse such as BigQuery or Snowflake.  

---

## Tools and stack

* SQL  
* dbt  
* Python and Pandas for simple ingestion  
* Postgres as local warehouse  
* Docker for local environment  
* Airflow placeholder  
* Power BI or Tableau for reporting  

---

## How to run locally

1. Start the local platform  
   * Use Docker compose from the `docker` folder  

2. Load raw data  
   * Run the Python ingestion script in `src/ingest`  

3. Build dbt models  
   * From the `dbt` folder, run your dbt build command with the local profile  

4. Explore results  
   * Connect your BI tool or SQL client to the mart schema  

---

## Outputs

Planned dbt marts

* Revenue and volume by product and channel  
* Marketing spend and simple efficiency ratios  
* Support ticket resolution metrics and basic service indicators  

Each model includes tests and descriptions to make the logic easy to trust and reuse.  

---

## What this project proves

This project shows that I can

* Design a clear layered model structure with dbt  
* Write readable SQL that others can maintain  
* Add basic testing and documentation around data models  
* Support BI and self service analysis with a strong semantic layer  

It anchors the analytics engineering side of my data science portfolio and complements the batch and streaming projects with a clean, warehouse first design.
