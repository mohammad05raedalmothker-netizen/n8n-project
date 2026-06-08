# n8n-project
# n8n Automation & AI Projects

Welcome to my portfolio of n8n workflows. Here, I showcase production-ready automations and AI integrations built to optimize business operations.

---

## 🚀 Project 1: AI Chatbot Agent for Computer Company (Dynamic Operations)

### 📋 Overview
An intelligent AI Agent built using n8n's advanced AI nodes. The chatbot acts as a smart assistant tailored for a computer company, capable of maintaining conversation context, querying company data from spreadsheets, and sending automated emails.

### 🧠 Core Architecture & Nodes Used
* **Trigger:** `When chat message received` (n8n Chat Trigger for UI-based client interaction).
* **AI Engine:** `AI Agent` node utilizing **OpenAI Chat Model** for reasoning, intent recognition, and decision making.
* **Context Management:** `Simple Memory` node to maintain session history and ensure a smooth user experience.
* **Tools (Function Calling):**
    * **Google Sheets Tool:** (`Get row(s) in sheet`) Used as a dynamic product catalog and inventory database, allowing the agent to fetch real-time details of available products, pricing, and specifications based on customer inquiries.
    * **Gmail Tool:** (`Send a message in Gmail`) Allows the agent to automatically draft and send professional follow-ups or confirmation emails to clients.

### 💡 Use Case Example
When a customer interacts with the chat and asks: *"Do you have core-i7 laptops in stock? If yes, please email me the pricing list."* The **AI Agent** processes the query, autonomously triggers the **Google Sheets Tool** to scan the inventory and fetch the details of available products, interprets the result, and then uses the **Gmail Tool** to send the exact pricing and specs directly to the customer's inbox.

### 🛠️ How to Import & Test
1. Download the file `computer company chatbot last version.json` from this repository.
2. Open your n8n instance.
3. Create a new workflow, click on the top-right menu, and select **Import from File**.
4. Configure your own OpenAI, Google Sheets, and Gmail credentials.

---

## 🚀 Project 2: NFC/Card-Based Student Reward & Attendance System

### 📋 Overview
An innovative automation workflow designed for educational environments. The system triggers instantly when a student taps their card (NFC) or scans a code using the teacher's smartphone, automatically validating the student's identity, updating their reward points, and logging the transaction in a central database.

### 🧠 Core Architecture & Nodes Used
* **Trigger:** `Webhook` node. Acts as a secure endpoint that listens to real-time HTTP POST requests sent from the teacher's mobile scanning app whenever a student's card is read.
* **Data Processing & Logic:** * `Set` / `Code` nodes (if any): Used to parse incoming student metadata (e.g., Student ID, Timestamp, and pre-defined points increment).
* **Database & CRM Integration:**
    * **Google Sheets Tool:** (`Update row` / `Append row`) Dynamically locates the specific student's record in the registry, increments their current point balance, and logs the activity history for administration tracking.

### 💡 Use Case Example
In a classroom, a student performs a positive action or attends a session. The teacher taps the student's NFC card with their phone. The phone app triggers the n8n **Webhook**. The workflow immediately captures the payload, identifies the student, adds (e.g., +5 points) to their profile in **Google Sheets**, and updates the school's live dashboard instantly.

### 🛠️ How to Import & Test
1. Download the file `student-attendance-points-system.json` (or your exact file name) from this repository.
2. Import it into your n8n instance using **Import from File**.
3. Copy the production **Webhook URL** from the trigger node and configure your trigger source (mobile application or HTTP client) to send payloads to it.
4. Link your own Google Sheets credentials.

---

## 🚀 Project 3: Omnichannel AI Student Assistant & Cost-Effective Payment Pipeline

### 📋 Overview
A multi-channel AI-powered system designed to handle student inquiries, track payment steps, and manage records autonomously. The system deploys an advanced AI Agent accessible via both a **Telegram Bot** and an **On-site Web Chat**, backed by a cost-effective data architecture to minimize production overhead.

### 🧠 Core Architecture & Nodes Used
* **Triggers (Multi-Channel):**
    * **Telegram Trigger:** Listens for real-time messages from students on Telegram.
    * **Webhook / Chat Trigger:** Handles incoming inquiries from the website’s live chat widget.
* **AI Engine & Context:** `AI Agent` utilizing **OpenAI Chat Model** combined with `Simple Memory` to retain conversation history across user interactions.
* **Cost-Optimized Database:**
    * **Google Sheets Tool:** Employed strategically as a serverless, highly scalable, and **zero-cost database solution** to query available courses, student payment tracking logs, and FAQ records without incurring expensive cloud database fees.

### 💡 Use Case & Business Value
1. **Automated Support:** A student asks either on Telegram or the website about their payment status or course details. The AI Agent fetches data directly from Google Sheets and replies instantly.
2. **Payment Tracking:** The system securely routes students through their payment milestones, logging each step in the spreadsheet.
3. **Cost Reduction:** By substituting traditional databases (like PostgreSQL or MongoDB) with Google Sheets, this architecture significantly minimizes API costs and maintenance efforts for small to medium enterprise (SME) owners.

### 🛠️ How to Import & Test
1. Download `student-payment-ai-assistant.json` from this repository.
2. Import it into your n8n instance.
3. Replace the placeholder credentials with your own Telegram Bot Token, OpenAI API Key, and Google Sheets access.
