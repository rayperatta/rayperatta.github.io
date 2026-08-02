# Prompt — Portfolio Web de Ray Peratta (para v0 / Lovable / Cursor / cualquier generador)

> Generado 2026-08-02 (v2 — enfoque 100% IA/automatización). Datos 100% reales verificados contra su CV, LinkedIn y repos. No añadir experiencia ni métricas inventadas.

---

Build a single-page professional portfolio website for a job interview for **AI Engineering / Automation roles**. It will be screen-shared live with an interviewer, so it must look stunning in fullscreen and work offline as a single self-contained HTML file (inline CSS/JS, no build step, no external JS libraries; Google Fonts optional with system fallbacks).

## Person

**Ray Peratta** — AI Automation Engineer
📍 Lisbon, Portugal · ray.peratta.e@gmail.com · +351 911 917 585 · github.com/gozuray
Legal work permit for Portugal/EU. Languages: Spanish (native), English (C1), Portuguese (B2).

**Profile:** AI Automation Engineer specialised in building intelligent systems with Large Language Models (LLMs), AI agents and process automation — backed by 2+ years as a Data Analyst in consulting and multinational operations (Accenture, Conectys). Builds production-grade AI systems, not just prototypes.

## Work experience (timeline)

1. **Data Analyst — Accenture** (Oct 2025 – Present, Lisbon): analyse operational data and produce reports supporting client decision-making; automate reporting with Python and Power Automate reducing manual work; build and maintain Power BI dashboards tracking key KPIs.
2. **Data Analyst — Conectys** (Sep 2023 – May 2025, Lisbon): analysed operational KPIs (quality, volume, SLAs); identified trends/bottlenecks and implemented process improvements; delivered periodic reports to management and clients.

## Featured projects (cards, 7 — AI/automation, verified real)

1. **AI Job Hunter** — LangGraph-based multi-agent system that automates the job application process: scrapes job postings, analyses role fit, tailors the CV and writes a personalized cover letter, powered by LLMs via OpenRouter. Tags: LangGraph · Multi-agent · LLMs · Python · OpenRouter.
2. **AI Document Intake Pipeline** — simulated inbox (emails, PDFs, invoices, forms) → LLM-powered structured extraction → validation → Postgres persistence → automatic routing by type/urgency → notification. The LLM is a component of the pipeline, not the product. CI with ruff + pytest. Tags: Python · LLM extraction · PostgreSQL · Docker · CI.
3. **RAG Document Q&A API** — production-ready Retrieval-Augmented Generation system for querying PDF documents in natural language: documents chunked and embedded with sentence-transformers (local, free), served via FastAPI. Tags: RAG · FastAPI · sentence-transformers · Embeddings · Docker.
4. **AI Lead Enrichment & Routing** — automated lead processing pipeline with n8n + LLMs: classifies leads (industry, company size, intent score), enriches them with personalized outreach suggestions, routes by score and logs to Notion/Sheets with Slack/Telegram notifications. Tags: n8n · LLM classification · Webhooks · Notion · Slack/Telegram.
5. **Personal AI Agent Infrastructure** — self-hosted AI assistant running 24/7 on his own server: Telegram interface, persistent memory, scheduled automations (price tracking, boot notifications via systemd/cron) and multi-model routing. Tags: LLM APIs · Agents · Linux · systemd · Node.js.
6. **Natively for Linux** — AI meeting assistant built from source for Linux: local Whisper speech-to-text, LLM answers via OpenRouter, and a custom Rust system-audio backend over PipeWire, plus Wayland/Hyprland UI fixes. Tags: Whisper STT · Rust · PipeWire · Electron · LLMs.
7. **Excel VBA Report Automation** — production-grade Excel VBA toolkit that automates the full daily reporting cycle: consolidates multi-source CSV/Excel exports, cleans and deduplicates data, applies corporate formatting, exports a print-ready PDF and distributes it via Outlook — with centralized error handling, performance tuning and audit logging. Tags: VBA · Excel · Outlook · Reporting Automation · PDF Export.

## Screenshots

Cards 1–4 have real screenshots of their public GitHub repos (taken with headless Chromium, stored in `assets/screenshots/`, displayed at the top of each card, clickable → repo URL, plus a "View on GitHub ↗" link):
- ai-job-hunter → github.com/gozuray/ai-job-hunter
- ai-document-intake → github.com/gozuray/ai-document-intake
- rag-document-qa → github.com/gozuray/rag-document-qa
- n8n-lead-enrichment → github.com/gozuray/n8n-lead-enrichment

## Skills (grouped chips — AI first)

- **AI & LLMs:** LLM integration (OpenAI, OpenRouter), multi-agent systems (LangGraph), RAG, prompt engineering, vector databases (Qdrant, Pinecone)
- **Automation:** n8n / Make, Power Automate, VBA (Excel/Outlook), REST APIs, webhooks, scripting
- **Data:** SQL, Python (Pandas, NumPy), Power BI, Tableau, Advanced Excel
- **Engineering:** FastAPI, Docker, Git, PostgreSQL, ETL/data cleaning

## Education

Systems Engineering (Bachelor's) — Universidad Privada del Norte, Lima, Peru (2016–2020)

## Design requirements

- **Dark, premium theme**: near-black background (#0a0a0f), subtle surface cards, one accent gradient (violet #7c6cf8 → teal #4dd0c4), thin 1px borders, generous whitespace. Think Linear/Vercel quality.
- **Typography:** Inter or system-ui stack; mono font (JetBrains Mono) for small labels/tags.
- **Sections:** fixed blur nav with active-section highlight → hero (name, "AI Automation Engineer" headline, one-line pitch, CTAs "View projects" + "Download CV") → about → experience timeline → projects grid (6 cards) → skills → languages/education → contact footer.
- **Animations — smooth and restrained, GPU-only (transform/opacity):**
  - Hero elements fade+rise on load with stagger (cubic-bezier(0.22, 1, 0.36, 1))
  - Scroll-reveal on every section via IntersectionObserver, staggered children
  - Project cards lift (-6px) with soft accent glow that follows the cursor
  - Two blurred gradient orbs slowly floating behind the hero
  - Smooth anchor scrolling; nav gains background after scrolling
  - Respect `prefers-reduced-motion`
- Fully responsive (must look perfect at 1920×1080 fullscreen and on mobile).
- Language: **English**.
