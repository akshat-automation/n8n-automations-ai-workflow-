
# Autonomous Market Intelligence System (V2)

An advanced multi-agent n8n pipeline designed to track crypto market volatility, autonomously research fundamental catalysts via the live web, and deliver high-signal alerts via Telegram.


## 📸 Screenshots

### 1. The n8n Workflow Canvas
![Workflow Canvas](workfloww.png)

### 2. The Final Telegram Output
![Telegram Output](telegrameg.jpeg)


## V2 Architecture (The Agentic Upgrades)

This version transitions from a static data pipeline to an *Autonomous Agentic Workflow* by injecting external tools into the LLM's logic loop:

1.  *Data Ingestion & Filtering:* Fetches real-time price data from the CoinGecko API and strictly filters out market noise (drops any asset moving less than 3%).
2.  *Agent 1: The Quant Analyst (gemini-3-flash):*
    * *Role:* Mathematical Analysis & Autonomous Research.
    * *Execution:* Calculates market breadth to find the top performer. Once identified, it *autonomously triggers a SerpAPI web search* to find the live news or protocol upgrade causing the pump.
3.  *Agent 2: The Comm Manager (gemini-3-flash):*
    * *Role:* Formatting & Persona Engine.
    * *Execution:* Takes the raw math and news data from Agent 1 and structures it into a high-status, Wall Street-grade alert.
4.  *Delivery:* Sent directly via the Telegram Bot API.

## 💻 Tech Stack

* *Orchestration:* n8n (Self-hosted/Local)
* *AI Models:* Google Gemini 3 Flash 
* *Tooling:* SerpAPI (For live Google Search execution)
* *Data Source:* CoinGecko Public API

## Developer Notes (V2 Learnings)
* *Prompt Engineering for Tools:* Learned that AI requires strict sequential commands to use tools effectively (e.g., "Analyze JSON first, then search the web for the reason").
* *Chain-of-Thought:* Implemented a system where the AI correlates numerical data with external real-world events without human intervention.
