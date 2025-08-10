# CASE STUDY: Build a Real-Time Dashboard using Apache Kafka, Spark, Node.js & HighCharts

<p align="center">
  <img width="600" height="600" alt="Building a Real Time Dashboard using Apache Kafka, Spark, NodeJS and HighCharts" src="https://github.com/user-attachments/assets/d5357ce6-acfd-4e31-be9d-79f0022fc226" />
</p>


**Author:** Mohamed El Hassnaoui  
**Tech Stack:** Apache Kafka → Apache Spark Streaming → Kafka (processed topic) → Node.js (Socket.io) → HighCharts (browser)  
**Use Case:** Real-time visualization of *orders* data ingested from CSV files, processed in near real-time, and displayed in a live dashboard.

---

## 📌 Overview

This project showcases the design and implementation of a **real-time analytics dashboard** built on a distributed streaming architecture:

1. **Ingest** — Load orders CSV data into Kafka (`orders_data` topic).  
2. **Stream Process** — Use Spark Streaming to compute aggregated metrics every 10 seconds and publish to Kafka (`orders_ten_sec_data`).  
3. **Serve** — Broadcast processed metrics to connected web clients via Node.js (`kafka-node` + `socket.io`).  
4. **Visualize** — Render live updates in an interactive HighCharts dashboard.

The solution runs on an **EMR cluster** and can be adapted to local or cloud-based deployments.

---

## ⚙️ EMR Cluster (Example Setup)

- **EMR version:** `emr-4.9.4`  
- **Requirements:**  
  - Spark with `pyspark` support  
  - Kafka brokers accessible from the cluster  
  - Python dependencies installed on EMR nodes

📂 Repository Layout

```plaintext
spark-project/
├─ spark_dashboard/
│  ├─ kafka/
│  │  ├─ push_orders_data_in_topic.sh
│  │  └─ data/                # sample CSV orders data
│  ├─ spark/
│  │  └─ spark_streaming_order_status.py
│  └─ nodejs/
│     ├─ index.js
│     └─ index.html           # frontend with HighCharts
##-----

## Introduction

This project demonstrates a complete **real-time data processing and visualization pipeline** using **Apache Kafka**, **Apache Spark Streaming**, **Node.js**, and **HighCharts**.  
The goal is to simulate and process incoming **orders data** in near real-time, apply stream-based aggregation, and present the processed insights through a **dynamic, interactive dashboard**.

### Data Flow
1. **Kafka** — Ingests raw CSV order data into a distributed streaming platform.
2. **Spark Streaming** — Consumes data from Kafka, processes it in **10-second micro-batches**, and publishes aggregated results back to Kafka.
3. **Node.js + Socket.io** — Consumes processed messages and streams them to the frontend via WebSockets.
4. **HighCharts** — Renders the live updates into rich, interactive charts for instant visualization.

This architecture closely resembles production-grade streaming solutions used in **e-commerce, finance, IoT, and logistics**.

---

## Summary

Through this project, you will:

- Install and configure **Apache Kafka** to handle streaming order data.
- Develop a **Spark Streaming job** to aggregate order statuses in real-time.
- Build a **Node.js + Socket.io** server to broadcast updates to clients.
- Create a **HighCharts-powered dashboard** that updates live as new data arrives.
- Deploy the entire pipeline on an **EMR cluster** (or equivalent setup).

**Key Skills Demonstrated:**
- Designing and integrating distributed systems.
- Real-time data processing with **Spark Streaming**.
- Event-driven web development using **WebSockets**.
- Building production-ready dashboards for actionable insights.
- Troubleshooting distributed system issues in clustered environments.

---

## Why This Project Is Useful

- **Practical Mastery:** Demonstrates hands-on experience with modern big data and streaming tools.
- **Real-World Relevance:** Mirrors use cases like live analytics dashboards, fraud detection, and IoT monitoring.
- **Full-Stack Capability:** Covers backend ingestion, real-time processing, and frontend visualization.
- **Portfolio-Ready:** Ideal for interviews, technical demonstrations, and showcasing engineering skills to employers.
- **Performance-Focused:** Provides insight into handling latency, throughput, and fault tolerance in real-time architectures.


