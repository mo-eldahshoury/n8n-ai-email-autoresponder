# 🤖 n8n AI-Powered Lead Autoresponder

An automated workflow built with **n8n** that intercepts incoming lead form submissions, processes customer requirements using OpenAI (ChatGPT), and generates a personalized, formatted email response sent automatically via Gmail.

---

## 📌 Overview

Speed to lead is critical for agency growth. This workflow automates the initial touchpoint by reading incoming form entries, extracting customer needs, generating a custom solution email draft using AI, and instantly delivering it to the prospect.

---

## ⚡ Features

* **Instant Trigger:** Activates immediately upon a new form submission.
* **AI-Powered Personalization:** Generates context-aware email body text based on specific client constraints (Budget, Needs, Name).
* **HTML Email Formatting:** Formats output with structural HTML headings (`<h2>` / `<h1>`) and clean typography.
* **Seamless Dispatch:** Automatically sends out the email via Gmail OAuth2 integration.

---

## 🛠️ Tech Stack & Integrations

* **Automation Engine:** [n8n](https://n8n.io/)
* **AI Model:** OpenAI (ChatGPT API)
* **Email Service:** Gmail API
* **Triggers:** n8n Form Trigger / Webhook

---

## 🔄 Workflow Logic

1. **Trigger (`On form submission`):** Captures incoming data fields:
   * `Customer Name` / `Your Secondary Name`
   * `Your Email`
   * `What Is Your Budget?`
   * `What's Your Need?`
2. **AI Processing (`Message a model`):** Passes variables into OpenAI with custom prompt instructions:
   * Drafts tailored solutions from **Egynt (AI Automation Agency)**.
   * Strips out redundant subjects or placeholders.
   * Formats the output with HTML tags (`<h2>` header, `<b>` bold signature).
3. **Action (`Send a message`):** Dispatches the finalized HTML email directly to the lead via Gmail.

---

## 🚀 How to Import & Use

1. **Clone this repository:**
   ```bash
   git clone [https://github.com/mo-eldahshoury/n8n-ai-email-autoresponder.git](https://github.com/mo-eldahshoury/n8n-ai-email-autoresponder.git)
