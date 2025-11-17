# Building-A-New-MCP-Server-Use-Claude-LLM-Demo
# Weather Tools for Claude

A custom integration that provides Claude with real-time weather information through two specialized tools: `Get alerts` and `Get forecast`.

## Overview

This integration enables Claude to access current weather alerts and detailed forecasts for any location in California (and potentially other regions). The tools appear to be connected to the National Weather Service or similar weather data providers.

## Features

### 1. Get Alerts (`Get alerts`)
Retrieves active weather alerts and advisories for specified locations.

**Capabilities:**
- Fetches current weather warnings, watches, and advisories
- Provides severity levels (Minor, Moderate, Severe)
- Includes detailed descriptions of weather events
- Shows affected areas and time periods

**Example Response:**
- Flood Advisories
- Flash Flood Warnings
- High Wind Warnings
- Fire Weather Watches
- And other NWS alerts

### 2. Get Forecast (`Get forecast`)
Provides detailed weather forecasts for specific coordinates.

**Capabilities:**
- Multi-period forecasts (5-period forecast shown in example)
- Temperature predictions
- Wind speed and direction
- Precipitation chances and amounts
- Cloud cover and general conditions
- Overnight and daytime forecasts

**Example Output:**
```
Overnight:
Temperature: 54°F
Wind: 5 mph ESE
Forecast: A chance of rain. Mostly cloudy, with a low around 54.
Chance of precipitation is 30%. New rainfall amounts less than a tenth of an inch possible.
```

## Usage

### Enabling the Tools

1. Open the tools menu in Claude (search icon)
2. Locate "Get alerts" and "Get forecast" under weather tools
3. Toggle both tools to enabled (blue)
4. The tools will now be available for Claude to use automatically

### Example Queries

**For Weather Alerts:**
- "What are the active weather alerts in California right now?"
- "Are there any flood warnings in the Bay Area?"
- "Show me current weather advisories for Los Angeles"

**For Weather Forecasts:**
- "Get the next 5-period forecast for 34.0522, -118.2437" (Los Angeles)
- "What's the weather forecast for San Francisco?"
- "Will it rain in Sacramento tonight?"

## Technical Details

### Input Format

**Get Alerts:**
- Accepts location queries (city, county, or state)
- Returns structured data with event type, area, severity, and description

**Get Forecast:**
- Accepts coordinates (latitude, longitude)
- Returns multi-period forecast data with temperature, wind, and precipitation details

### Response Structure

Both tools return structured data that Claude can parse and present in a user-friendly format, including:
- Temperature readings
- Wind information
- Precipitation chances
- Alert severity levels
- Time periods and durations

## Integration Notes

- Tools are accessed through Claude's function calling interface
- Responses are automatically formatted for readability
- Data appears to be real-time or near-real-time
- Geographic coverage shown includes California (may extend to other regions)

## Privacy & Data

- No API keys are required from the user
- Location data is only used for weather queries
- All data is sourced from public weather services

## Outputs
![image3](https://github.com/user-attachments/assets/8a9be5ab-7ace-43db-a40e-07dd76707556)
![image 2](https://github.com/user-attachments/assets/b34dceab-f9f3-470b-9352-c1836d68ed26)
![image 1](https://github.com/user-attachments/assets/e57365a1-61d0-49d8-af6e-c7c4069e5221)




*Last Updated: November 17, 2025*

