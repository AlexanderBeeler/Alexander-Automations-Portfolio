# Cold Email Agency Automation

## Overview

A two-part lead processing and reporting automation designed for cold email campaigns.

The first workflow receives lead information, checks for duplicate email addresses, uses AI to analyze qualified leads, stores the processed information, assigns the lead to a campaign, and sends Discord notifications.

The second workflow runs automatically at **5:00 PM each day**, gathers the day's campaign data, generates a report using JavaScript, and sends the daily results to Discord.

## Part 1 — Lead Processing

### Workflow

**[!Cold Email Agency Workflow 1]**

```text id="0q5z1m"
Lead Information
       ↓
Check Email Against Sheet
       ↓
   Duplicate?
    ↙      ↘
  Yes       No
   ↓         ↓
Discord     AI Analysis
Alert          ↓
           Extract:
        • Summary
        • Urgency
        • Industry
        • Opening Line
              ↓
        Store Lead Data
              ↓
       Add Lead to Campaign
              ↓
        Discord Alert
              ↓
       Store Campaign Data
```

### Lead Information

The workflow receives:

* Name
* Email
* Company
* Website
* Industry
* Employee Count
* Country
* Campaign Source

### Duplicate Detection

Before processing a lead, the workflow checks a Google Sheet for the lead's email address.

If the email already exists, the lead is rejected and a Discord alert is sent indicating that a duplicate email was found.

If the email is not found, the lead continues through the workflow.

### AI Lead Analysis

Qualified leads are sent through an AI processing step that generates:

* Lead Summary
* Urgency
* Industry
* Personalized Opening Line

The processed information is then stored for campaign use.

### Campaign Processing

The workflow stores:

* Name
* Email
* Company
* Website
* Industry
* Urgency
* Summary
* Opening Line

The lead is then added to the appropriate campaign.

A Discord notification confirms the lead was added and provides a brief summary.

A second Google Sheet stores:

* Timestamp
* Email
* Campaign
* Urgency

**[!]**

**[!]**

**[!]**

---

# Part 2 — Daily Campaign Report

The second workflow runs automatically at **5:00 PM every day**.

It retrieves the campaign information stored throughout the day and uses JavaScript to process the data into a daily report.

The completed report is then sent to Discord.

```text id="9h2v3c"
5:00 PM Schedule
       ↓
Retrieve Campaign Data
       ↓
JavaScript Processing
       ↓
Generate Daily Report
       ↓
Discord
```

**[!]**

### Daily Report

The Discord report provides a summary of the day's campaign activity and lead information.

This allows campaign activity to be reviewed without manually checking the underlying spreadsheets.

---

## Tools Used

* Google Sheets
* Discord
* AI processing
* JavaScript
* Scheduled automation
* Conditional logic
* Data filtering
* Data mapping

## Key Automation Features

* Duplicate lead detection
* AI-powered lead analysis
* Automated campaign assignment
* Lead data organization
* Real-time Discord notifications
* Scheduled daily reporting
* JavaScript data processing
* Centralized Google Sheets storage

## Workflow

**[!]**
