# Stripe Payment Automation

## Problem

Businesses often spend time manually tracking subscription payments, identifying failed transactions, and notifying customers. Automating these processes improves response times and reduces administrative work.

---

## Solution

This automation monitors Stripe payment events, routes successful, failed, and voided payments through separate workflows, logs activity in Google Sheets, notifies the team through Discord, and sends customer emails for successful and failed payments.

---

## Workflow

Stripe → Make → Router

Payment Successful
- Google Sheets
- Gmail
- Discord

Payment Failed
- Google Sheets
- Gmail
- Discord

Payment Voided
- Google Sheets
- Discord

---

## Services Used

- Make.com
- Stripe
- Google Sheets
- Gmail
- Discord
- Router

---

## Skills Demonstrated

- Stripe Integration
- Event-Based Automation
- Router Logic
- Business Process Automation
- Payment Monitoring
- Customer Notifications
- Google Workspace Integration

---

## Screenshots

### Workflow

![Workflow](images/Stripe%20Payment%20Scenario.png)

### Google Sheets Output

![Google Sheets](images/Stripe%20Payment%20Sheets.png)

### Discord Notification

![Discord](images/Stripe%20Payment%20Discord.png)

### Success Email

![Success Email](images/Stripe%20Payment%20Success.png)

### Failed Payment Email

![Failed Email](images/Stripe%20Payment%20Fail.png)
