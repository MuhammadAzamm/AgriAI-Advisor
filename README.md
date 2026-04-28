#  AgriAI Advisor
### An Intelligent Crop Disease Detection & Advisory System for Precision Agriculture in Pakistan

[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](https://opensource.org/licenses/MIT)
[![Python](https://img.shields.io/badge/Built%20with-n8n-orange)](https://n8n.io/)
[![AI Powered](https://img.shields.io/badge/AI-Groq%20LLM-blue)](https://groq.com/)
[![Weather](https://img.shields.io/badge/Data-OpenWeather%20API-lightblue)](https://openweathermap.org/)
[![IEEE](https://img.shields.io/badge/Published-IEEE%20Format-red)]()

> **AgriAI Advisor** is an AI-powered system that helps Pakistani farmers detect crop diseases and receive real-time, localized treatment recommendations — in both English and Urdu.



##  Overview

Agriculture contributes approximately **19% to Pakistan's GDP** and employs a large portion of its rural population. However, farmers frequently suffer crop losses due to undetected diseases and lack of timely expert advice.

**AgriAI Advisor** bridges this gap by combining:
-  Large Language Models (LLMs) via **Groq API**
-  Workflow automation via **n8n**
-  Real-time weather context via **OpenWeather API**
-  A simple, accessible **web interface**
- 🇵🇰 **Urdu language** support for local farmers

---

##  Problem Statement

Farmers in Pakistan lack access to:
- Real-time crop disease diagnosis
- Localized treatment recommendations
- Easy-to-use digital agricultural tools

This results in **delayed decision-making** and **increased crop damage**, directly impacting livelihoods and food security.

---

##  Features

| Feature | Description |
|---|---|
|  Disease Identification | AI-powered detection of crop diseases from text descriptions |
|  Cause Analysis | Explains the root causes behind identified diseases |
|  Treatment Recommendations | Actionable treatment steps tailored to the crop and conditions |
|  Prevention Strategies | Long-term measures to avoid future outbreaks |
|  Risk Scoring | Quantified risk level (60–100% scale) for each case |
|  Weather Integration | Factors in live temperature and humidity data |
| 🇵🇰 Urdu Translation | Full Urdu output for farmer accessibility |
|  Structured Reports | Clean, readable advisory reports via the web UI |

---

##  System Architecture

```
User Input (Web UI)
        │
        ▼
  n8n Webhook Trigger
        │
        ▼
  Data Normalization (Function Nodes)
        │
        ▼
  OpenWeather API ──► Data Enrichment
        │
        ▼
  ┌─────────────────────────────────┐
  │       Groq LLM AI Modules       │
  │  • Disease Identification        │
  │  • Cause Analysis                │
  │  • Treatment Suggestions         │
  │  • Prevention Strategies         │
  │  • Risk Score Calculation        │
  └─────────────────────────────────┘
        │
        ▼
  Urdu Translation (AI)
        │
        ▼
  Structured Report → Web UI Output
```

**Pipeline:**  `Input → Processing → AI Analysis → Localization → Output`

---

##  Tech Stack

| Layer | Technology |
|---|---|
| Frontend | HTML, CSS, JavaScript |
| Workflow Automation | [n8n](https://n8n.io/) (17-node workflow) |
| AI Engine | [Groq API](https://groq.com/) (LLM) |
| Weather Data | [OpenWeather API](https://openweathermap.org/) |
| Language Support | AI-powered Urdu Translation |

---

##  Workflow Pipeline

The n8n workflow consists of **17 nodes**:

1. **Webhook Trigger Node** — Receives user input from the frontend
2. **Set / Function Nodes** — Normalizes and structures the input
3. **HTTP Request Nodes** — Calls OpenWeather API and Groq API
4. **AI Processing Nodes** — Runs 4 parallel AI analysis modules
5. **Merge Node** — Consolidates all AI outputs
6. **Translation Node** — Converts output to Urdu
7. **Respond to Webhook Node** — Returns the final structured report

---

##  Results

The system generates complete advisory reports in real-time, including:

-  **Disease Name & Identification**
-  **Risk Level** (scored 60–100%)
-  **Cause Explanation**
-  **Treatment Recommendations**
-  **Prevention Measures**
- 🇵🇰 **Urdu Translation** of the full report

The interface presents results in a clean, readable format optimized for low-literacy and rural users.

---

##  Limitations

- Requires active internet connectivity
- AI response quality may vary across different crop types
- Limited training data coverage for certain niche crops

---

##  Future Work

- [ ]  **Image-based Disease Detection** using Computer Vision
- [ ]  **Mobile Application** (Android/iOS)
- [ ]  **WhatsApp / Telegram Bot** integration
- [ ]  **Historical Database** for trend analysis
- [ ]  **IoT Sensor Integration** for real-time field monitoring

---

##  Author

**Muhammad Azam**
BS Artificial Intelligence — PAF-IAST, Pakistan
📧 [axamkhan7@gmail.com](mailto:axamkhan7@gmail.com)

---

## 📚 References

1. [OpenWeather API Documentation](https://openweathermap.org)
2. [Groq API Documentation](https://groq.com/)
3. [n8n Workflow Automation Platform](https://n8n.io/)

---

> *This project was developed as part of an academic research initiative to leverage AI for smart farming in developing regions. Published in IEEE format.*

##  UI
![UI Screenshot](assets/ui.png)

##  Workflow
![Workflow Screenshot](assets/workflow.png)

---

##  Project Structure
AgriAI-Advisor/
├── report/        # Project documentation
├── workflow/      # n8n workflow JSON
├── ui/            # Frontend interface
├── assets/        # Screenshots and media
