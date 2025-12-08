# Project 1: Retail Demand and Revenue Intelligence

## Overview

This project is part of my data science portfolio.  
It shows how I move from raw retail data to clear demand and revenue insight.  

The goal is simple.  
Understand what customers are buying, where they buy, and how revenue behaves over time.  

---

## Business questions

* Which products drive most revenue  
* How demand changes by day, store, and category  
* Which stores perform best  
* Where there are early warning signs for stock or demand issues  

---

## Data

Sample input tables

* Orders  
* Order items  
* Products  
* Stores  

Each table is small for learning but structured like a real retail system.  

---

## Architecture

High level flow

* Raw CSV files  
* Python ingestion into Postgres  
* Spark batch cleaning and aggregation  
* dbt models to build clean marts  
* Simple Scikit learn model for demand baseline  
* Optional Power BI or Tableau dashboard  

---

## Tools and stack

* Python  
* SQL  
* Pandas  
* Scikit learn  
* Postgres  
* Spark  
* dbt  
* Airflow placeholder  
* Docker for local platform  
* Power BI or Tableau for visualisation  

---

## How to run locally

This is the intended local run path.  
Exact commands may change as the project evolves.

1. Start the local platform  
   * Go to the `docker` folder  
   * Run your Docker compose command  

2. Load raw data into Postgres  
   * Run the ingestion script in `src/ingest`  

3. Run Spark batch transforms  
   * Use the scripts in the `spark` folder for raw to silver and silver to gold  

4. Build dbt models  
   * From the `dbt` folder, run your dbt build command with the Postgres profile  

5. Run the ML baseline  
   * Use the script in `src/ml` to train and generate a simple forecast  

6. Open your BI tool  
   * Connect to the mart tables for dashboards  

---

## Outputs

Planned outputs

* Gold level daily sales table  
* Clean dimensions for product and store  
* Simple seven day demand baseline forecast  
* Dashboard views for revenue and product performance  

---

## What this project proves

This project shows that I can

* Design a clear batch pipeline  
* Use Python, SQL, and Spark together  
* Apply dbt for clean and tested models  
* Build a small but honest ML baseline  
* Present results visually for non technical people  

This is one of the core projects in my data science portfolio that demonstrates end to end thinking from raw data to decision support.
