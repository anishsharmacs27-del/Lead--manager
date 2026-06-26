# 🚀 Lead Manager — AI-Powered Lead Management & Email Tracking System

A fully functional, single-file web application for capturing leads, sending personalized emails, and tracking engagement — powered by Claude AI.

---

## 🌐 Live Demo

👉 **[https://anishsharmacs27-del.github.io/Lead--manager/](https://anishsharmacs27-del.github.io/Lead--manager/)**

---

## 📋 Features

### 1. Lead Capture Form
- Collects Full Name, Email, Phone, Company, and Requirement
- Real-time form validation
- Instant submission with feedback

### 2. AI Lead Classification (Bonus)
- Powered by **Claude AI (claude-sonnet-4-6)**
- Auto-classifies leads by category (e.g. AI Automation, Web Development)
- Assigns priority: **High / Medium / Low**
- Scores leads from **1–10**
- Generates tags and a one-line summary

### 3. Automated Personalized Email
- Sends a personalized email using the lead's name and requirement
- Includes a unique **trackable link** per lead

### 4. Email Open Tracking
- Tracks whether the email was opened
- Shows open status in the Emails tab and Dashboard

### 5. Link Click Tracking
- Each email contains a unique tracking URL
- Clicks are logged and shown in the Dashboard
- Redirects user to the destination after tracking

### 6. Analytics Dashboard
- Live metrics: Total Leads, Emails Sent, Opened, Clicks, Open Rate %, Click Rate %
- Bar chart for email performance
- Doughnut chart for lead categories
- Click activity log per lead

### 7. Leads Table
- Full table of all submitted leads
- Shows AI category, priority, score, and email status
- **CSV export** with one click

---

## 🛠️ Tech Stack

| Layer | Technology |
|---|---|
| Frontend | HTML5, CSS3, Vanilla JavaScript |
| Charts | Chart.js 4.4 |
| Icons | Tabler Icons |
| AI Classification | Anthropic Claude API (claude-sonnet-4-6) |
| Hosting | GitHub Pages |
| Database | In-memory (browser session) |

---

## 🏗️ Architecture

```
User fills form
      ↓
Lead saved to in-memory DB
      ↓
Unique trackable link generated (trk_xxxxxxxx)
      ↓
Personalized email preview shown
      ↓
AI analyzes requirement → category, priority, score, tags
      ↓
Email open simulated (70% open rate)
      ↓
Dashboard updates live with all metrics
```

---

## 📊 How Tracking Works

### Email Open Tracking
In a production system, a 1×1 invisible pixel image is embedded in the HTML email. When the recipient opens the email, their email client loads the image, triggering a request to the server which logs the open event. In this demo, a 70% probability simulation is used.

### Link Click Tracking
Each lead gets a unique tracking ID (`trk_xxxxxxxx`). The trackable link points to this app with the tracking ID as a URL parameter. When clicked, the click is logged in the database before redirecting the user to the actual destination URL.

---

## 🔑 Setup & Usage

1. Open the [live demo](https://anishsharmacs27-del.github.io/Lead--manager/)
2. Enter your **Anthropic API key** (`sk-ant-...`) in the banner at the top to enable AI features
3. Fill in the lead capture form and submit
4. View AI classification results instantly
5. Navigate to **Dashboard** to see analytics
6. Use **Leads** tab to view all leads and export CSV
7. Use **Emails** tab to view open tracking log

> **Note:** API key is stored in browser localStorage. All lead data resets on page refresh (no backend database in this demo version).

---

## 📁 Project Structure

```
index.html        ← Entire application (self-contained)
README.md         ← This file
```

---

## 🔮 Future Improvements

- [ ] Backend database (Firebase / Supabase) for persistent storage
- [ ] Real email sending via SendGrid / Nodemailer
- [ ] Real open tracking pixel server
- [ ] User authentication
- [ ] Lead pipeline / CRM view
- [ ] Bulk email campaigns
- [ ] Webhook integrations (Slack, Zapier)

---

## 👨‍💻 Built By

**Anish Sharma**
GitHub: [@anishsharmacs27-del](https://github.com/anishsharmacs27-del)

---

## 📄 License

MIT License — free to use and modify.
