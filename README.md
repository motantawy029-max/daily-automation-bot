# 🤖 Daily Automation Bot — Weather + News (n8n workflow)

Automated daily summary workflow built with **n8n** ⚡ that fetches current 🌤 weather (OpenWeather) and 📰 top news headlines (NewsAPI), and delivers a single organized message to **Telegram** 💬 and **Email** 📧.

---

## ✨ Features
- 🌍 Fetches live weather for **Alexandria, Egypt**.
- 📰 Fetches top news headlines (configurable country / keyword).
- 📑 Aggregates results into one nicely formatted HTML email and a short Telegram message.
- ⏰ Runs daily via a schedule trigger.

---

## 🛠 Tech stack
- 🔄 **n8n** (workflow automation)
- 🌤 **OpenWeather API**
- 📰 **NewsAPI**
- 💬 **Telegram Bot API**
- 📧 **Gmail OAuth** (optional for email delivery)

---

## 📦 What’s included
- 📂 `workflow.json` — n8n workflow export (safe version, **no secrets**).
- 📝 `README.md` — this file.
- 🔑 `env.template` — list of environment variables / keys to fill before running.
- 🖼 `screenshots/` — (recommended) add screenshots of the workflow and sample output.

> ⚠️ **Important:** This repository does **not** contain API keys or credentials. You must provide them locally in your n8n instance.

---

## 🚀 Quick setup (Import & Credentials)
1. **📥 Import workflow**
   - Open your n8n instance → Workflows → Import → Upload `workflow.json`.
2. **🔑 Add credentials**
   - 🌤 **OpenWeather**: replace placeholder `YOUR_OPENWEATHER_KEY` in the OpenWeather HTTP node, or set as environment variable and reference it.
   - 📰 **NewsAPI**: replace `YOUR_NEWSAPI_KEY` in the NewsAPI HTTP node or set as environment variable.
   - 💬 **Telegram**: create a Telegram Bot via BotFather 🤖 and set the Bot Token in n8n Credentials (Telegram).
   - 📧 **Gmail** (optional): create OAuth credentials in Google Cloud Console and add Gmail OAuth2 credential in n8n.
3. **🔗 Connect credentials to nodes**
   - After importing, open each node that requires credentials (Gmail/Telegram) and select the correct credential (or create new one).
4. **✅ Test**
   - Run the OpenWeather and News nodes individually (▶️ Execute Node) to ensure they return valid JSON.
   - Execute the `BuildEmail` (Function) node to preview `bodyHtml` and `telegramText`.
   - Execute the whole workflow or wait for the scheduled run.

---

## 🧩 env.template
Use this file as a guide to store your keys (locally, not in Git).
