# 📈 AWS Stock Analytics – Real-Time Kafka Streaming Project

This project demonstrates a **real-time data streaming pipeline** using  
**Apache Kafka**, **Python**, and **AWS S3**.  
It simulates live stock market data and processes it end-to-end — from data generation to cloud storage.

Built as part of a learning project inspired by a YouTube tutorial, this repo organizes the entire workflow into a clean structure that is easy to run, modify, and extend.

---

## 🧠 Project Overview

This system consists of two main components:

### 🔹 **Producer**
- Reads a stock dataset (`indexProcessed.csv`)
- Picks random rows (simulating real-time stock ticks)
- Sends JSON messages to the Kafka topic `demo_test`

### 🔹 **Consumer**
- Listens to the Kafka topic
- Deserializes incoming JSON messages
- Uploads each record to an **AWS S3 bucket** as `stock_market_<count>.json`

Later, this S3 data can be queried using:
- 🧊 **AWS Glue**  
- 🔍 **AWS Athena**  
- 📊 **Power BI / QuickSight / Redshift**

---
