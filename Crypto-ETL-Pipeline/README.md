# 🚀 Autonomous Intelligence Crypto ETL Pipeline & Smart Alert System 

## 📌 Project Overview
This project is an automated ETL (Extract, Transform, Load) data pipeline built using *n8n*. It acts as an autonomous tracking system that fetches real-time cryptocurrency data, maintains a historical database, and triggers smart alerts based on dynamic conditional logic.

Instead of spamming notifications, the system is designed to analyze data efficiently and only alerts the user when specific, pre-defined market conditions are met (e.g., a significant price drop).

## 🛠️ Tech Stack & Integrations
* *Workflow Engine:* n8n 
* *Data Source (API):* Binance Public API (REST) 
* *Database:* Google Sheets API (Easily swappable with SQL/NoSQL databases)
* *Notification System:* Telegram Bot API
* *Data Processing:* JSON mapping, Array manipulation, Data sorting & limiting

## 🧠 The ETL Architecture & Logic
1. *Extract (E):* A customizable Cron-based Schedule Trigger calls the Binance API for live prices while simultaneously retrieving the latest historical price from the database.
2. *Transform (T):* Data is filtered using a strictly defined Limit node to isolate only the absolute latest historical record. The fresh API data and the historical database record are merged side-by-side. An IF node then evaluates the condition (e.g., New Price < Old Price).
3. *Load (L):* Every fetched price is automatically appended to the database for continuous historical tracking. If the IF condition evaluates to True, a dynamically formatted payload is sent to the integrated messaging platform.

## 💡 Key Features & Problem Solving
* *Flow Logic Optimization:* Ensures strict adherence to conditional logic, preventing data bypass and eliminating false positive alerts.
* *Redundancy Elimination:* Streamlined the workflow by using precise data limiters, ensuring a clean, single-source-of-truth data flow.
* *Parallel Execution:* Implemented parallel routing to update the database and evaluate alert logic simultaneously, significantly reducing execution time. 
