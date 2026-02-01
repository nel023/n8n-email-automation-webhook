# n8n Email Automation via Webhook


## Overview

This project is a webhook-based email automation built using **n8n**.  

It accepts incoming HTTP requests, evaluates request priority, sends an email notification, and returns a structured JSON response. 

This workflow demonstrates real-world automation patterns commonly used in IT support, DevOps, and workflow engineering.

---

## Features

- Webhook-triggered automation
- Conditional logic based on request priority
- Dynamic email subject and body
- SMTP email integration
- Structured JSON API response
- Timestamped execution result

---


## Tech Stack

- n8n (self-hosted via Docker)
- SMTP (Gmail App Password)
- Postman (for API testing)

---

## How It Works

1. A POST request is sent to the webhook endpoint
2. The workflow evaluates the request priority
3. An email is sent with dynamic content
4. The webhook responds with execution status

---

## 📥 Sample Request (POST)

```json
{
"requester_name": "Jane Doe",
"request_email": "jane@example.com",
"request_subject": "VPN Access Issue",
"request_message": "Unable to connect to VPN",
"priority": "high"
}
```

---

## Sample Response 

```json
{
"status": "success",
"priority": "high",
"message": "Email sent successfully",
"timestamp": "2026-02-01T08:14:29.445-05:00"
}
```

---

## Workflow Diagram

![Workflow](/screenshots/workflow.png)

---

## How to Use

1. Import the JSON file into n8n
2. Configure SMTP credentials
3. Activate the workflow
4. Send requests via Postman or any HTTP client

---

## Use Cases

1. IT support ticket notifications
2. Contact form email automation
3. Internal alerting systems
4. API-based workflow automation

---

## Author

Built by an EUC Engineer upskilling in automation and AI-driven workflows.
