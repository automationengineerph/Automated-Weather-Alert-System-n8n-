# Automated-Weather-Alert-System-n8n
# 🌦️ Automated Weather Alert System (n8n)

An autonomous workflow built in n8n that monitors real-time weather data and sends critical email alerts based on atmospheric conditions.

## 🚀 Features
* **Scheduled Trigger:** Runs every morning at 8:00 AM using n8n's Schedule Trigger.
* **Secure API Integration:** Authenticated connection to OpenWeatherMap API using n8n Credential Manager.
* **Dynamic Logic Gate:** Filters weather states (e.g., Rain/Clouds) using JSON pathing (`$json.weather[0].main`).
* **Data Transformation:** Converts raw Kelvin temperatures from the API into Celsius using JavaScript expressions.
* **Automated Notifications:** Sends formatted HTML emails via Gmail SMTP.

## 🛠️ Technical Stack
* **Automation:** n8n (Cloud/Self-hosted)
* **API:** OpenWeatherMap API v2.5
* **Communication:** Gmail Node (OAuth2)
* **Formatting:** JavaScript Expressions & HTML
