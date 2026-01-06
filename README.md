## 📌 Project Requirements – Social Media Auto-Posting AI Agent

This project is an automated AI-powered workflow built using **n8n** that fetches AI-related news, generates content using AI models, creates images, and posts automatically to multiple social media platforms.

To successfully run and work on this workflow, the following requirements are needed.

---

## 🛠️ 1. Platform & Environment Requirements

* **n8n Automation Platform**

  * Self-hosted n8n instance **or**
  * n8n Cloud account
* **Node.js** (recommended v18+ for self-hosted n8n)
* Stable internet connection (required for API calls)

---

## 🔐 2. API Keys & Credentials Required

### 📰 News Data

* **NewsAPI Key**

  * Used to fetch latest AI-related news articles
  * Endpoint: `https://newsapi.org/v2/everything`

---

### 🤖 AI & Language Models

* **Google Gemini (PaLM) API Key**

  * Used for:

    * News summarization
    * Title generation
    * Hashtag generation
* **OpenAI API Key**

  * Used for:

    * AI image generation (DALL·E)
* **Hugging Face API Token**

  * Used for:

    * Image generation using FLUX model

---

## 📱 3. Social Media Platform Requirements

### 📘 Facebook & 📸 Instagram

* **Facebook Graph API Access**
* Required permissions:

  * `pages_manage_posts`
  * `pages_read_engagement`
  * `instagram_basic`
  * `instagram_content_publish`
* Facebook Page connected to an Instagram Business Account
* Valid **Page ID / Instagram User ID**
* Long-lived access token configured in n8n credentials

---

### ❌ X (Twitter)

* **X Developer Account**
* OAuth 2.0 credentials
* Permissions:

  * `tweet.write`
* Connected via n8n **Twitter OAuth2 node**

> ⚠️ Note: X posting integration was assisted by a teammate, while the rest of the workflow was designed independently.

---

### 💼 LinkedIn

* **LinkedIn Developer Application**
* OAuth 2.0 access token
* Required scopes:

  * `w_member_social`
  * `r_liteprofile`
* Ability to upload media and create UGC posts

---

## 📧 4. Email Notification System

* **Gmail OAuth2 Credentials**
* Used to send automated confirmation emails after successful posts to:

  * Instagram
  * Facebook
  * X (Twitter)
  * LinkedIn

---

## ⏰ 5. Scheduling Requirement

* **n8n Schedule Trigger Node**
* Configured to run automatically at a specific time (e.g., daily at 9:01 AM)
* Server or cloud instance must remain active for scheduled execution

---

## 🧠 6. Workflow Logic Dependencies

* Structured Output Parsers (JSON enforced)
* AI Memory Buffer (for context retention)
* Proper node-to-node data mapping
* Error handling enabled for retry on failure

---

## 👤 7. Team & Contribution

* **Primary Designer & Developer:** Pavan
* **Contribution:**

  * X (Twitter) posting integration assisted by one teammate
  * All remaining workflow design, logic, integrations, and automation handled independently

---

## ✅ Summary

To work on or deploy this workflow, you must have:

* A working n8n environment
* Valid API keys for news, AI models, and image generation
* Developer access to Facebook, Instagram, X, and LinkedIn
* Gmail account for notifications
* Proper OAuth and permission setup for all platforms

Once configured, the agent runs **fully automatically**, requiring no manual intervention.
