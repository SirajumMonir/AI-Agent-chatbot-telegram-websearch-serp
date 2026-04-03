## 🚀 Day 11: Real-World Lead Generation & API Troubleshooting

### 📌 Project Overview
Upgraded the AI Agent into a functional Lead Generation Machine. The goal was to perform reverse phone lookups and extract targeted US business details (Owner Name, Address, Contact Info) autonomously from the web.

### ⚙️ Architecture Pivot
* **Initial Plan (Google Custom Search API):** Successfully generated API Keys and CX ID. However, discovered that Google recently deprecated the "Search the entire web" feature for new configurations, severely limiting the bot's data-mining capabilities.
* **The Pivot (SerpAPI):** Rapidly adapted the architecture by replacing the Google tool with SerpAPI. 

### 🧠 System Prompt Engineering
Engineered a highly specific system prompt to guide the LLM:
*"You are an expert Lead Generation Specialist... When the user gives you a business name or a phone number, YOU MUST use the SerpAPI tool to search the web and extract: 1. Business Name, 2. Owner Name, 3. Full Address (including geographic area), 4. Other Contact Info. Output in a professional bulleted list."*

### 🎯 Result
The Telegram bot now successfully receives a phone number, autonomously queries SerpAPI, bypasses hallucinations, and returns a verified, formatted lead profile in real-time. Also resolved a dynamic Webhook URL issue (`invalid webhook URL specified`) by resetting the Ngrok tunnel and refreshing the n8n environment variables.
