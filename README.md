# 🤖 AI News Automation with n8n

An automated AI-powered news intelligence pipeline built with n8n.

The system collects news, processes and structures it using AI, stores the results in a database, and automatically delivers formatted news updates through Telegram.

## 🚀 Features

- Automated news collection
- AI-powered news processing
- Structured JSON generation
- Automatic article ID generation
- Individual article processing
- Database storage
- Automated Telegram delivery
- Scheduled execution
- HTML-formatted Telegram messages

## 🏗️ Architecture

```text
Schedule Trigger
       ↓
   News Source
       ↓
   AI Processing
       ↓
 JSON Parser / Code
       ↓
    Split Out
       ↓
 Database Storage
       ↓
 Telegram Delivery
