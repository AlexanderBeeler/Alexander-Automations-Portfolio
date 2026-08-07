# Riot Patch Notes Notifier

## Problem

Gamers want to receive patch notes as soon as they are published without repeatedly checking official sources.

## Solution

This Make automation monitors an RSS feed for new Riot Games patch notes. When a new patch is detected, it sends a Discord notification with the update and direct link while also logging the announcement to Google Sheets.

## Services Used

- Make
- RSS
- Discord
- Google Sheets

## Skills Demonstrated

- RSS integration
- Content filtering
- Dynamic data mapping
- Google Sheets logging
- Discord notifications

## Workflow

RSS Feed → Make → Discord → Google Sheets

## Screenshots

### Make Scenario

![Make Scenario](images/Riot%20Patch%20Notes%20Scenario.png)

### Google Sheets Output

![Google Sheets Output](images/Riot%20Patch%20Notes%20Sheets.png)

### Discord Output

 **Note**

 This workflow was developed and successfully tested using an RSS provider's free trial. The trial expired before the portfolio was finalized, so a current Discord notification screenshot is unavailable. The Make scenario and Google Sheets output demonstrate the workflow.



