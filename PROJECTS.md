# Projects overview

A brief summary of each project in the portfolio.

---

## 01: AI Document Intake Pipeline

Simulates a company inbox (emails, PDFs, invoices, forms) and uses an LLM to pull out the important data automatically. The system validates what it extracts, saves it to PostgreSQL, then routes each document based on type and urgency.

**Stack:** Python, LLM extraction, PostgreSQL, Docker, CI

---

## 02: RAG Document Q&A API

A backend service for asking questions about PDFs in plain language. Documents get split into small pieces and embedded with local sentence-transformers. When you ask something, the system retrieves the most relevant chunks and lets an LLM generate an answer from them. Served as a FastAPI endpoint.

**Stack:** RAG, FastAPI, sentence-transformers, embeddings, Docker

---

## 03: AI Lead Enrichment & Routing

Built with n8n. Incoming leads pass through an LLM that tags them by industry, company size, and intent score. The pipeline then writes personalized outreach suggestions and routes each lead by priority. Notifications go to Slack or Telegram.

**Stack:** n8n, LLM classification, webhooks, Notion, Slack/Telegram

---

## 04: Personal AI Agent Infrastructure

A self-hosted AI assistant running 24/7 on my own server. It talks to me through Telegram, keeps persistent memory, and handles scheduled tasks like price tracking and notifications through systemd and cron. Multi-model routing picks the right LLM for each job.

**Stack:** LLM APIs, agents, Linux, systemd, Node.js

---

## 05: Excel VBA Report Automation

A VBA toolkit that handles the full daily reporting cycle in Excel. It pulls data from multiple CSV and Excel exports, cleans and deduplicates it, applies corporate formatting, then exports a print-ready PDF and sends it through Outlook. Error handling and audit logging are built in.

**Stack:** VBA, Excel, Outlook, reporting automation, PDF export
