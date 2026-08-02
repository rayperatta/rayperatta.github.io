# Prompt — Portfolio Web de Ray Peratta (para v0 / Lovable / Cursor / cualquier generador)

> Generado 2026-08-02. Datos 100% reales verificados contra su CV y repos. No añadir experiencia ni métricas inventadas.

---

Build a single-page professional portfolio website for a job interview. It will be screen-shared live with an interviewer, so it must look stunning in fullscreen and work offline as a single self-contained HTML file (inline CSS/JS, no build step, no external JS libraries; Google Fonts optional with system fallbacks).

## Person

**Ray Peratta** — Data Analyst & AI Automation Engineer
📍 Lisbon, Portugal · ray.peratta.e@gmail.com · +351 911 917 585 · github.com/gozuray
Legal work permit for Portugal/EU. Languages: Spanish (native), English (C1), Portuguese (B2).

**Profile:** Data Analyst with 2+ years across consulting and multinational operations (Accenture, Conectys), focused on automating operational processes and reporting workflows with Python, Power BI and Power Automate. Builds production-grade AI automation systems and full-stack personal projects.

## Work experience (timeline)

1. **Data Analyst — Accenture** (Oct 2025 – Present, Lisbon): analyse operational data and produce reports supporting client decision-making; automate reporting with Python and Power Automate reducing manual work; build and maintain Power BI dashboards tracking key KPIs.
2. **Data Analyst — Conectys** (Sep 2023 – May 2025, Lisbon): analysed operational KPIs (quality, volume, SLAs); identified trends/bottlenecks and implemented process improvements; delivered periodic reports to management and clients.

## Featured projects (cards, 5)

1. **SnackTrack** — Android macro-nutrient calendar with real supermarket prices from Portugal (Continente, Auchan). Kotlin · Jetpack Compose · Material 3 · MVVM + Clean Architecture · Room · Hilt, backend on Cloudflare Workers + D1 (SQLite) in TypeScript with AI product matching and scheduled price-scraping jobs.
2. **Finance Dashboard** — full-stack personal finance dashboard (TypeScript, Prisma + SQLite) with a token-authenticated REST API, Bybit exchange integration (HMAC-SHA256 signed requests) tracking a SOL/USDT pool, and a systemd timer updating prices every 5 minutes.
3. **Natively for Linux** — built an AI meeting assistant from source for Linux: wrote a custom Rust system-audio backend using PipeWire (parec + monitor capture), plus Wayland/Hyprland UI fixes (blur→hide window management). Electron · TypeScript · Rust.
4. **Personal AI Agent Infrastructure** — 24/7 self-hosted AI assistant: Telegram bot, systemd services/timers, cron automations (price tracking, boot notifications), messaging routing and memory systems. Linux · Node.js · systemd · REST APIs.
5. **Pixel Agents** — real-time visual dashboard that monitors local AI coding agent sessions (React + Vite frontend, Node API, polls the agent CLI every 3s with zero token cost). Audited and adapted the codebase for personal use.

## Skills (grouped chips)

- **Data:** SQL, Python (Pandas, NumPy), Advanced Excel, Google Sheets
- **Visualisation:** Power BI, Tableau, Looker Studio
- **Automation & AI:** Power Automate, n8n / Make, REST APIs, LLM integration (OpenAI), prompt engineering, scripting
- **Engineering:** ETL/data cleaning, Git, KPI reporting, process improvement

## Education

Systems Engineering (Bachelor's) — Universidad Privada del Norte, Lima, Peru (2016–2020)

## Design requirements

- **Dark, premium theme**: near-black background (#0a0a0f), subtle surface cards, one accent gradient (violet #7c6cf8 → teal #4dd0c4), thin 1px borders, generous whitespace. Think Linear/Vercel quality.
- **Typography:** Inter or system-ui stack; mono font (JetBrains Mono) for small labels/tags.
- **Sections:** fixed blur nav with active-section highlight → hero (name, role, one-line pitch, CTAs "View projects" + "Download CV") → about → experience timeline → projects grid → skills → languages/education → contact footer.
- **Animations — smooth and restrained, GPU-only (transform/opacity):**
  - Hero elements fade+rise on load with stagger (cubic-bezier(0.22, 1, 0.36, 1))
  - Scroll-reveal on every section via IntersectionObserver, staggered children
  - Project cards lift (-6px) with soft accent glow on hover
  - Two blurred gradient orbs slowly floating behind the hero
  - Smooth anchor scrolling; nav gains background after scrolling
  - Respect `prefers-reduced-motion`
- Fully responsive (must look perfect at 1920×1080 fullscreen and on mobile).
- Language: **English**.
