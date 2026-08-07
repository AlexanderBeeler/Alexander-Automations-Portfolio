# HTTP Programming Joke Bot

## Problem

Demonstrate how external APIs can be integrated into an automation workflow while handling multiple response formats.

## Solution

This Make automation retrieves programming jokes from JokeAPI using an HTTP request. A router separates single-part jokes from two-part jokes, formats the response appropriately, sends the joke to Discord, and logs it to Google Sheets.

## Services Used

- Make
- HTTP
- Router
- Discord
- Google Sheets

## Skills Demonstrated

- HTTP API integration
- JSON parsing
- Router logic
- Conditional branching
- Dynamic data mapping
- Google Sheets integration
- Discord notifications

## Workflow

HTTP Request → Router → Discord → Google Sheets

## Screenshots

### Make Scenario

![Make Scenario](images/HTTP%20API%20Scenario.png)

### Discord Output

![Discord Output](images/HTTP%20API%20Single%20line%20joke.png)
![Discord Output](images/HTTP%20API%20Discord%20Double%20line%20joke.png)

### Google Sheets Output

![Google Sheets Output](images/HTTP%20API%20Sheets%20Single%20line%20and%20Double%20line%20jokes.png)
