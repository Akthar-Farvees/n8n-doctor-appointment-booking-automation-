# 🏥 Doctor Appointment Booking Automation (n8n)

An end-to-end workflow automation system built using **n8n** to streamline doctor appointment booking, payment processing, and real-time notifications via **WhatsApp**, **Google Sheets**, and **Stripe**.

This project demonstrates practical implementation of event-driven architecture, API integrations, and workflow orchestration.

---

## 📌 Overview

This system automates the complete lifecycle of a doctor appointment:

1. User submits appointment request  
2. Request is validated and processed  
3. Payment link is generated via Stripe  
4. User completes payment  
5. Appointment is confirmed  
6. Notification is sent via WhatsApp  
7. Data is stored in Google Sheets  

---

## 🚀 Features

- Fully automated appointment booking workflow  
- Secure payment integration using Stripe  
- Real-time WhatsApp notifications  
- Centralized data tracking with Google Sheets  
- Webhook-based trigger system  
- Scalable and modular workflow design  

---

## 🧰 Tech Stack

- **n8n** – Workflow automation engine  
- **WhatsApp API** – Messaging and notifications  
- **Google Sheets API** – Data storage  
- **Stripe API** – Payment processing  
- **Webhooks** – Event-driven triggers  

---

## 🔄 Workflow Architecture
User Request
↓
Webhook Trigger
↓
Data Validation
↓
Stripe Payment Link
↓
Payment Confirmation (Webhook)
↓
Google Sheets Update
↓
WhatsApp Notification
↓
Appointment Confirmed


---

## 🧩 Workflow Breakdown

### 1. Trigger Layer
- Receives user input via webhook or form  
- Captures user details and appointment information  

### 2. Processing Layer
- Validates input data  
- Generates appointment ID and timestamp  

### 3. Payment Layer
- Creates Stripe payment session  
- Generates payment link  
- Handles payment confirmation via webhook  

### 4. Data Layer
- Stores appointment records in Google Sheets  
- Tracks status: Pending, Paid, Confirmed  

### 5. Notification Layer
- Sends confirmation message via WhatsApp  
- Notifies admin or doctor  

---

## 📂 Project Structure
project-root/
│
├── workflows/
│ └── doctor-appointment.json
│
├── docs/
│ └── architecture.png
│
├── config/
│ └── environment.md
│
└── README.md

---

## ⚙️ Setup Instructions

### 1. Install n8n
```bash
npm install -g n8n

n8n start