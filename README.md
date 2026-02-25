# n8n-automations-ai-workflow-

## Project: Automated Google Sheets Integration
- *Objective:* Automated the creation and management of Google Spreadsheets using n8n and Google Cloud Platform.
- *Tech Stack:* n8n (Localhost), Google Cloud Console (OAuth 2.0), Google Sheets API, Google Drive API.
- *Key Achievements:*
    - Successfully implemented OAuth 2.0 authentication flow.
    - Resolved complex "403 Forbidden" errors related to API propagation.
    - Optimized workflow execution for a 4GB RAM / 128GB SSD hardware environment.
- *Troubleshooting:* Managed API enablement and credential refresh cycles to ensure stable connectivity.


## Project : Real-Time Crypto Data Extraction Pipeline
This is an automated ETL (Extract, Transform, Load) data pipeline. It fetches live Bitcoin (BTCUSDT) prices from the Binance REST API and dynamically logs them into a Google Sheet in real-time. 
## Tech Stack
* *Automation Engine:* n8n (Local Environment)
* *Data Source:* Binance Public API
* *Database:* Google Sheets (OAuth2 Integration)
## Key Achievements
* Eliminated manual data entry by building a fully hands-free data collection system.
* Successfully handled Google API Rate Limiting (HTTP 429 Error) by optimizing the data execution loop.
* Designed a clean, unidirectional data flow (Fetch ➡️ Process ➡️ Store) that runs seamlessly on minimal system resources.
### 1. n8n Automation Workflow
![n8n Workflow](workflow.jpeg.jpeg)

### 2. Live Data Populating in Google Sheets
![Google Sheets Output](sheets.jpeg.jpeg)
