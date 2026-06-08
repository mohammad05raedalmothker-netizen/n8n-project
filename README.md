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
