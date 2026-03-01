This README.md is designed to showcase your ability to handle complex API data, multi-channel notifications (Gmail + Telegram), and professional data formatting. It is perfect for your portfolio or MagentIQ application.

🌦️ Multi-Channel Weather Monitoring System
An automated workflow built with n8n that fetches real-time weather data for Manila/Pasig City and distributes comprehensive, human-readable reports across both Email (Gmail) and Instant Messaging (Telegram).

🚀 Overview
This project demonstrates a production-ready automation pipeline that handles everything from API authentication to complex data transformation and multi-node distribution.

🛠️ Core Features
Automated Scheduling: Triggers every 3 hours to ensure data is always fresh.

Live Weather Integration: Fetches real-time metrics (Temp, Humidity, Pressure, Wind) from the OpenWeatherMap API.

Multi-Channel Delivery: Simultaneously sends formatted HTML reports via Gmail and plain-text summaries via Telegram.

Advanced Data Formatting:

Converts Kelvin/Metric data into professional Celsius displays.

Transforms Unix Timestamps into human-readable clock times (AM/PM) for Sunrise/Sunset.

Organizes technical JSON payloads into structured sections (Location, Measurements, Wind, Metadata).

🏗️ Workflow Architecture
Schedule Trigger: Initiates the flow every 3 hours.

HTTP Request: Calls OpenWeatherMap API with predefined credentials for Pasig City, Philippines.

Gmail Node: Formats the JSON response into a professional HTML email with bold headers and lists.

Telegram Node: Parallel branch that pushes a condensed text version of the data to a private chat/bot.

📄 Data Points Captured
This workflow extracts and processes the following "Up and Down" data:

Coordinates: Precise Lat/Lon for Pasig City.

Atmospherics: Humidity, Sea Level Pressure, Ground Level Pressure, and Visibility.

Temperature: Current, "Feels Like," and Min/Max daily ranges.

Astronomy: Real-time conversion of Sunrise and Sunset times.

Wind: Speed and Directional Degrees.

🔧 Technical Setup
Platform: n8n

API: OpenWeatherMap (Metric Units)

Credentials:

OpenWeatherMap API Key

Gmail OAuth2

Telegram Bot Token

Expressions: Utilizes JavaScript new Date() objects and .toLocaleTimeString() for professional data rendering.

📂 How to Use
Copy the JSON code from the Weather-Workflow.json file.

Import into your n8n instance.

Update the Gmail and Telegram credentials with your own accounts.

Toggle the workflow to Active.
