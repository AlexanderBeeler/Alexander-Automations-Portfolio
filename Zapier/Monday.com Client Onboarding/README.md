# Monday.com Client Onboarding Automation

## Overview

An automated client onboarding workflow that connects **Monday.com, Google Drive, Google Docs, Discord, and Google Sheets**.

The workflow checks whether a client already exists in Monday.com using their email. If the client is new, it creates a Monday.com item. Both new and existing clients then go through the onboarding process.

The automation:

* Checks Monday.com for an existing client
* Creates a Monday.com item for new clients
* Creates a dedicated Google Drive folder
* Creates a Welcome Document
* Updates the Monday.com item with the folder and document links
* Sends a Discord notification with the client's name and links
* Logs the client information and timestamp in Google Sheets

## Workflow

**[!Zapier Workflow](./images/)**

```text
Client Information
        ↓
Search Monday.com by Email
        ↓
   Client Exists?
     ↙       ↘
   No         Yes
   ↓           ↓
Create Item    │
     ↘        ↙
       ↓
Create Drive Folder
       ↓
Create Welcome Doc
       ↓
Update Monday.com
       ↓
Discord Notification
       ↓
Google Sheets Log
```

## Tools Used

* Monday.com
* Google Drive
* Google Docs
* Google Sheets
* Discord
* Webhooks / API integrations
* Conditional logic

## Screenshots

### Monday.com

**[!]**

### Google Drive

**[!]**

### Welcome Document

**[!]**

### Discord Notification

**[!]**

### Google Sheets Log

**[!]**

## Workflow

**[!]**

