Project 2: NFC/Card-Based Student Reward & Attendance System

📋 Overview

An innovative automation workflow designed for educational environments. The system triggers instantly when a student taps their card (NFC) or scans a code using the teacher's smartphone, automatically validating the student's identity, updating their reward points, and logging the transaction in a central database.

🧠 Core Architecture & Nodes Used

Trigger: Webhook node. Acts as a secure endpoint that listens to real-time HTTP POST requests sent from the teacher's mobile scanning app whenever a student's card is read.
Data Processing & Logic: * Set / Code nodes (if any): Used to parse incoming student metadata (e.g., Student ID, Timestamp, and pre-defined points increment).
Database & CRM Integration:
Google Sheets Tool: (Update row / Append row) Dynamically locates the specific student's record in the registry, increments their current point balance, and logs the activity history for administration tracking.
💡 Use Case Example

In a classroom, a student performs a positive action or attends a session. The teacher taps the student's NFC card with their phone. The phone app triggers the n8n Webhook. The workflow immediately captures the payload, identifies the student, adds (e.g., +5 points) to their profile in Google Sheets, and updates the school's live dashboard instantly.

🛠️ How to Import & Test

Download the file student-attendance-points-system.json (or your exact file name) from this repository.
Import it into your n8n instance using Import from File.
Copy the production Webhook URL from the trigger node and configure your trigger source (mobile application or HTTP client) to send payloads to it.
Link your own Google Sheets credentials.
