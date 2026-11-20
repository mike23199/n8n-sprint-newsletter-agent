# Automated Sprint Summary & Sponsor Newsletter Draft Agent (n8n)

A lightweight **AI workflow prototype** built in **n8n** for the **Panther Racing Team (Aristotle University of Thessaloniki)**. It automates the process of turning uploaded sprint notes (PDF) into a structured sponsor update / newsletter draft.

> **Status:** Functional Prototype (Draft Generator) — designed to generate ready-to-review email drafts rather than sending automated emails directly.

---

## 🎯 Problem & Motivation
Writing regular progress updates and sponsor newsletters from technical sprint documentation takes recurring manual effort. This workflow automates the extraction and initial drafting steps while keeping a human-in-the-loop before final distribution.

---

## ⚙️ How the Workflow Works
1. **Google Drive Trigger (`fileCreated`):** Monitors a dedicated Google Drive folder for newly uploaded sprint files.
2. **Download File:** Retrieves the newly created file from Google Drive.
3. **Extract from File (`Extract From PDF`):** Parses and extracts raw text content from the uploaded PDF document.
4. **AI Agent (`panther agent`):** Processes the extracted text using **Gemini 3.1 Flash Lite** (with a **Wikipedia** tool connection for quick background/terminology context) to generate a structured, sponsor-friendly email/newsletter draft.

---

## 🛠️ Tools & Technologies
- **Workflow Automation:** n8n
- **Cloud Storage:** Google Drive API
- **LLM & Agent Framework:** Google Gemini (`Gemini 3.1 Flash Lite`), n8n AI Agent node

---

## 📂 Repository Contents
- `workflow.json` – Sanitized n8n workflow export (credentials and sensitive IDs removed).
- `screenshots/` – Visual overview of the n8n node architecture and sample output.

---

## 🔒 Privacy Note
Team-specific credentials, folder IDs, and internal sprint documents have been omitted for confidentiality.
