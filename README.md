# Building a Real Time Dashboard using Apache Kafka, Spark, NodeJS and HighCharts

<img width="1000" height="1000" alt="Building a Real Time Dashboard using Apache Kafka, Spark, NodeJS and HighCharts" src="https://github.com/user-attachments/assets/d5357ce6-acfd-4e31-be9d-79f0022fc226" />

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


