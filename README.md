# 🌤️📰 Daily Automation Bot (Weather + News)

This project is an **automation workflow built with n8n** that sends a **daily summary** of:
- Current **weather conditions** (powered by OpenWeather API).
- Latest **news headlines** (powered by NewsAPI).

The summary is automatically delivered to **Telegram** once per day.  
Perfect for staying updated without checking multiple apps.

---

## 🚀 Features
- Fetches live weather data (temperature, condition, city-specific).
- Collects top news headlines with links.
- Combines both into a **single organized message**.
- Sends the update automatically to **Telegram**.

---

## 🛠️ Tech Stack
- **n8n** (workflow automation tool)
- **OpenWeather API**
- **NewsAPI**
- **Telegram Bot API**
- (Optional) **Email Node** to send via Gmail

---

## 📸 Workflow Overview
1. **Trigger**: Workflow runs daily at a scheduled time.
2. **Weather Node**: Fetches weather data from OpenWeather.
3. **News Node**: Fetches headlines from NewsAPI.
4. **Function Node**: Formats data into a clean message.
5. **Telegram Node**: Sends message to user via Telegram.

---

## 📝 Example Output