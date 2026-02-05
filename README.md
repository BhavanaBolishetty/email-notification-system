# Gmail to WhatsApp Notification Service 

A Python-based automation tool that monitors unread Gmail emails and sends instant WhatsApp notifications using Twilio.  
The system avoids duplicate alerts, marks emails as processed, and runs continuously in the background.

This project demonstrates real-world backend integration using third-party APIs, OAuth authentication, and automation workflows.

---

## Features

- Gmail OAuth 2.0 authentication
- Fetches unread emails from Inbox
- Sends real-time WhatsApp alerts
- Marks emails as read after notification
- Prevents duplicate notifications
- Handles Twilio API rate limits
- Retry mechanism with error handling
- Background scheduler with logging

---

## Tech Stack

- Python 3
- Gmail API
- Twilio WhatsApp API
- OAuth 2.0
- REST APIs

---

## Project Structure

```

Gmail-notification-whatsapp/
│
├── email_to_whatsapp.py
├── requirements.txt
├── README.md
├── .gitignore
├── package-lock.json  
├── credentials.json        (not pushed to GitHub)
└── token.json              (not pushed to GitHub)

```

---

## Gmail API Permissions

This project uses the following Gmail scope:

- https://www.googleapis.com/auth/gmail.modify

This allows the application to:
- Read unread emails
- Mark emails as read to prevent duplicate alerts

---

## Setup Instructions

### 1. Clone Repository

git clone https://github.com/BhavanaBolishetty/email-notification-system.git

cd Gmail-notification-whatsapp

---

### 2. Install Dependencies

pip install -r requirements.txt


---

### 3. Google Gmail API Setup
1. Create a project in Google Cloud Console
2. Enable Gmail API
3. Create OAuth credentials
4. Download credentials.json
5. Place credentials.json in the project root directory

---

### 4. Twilio WhatsApp Configuration

Create environment variables:

TWILIO_ACCOUNT_SID=your_account_sid

TWILIO_AUTH_TOKEN=your_auth_token

TWILIO_WHATSAPP_NUMBER=whatsapp:+14155238886

TO_WHATSAPP_NUMBER=whatsapp:+91XXXXXXXXXX

---

### 5. Run the Application

python email_to_whatsapp.py


On first run, a browser window will open for Gmail authorization.

---










