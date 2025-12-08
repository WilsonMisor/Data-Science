# Project 2: Real Time Fraud and Risk Signal Pipeline

## Overview

This project simulates a real time fraud and risk monitoring system.  
It is part of my data science portfolio and focuses on event style data.  

The idea is simple.  
Incoming transactions are turned into live features and simple risk signals that can support monitoring or alerting.  

---

## Business questions

* How many transactions each user makes in a short window  
* How payment amounts behave over time for each user  
* Which merchants or countries look risky based on volume and value patterns  
* Which summary signals can support fraud analysts  

---

## Data

There is no real payment data.  
I generate synthetic events that look like transaction records.

Each event includes

* Event identifier  
* User identifier  
* Merchant identifier  
* Amount and currency  
* Country  
* Event time  

---

## Architecture

High level flow

* Python event generator writes JSON files into a stream inbox folder  
* Spark Structured Streaming reads the inbox and builds bronze and silver layers  
* Five minute rolling features are computed per user  
* Features and events are stored in Postgres  
* dbt builds marts for risk monitoring  
* A nightly Scikit learn baseline model trains on recent data  
* Airflow DAG scaffolds nightly feature backfill and training  

This is a local simulation of a streaming style pipeline without external message brokers.  

---

## Tools and stack

* Python  
* SQL  
* Pandas  
* Scikit learn  
* Spark Structured Streaming  
* Postgres  
* dbt  
* Airflow placeholder  
* Docker  

---

## How to run locally

Expected flow

1. Start the local platform  
   * Use Docker compose as defined in the repo  

2. Start the streaming job  
   * Run the Spark streaming script in the `spark` folder  

3. Generate events  
   * Run the Python script in `src/event_generator`  
   * Confirm JSON files are created in the stream inbox folder  

4. Build dbt models  
   * From the `dbt` folder, run your dbt build command  

5. Train the nightly model  
   * Run the script in `src/ml` to train and create a simple risk report  

---

## Outputs

Planned outputs

* Bronze and silver level transaction tables  
* Five minute rolling feature table by user  
* Risk monitoring mart with summary metrics  
* Sample model report showing basic performance and thresholds  

---

## What this project proves

This project shows that I can

* Work with event style and time based data  
* Use Spark Structured Streaming for a simple simulation  
* Design rolling feature logic for risk and fraud questions  
* Combine dbt with a streaming pipeline  
* Build a basic ML training loop for nightly models  

It extends my data science portfolio beyond batch analytics into streaming style thinking and near real time decision support.
