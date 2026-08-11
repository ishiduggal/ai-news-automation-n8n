# 🤖 AI News Automation with n8n

> An automated AI-powered news intelligence pipeline that collects the latest AI news, evaluates and structures it using LLMs, stores the results in a database, and delivers formatted news updates through Telegram.

---

## 🚀 Project Overview

This project automates the complete process of discovering and delivering relevant AI news.

Instead of manually searching through dozens of articles every morning, the workflow automatically:

- Fetches the latest AI-related news
- Processes articles using an LLM
- Evaluates relevance, impact, freshness, source quality, and uniqueness
- Selects the strongest stories
- Converts the output into structured JSON
- Generates unique article IDs programmatically
- Stores selected articles in a database
- Sends formatted news to Telegram
- Runs automatically on a scheduled basis

---

## 🏗️ System Architecture

```text
Schedule Trigger
       ↓
NewsData.io API
       ↓
AI News Analysis
       ↓
News Database Formatter
       ↓
JavaScript Processing
       ↓
Split Articles
       ↓
News Database
       ↓
Telegram Delivery
📸 Project Screenshots
🔄 n8n Automation Workflow
📱 Telegram News Delivery
🗄️ News Database
🧠 AI News Evaluation
The AI evaluates candidate articles using multiple criteria:
Criterion	Purpose
Relevance	Determines whether the story is important to AI, technology, business, science, India or world affairs
Impact	Estimates potential effect on people, companies, industries, governments or technology
Freshness	Prioritizes recent and timely developments
Source Quality	Favors credible and established sources
Uniqueness	Helps avoid selecting essentially duplicate stories
The system then selects the 5 strongest stories for the daily digest.
⚙️ Workflow
1. Scheduled Trigger
The workflow starts automatically according to the configured schedule.
2. News Collection
NewsData.io provides the latest articles matching the configured AI-related query.
3. AI Processing
The LLM analyzes the collected articles and selects the most valuable stories.
4. Structured Data Extraction
A second LLM step converts the final news digest into structured JSON.
5. Article ID Generation
JavaScript generates an article ID using the article title and source.
6. Database Storage
Each selected article is stored as an individual record in the News History database.
7. Telegram Delivery
The processed news is automatically delivered through Telegram.
🛠️ Tech Stack
n8n — Workflow automation
NewsData.io — News API
Groq / Llama 3.3 70B — LLM processing
JavaScript — Data transformation and article ID generation
JSON — Structured data exchange
n8n Data Tables — News storage
Telegram Bot API — News delivery
📊 Data Stored
Each selected article is stored with structured fields including:
article_id
title
category
source
url
importance_score
published_at
📱 Telegram Output
The Telegram bot delivers structured news containing:
Article title
Category
Source
Importance score
Article link
Example:
📰 AI News
📂 Category: AI
📰 Source: News Source
⭐ Importance: 8/10
🔗 Read Full Article
🔐 Security
API keys, Telegram credentials, database credentials and other sensitive information are not included in the public repository.
Users should configure their own credentials when importing the workflow.
Never commit real API keys, bot tokens or passwords to a public repository.
🚀 Setup
Requirements
n8n
NewsData.io API key
Groq API credentials
Telegram Bot
Telegram Chat ID
Basic Setup
Import workflow/ai-news-automation.json into n8n.
Configure your NewsData.io API credentials.
Configure your Groq credentials.
Configure your Telegram credentials.
Configure the News History database.
Set your preferred schedule.
Activate the workflow.
📂 Repository Structure
ai-news-automation-n8n/
│
├── README.md
├── LICENSE
│
├── workflow/
│   └── ai-news-automation.json
│
├── docs/
│   └── screenshots/
│       ├── architecture.png
│       ├── telegram-output.png
│       └── database.png
│
└── examples/
📈 Future Improvements
Potential future improvements include:
Duplicate detection
Historical news analytics
Advanced article ranking
Source reliability scoring
News category dashboards
User-specific news preferences
Web dashboard
Email delivery
Semantic similarity for duplicate detection
👨‍💻 Author
Ishmeet Singh Duggal
AI & Data Science Student
Built as a real-world AI and workflow automation project combining APIs, LLMs, JavaScript, databases, and automated communication.

### STEP 3 — Important before committing

After pasting, **do not add or remove any ` ``` ` yourself.**

The code blocks inside the README are intentional:

- Architecture diagram → code block
- Repository structure → code block

But the screenshot section is **NOT** inside a code block.

Your screenshot lines should look exactly like:

```text
![n8n Automation Workflow](./docs/screenshots/architecture.png)
