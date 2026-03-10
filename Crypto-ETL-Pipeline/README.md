# 🚀 Autonomous Crypto ETL Pipeline with Global Fault Tolerance

## 📌 System Overview
A production-grade, fully automated ETL (Extract, Transform, Load) pipeline built on n8n. This system fetches real-time cryptocurrency data via the Binance API, processes the payload, and logs the structured data into Google Sheets. 

## 🏗️ Architecture: Two-Tier Fault Tolerance
Unlike basic automation scripts, this project implements an industry-standard *Zero-Downtime Architecture* designed for high reliability:
* *Tier 1 (Core Pipeline):* Scheduled autonomous execution for data extraction, transformation, and database loading.
* *Tier 2 (Global Error Handler):* A decoupled, dedicated workflow that acts as a system-wide watchdog.

## 📸 System Architecture

*1. Core ETL Pipeline (Data Extraction & Loading):*
![Main Workflow](main-workflow-screenshot.png)

*2. Global Error Handler (Fault Tolerance & Alerts):*
![Error Handler](error-handler-screenshot.png)  

## ⚙️ Key Capabilities
* *100% Autonomous Execution:* Runs on a scheduled trigger without manual developer intervention.
* *Global Error Routing:* Dynamically intercepts failures at any node across the workspace (e.g., API timeouts, rate limits, database authentication errors).
* *Real-time Telemetry:* Pushes critical failure alerts directly to Telegram, injecting exact node names and error payloads for instant debugging.

## 🛠️ Tech Stack
* *Automation Engine:* n8n (Node-based workflow automation)
* *APIs & Integrations:* Binance REST API, Google Sheets API, Telegram Bot API
* *Error Handling:* Global Error Trigger, Dynamic JSON mapping
