Project 3: Omnichannel AI Student Assistant & Cost-Effective Payment Pipeline

📋 Overview

A multi-channel AI-powered system designed to handle student inquiries, track payment steps, and manage records autonomously. The system deploys an advanced AI Agent accessible via both a Telegram Bot and an On-site Web Chat, backed by a cost-effective data architecture to minimize production overhead.

🧠 Core Architecture & Nodes Used

Triggers (Multi-Channel):
Telegram Trigger: Listens for real-time messages from students on Telegram.
Webhook / Chat Trigger: Handles incoming inquiries from the website’s live chat widget.
AI Engine & Context: AI Agent utilizing OpenAI Chat Model combined with Simple Memory to retain conversation history across user interactions.
Cost-Optimized Database:
Google Sheets Tool: Employed strategically as a serverless, highly scalable, and zero-cost database solution to query available courses, student payment tracking logs, and FAQ records without incurring expensive cloud database fees.
💡 Use Case & Business Value

Automated Support: A student asks either on Telegram or the website about their payment status or course details. The AI Agent fetches data directly from Google Sheets and replies instantly.
Payment Tracking: The system securely routes students through their payment milestones, logging each step in the spreadsheet.
Cost Reduction: By substituting traditional databases (like PostgreSQL or MongoDB) with Google Sheets, this architecture significantly minimizes API costs and maintenance efforts for small to medium enterprise (SME) owners.
🛠️ How to Import & Test

Download student-payment-ai-assistant.json from this repository.
Import it into your n8n instance.
Replace the placeholder credentials with your own Telegram Bot Token, OpenAI API Key, and Google Sheets access.

