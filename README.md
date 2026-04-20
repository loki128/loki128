<div align="center">

# Karim Lukita

**AI-agentic developer · 19 · Jacksonville, FL · FSCJ**

I pilot AI agents to ship real products in days, not quarters.

Studying AI in college. Building production systems on the side. Already shipped what most teams take a year to finish.

[![Portfolio](https://img.shields.io/badge/lukita--portfolio.com-0A0A0A?style=for-the-badge&logo=vercel&logoColor=white)](https://lukita-portfolio.com)
[![Call Nathan](https://img.shields.io/badge/Call_Nathan-%28904%29_541--8192-00C853?style=for-the-badge&logo=phone&logoColor=white)](tel:+19045418192)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/karim-lukita-0282263a9)
[![Email](https://img.shields.io/badge/Email-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:lukita@cleopatradelights.com)

</div>

---

### Why "AI-agentic" is different from "using AI"

Most people use AI to write code. I architect systems where the AI is the pilot and I'm air traffic control — orchestrating agents, reasoning chains, and feedback loops that do real work at scale.

Every architecture decision, edge case, and product call is still mine. The AI compounds execution speed. The result: **a 19-year-old solo dev matching the output of a 4-person team**.

---

## Flagship — Lukita Dev Agency

**AI phone receptionists for dental practices. Live product, live clients, live money.**

### Meet Nathan

Nathan is a production voice agent that answers phones for dental practices 24/7. He's not a chatbot. He's not a decision tree. He's a Claude-powered AI with a dental-specific system prompt that handles real patient calls.

**Call him right now: [(904) 541-8192](tel:+19045418192)**

What Nathan does on a call:

- **Picks up on ring 1.** No "please hold." No voicemail. No missed opportunity.
- **Books new patients.** Asks for name, DOB, insurance carrier, pain level. Creates the appointment in the client's scheduler. Texts the confirmation.
- **Triages dental emergencies.** Knocked out tooth, severe swelling, bleeding that won't stop → immediate escalation to on-call dentist via Telegram/SMS.
- **Handles insurance questions intelligently.** Doesn't fake expertise. Hands off to a human for complex verification, books a callback if after hours.
- **Knows the practice.** Custom prompt per clinic: their hours, their providers, their accepted insurances, their tone.
- **Never says he's human.** TOS §5.3 compliant — meta-honest, admits he's AI if asked.

Typical call: 90 seconds. Booked appointment in the scheduler by the time the patient hangs up.

### How the agency operates end-to-end

```
┌─────────────────────────────────────────────────────────────────────┐
│                     PROSPECT JOURNEY (outbound)                     │
└─────────────────────────────────────────────────────────────────────┘

    50 dentists      Entity extraction     Personalized
    cold outreach  → per-practice data   → /for/[slug] page
    (Smartlead)      (regex, no LLM)       (unique pitch + video)
                                                   │
                                                   ▼
                                         TOS clickwrap gate
                                         (scroll + 3 acks + SHA-256)
                                                   │
                                                   ▼
                                         Stripe Checkout (live)
                                         $399 setup + $299/mo
                                                   │
                                                   ▼
┌─────────────────────────────────────────────────────────────────────┐
│                 CLIENT PROVISIONING (automated)                     │
└─────────────────────────────────────────────────────────────────────┘

    Supabase webhook      vapi-provision        New phone number
    (Stripe event)     →  edge function      →  assigned in ~10s
                          clones Nathan
                          per-client
                                                   │
                                                   ▼
                          Telegram DM to operator with 3 buttons:
                          🤖 auto-provision  ✓ manual  ⏱ snooze 24h
                                                   │
                                                   ▼
                                         Client goes live
                                         on their own phone number
                                                   │
                                                   ▼
┌─────────────────────────────────────────────────────────────────────┐
│                   PATIENT CALL FLOW (every call)                    │
└─────────────────────────────────────────────────────────────────────┘

    Patient calls      Nathan answers         Books / routes /
    practice line   →  ring 1, natural     →  escalates based on
                       conversation            intent classification
                                                   │
                                                   ▼
                       Call ends → Vapi webhook fires
                                                   │
                                                   ▼
                       Supabase: writes call record (transcript,
                       outcome, duration, recording URL, structured
                       data extracted from the conversation)
                                                   │
                                                   ▼
                       Client dashboard updates: calls answered,
                       patients booked, revenue recovered metric
```

### Built solo, wire by wire

- **Landing pages:** Next.js 16 App Router at `/for/[slug]`, 50 personalized pitches from entity-extracted prospect data (regex, not LLM — deterministic and <1ms)
- **Legal layer:** 7.5k-word Terms of Service + clickwrap gate (scroll-depth verified, 3 checkboxes, SHA-256 hash of accepted version). Red-teamed by 3 parallel Claude legal-advisor agents, graded A−/B+/A−
- **Payments:** Stripe live-mode Checkout → Supabase webhook → provisioning trigger
- **Voice layer:** Vapi for orchestration, ElevenLabs for voice, Claude Haiku 4.5 for low-latency turn generation (<500ms first token)
- **Per-client provisioning:** `vapi-provision` Supabase edge function clones the Nathan template, buys a real phone number in the client's area code, wires their scheduler + insurance list
- **Operator loop:** every payment → Telegram DM with one-tap approval, snooze, or reject buttons (idempotent, survives restart)
- **Outreach stack:** Smartlead warmup on dedicated domain `lukita-portfolio.com`, Resend transactional email, pg_cron scheduled drops, daily `infra-health-check` edge function monitoring 9 systems and emailing status at 9am EDT
- **Deterministic job queue:** custom Postgres-backed job system with `FOR UPDATE SKIP LOCKED` atomic claim, RLS-protected, zero LLM tokens on hot paths — email sends, webhook processing, batch entity extraction all routed through it

Site: **[lukita-portfolio.com](https://lukita-portfolio.com)** · Demo line: **[(904) 541-8192](tel:+19045418192)**

---

### Shipped products

<table>
<tr>
<td width="50%">

**[Cleopatra Delights](https://cleopatradelights.com)** — Production e-commerce

Full-stack platform for an Egyptian-inspired bakery business. 58-item menu, admin dashboard with KPI analytics, customer CRM with lifetime-value tracking, 6-layer anti-spam (Turnstile + rate limiting + honeypot + timing analysis), SEO with JSON-LD structured data.

`Next.js 16` · `Prisma` · `Supabase` · `NextAuth v5` · `Cloudflare Turnstile`

</td>
<td width="50%">

**[MixedRight](https://mixedright.vercel.app)** — AI Recipe SaaS

9-strategy URL scraper (YouTube / TikTok / Instagram / Reddit / blogs), AI-generated food photography via fal.ai FLUX, Stripe Connect marketplace with atomic rate limiting, tiered subscriptions, 30+ hardened API routes.

`Next.js 16` · `TypeScript` · `Supabase` · `Stripe Connect` · `OpenRouter` · `fal.ai`

</td>
</tr>
<tr>
<td width="50%">

**[Dr Dan's No BS Protein](https://dr-dans-protein.vercel.app)** — Brand site, shipped in a week

Conversion-focused landing with scroll-driven motion, product showcase, waitlist capture. Client went from idea to live site in 7 days.

`Next.js 16` · `Tailwind v4` · `shadcn/ui` · `Framer Motion`

</td>
<td width="50%">

**[ResumeAI](https://resume-rebuilder-cursor.vercel.app)** — Strict-truth resume rewriter

AI optimizer that rewrites resumes to match job descriptions without fabricating qualifications. Multi-LLM via OpenRouter, real-time streaming, keyword-match scoring.

`Next.js 14` · `OpenRouter` · `Tailwind CSS`

</td>
</tr>
</table>

---

### Engineering depth

<table>
<tr>
<td width="50%">

**[ASGARD](https://github.com/loki128/asgard)** — Autonomous AI trading agent

**16,000+ lines. Real money on Polymarket.**

- Multi-LLM pipeline: local Ollama pre-filter → Claude deep analysis (cost-optimized)
- 5-hook intelligence layer: market classification, query optimization, news scoring, gap tracking, HNSW memory recall
- 5-layer risk management: circuit breaker, position sizing, stop-loss, take-profit, volatility gate
- MIMIR episodic + semantic memory with temporal supersession
- AI agents found 5 critical vulns during self-audit (SSRF, race conditions, permission escalation) — all patched
- 9 slash commands, 4-tier RBAC, per-user portfolios

`Python` · `asyncio` · `Discord.py` · `Claude API` · `Ollama` · `Polymarket CLOB`

</td>
<td width="50%">

**[Throne](https://github.com/loki128/throne-showcase)** — Self-evolving multi-agent orchestration

**14,000+ lines. Architecture showcase (source private).**

- TAQL quality assessment + democratic voting + trust tiers
- Genetic algorithm prompt evolution with fitness scoring
- Swarm Immune System: 5-rule anomaly detection + quarantine
- Trust Contagion: social graph propagation with toxic-pair detection
- HNSW vector search, pure JS, zero external deps
- 50+ MCP tools exposed via Model Context Protocol server

`Node.js` · `SQLite` · `better-sqlite3` · `MCP`

</td>
</tr>
</table>

---

### Stack

```
Frontend        Next.js 16 (App Router) · React 19 · TypeScript · Tailwind v4 · Framer Motion · shadcn/ui
Backend         Next.js API · Server Actions · Node.js · Python · Stripe Connect · Supabase Edge Functions
Database        Postgres (Supabase) · Prisma · pg_cron · Row-Level Security · HNSW vector search
Voice / AI      Vapi · Claude API (Sonnet + Haiku) · ElevenLabs · HeyGen · OpenRouter · Ollama · fal.ai · MCP
Infra           Vercel · Cloudflare · Resend · Smartlead · Telegram bots · GitHub Actions
Trading         Polymarket CLOB API · orderbook analysis · risk layers · whale detection
```

---

### How I work

I use AI agents as force multipliers, not crutches. I pilot a fleet of specialized agents (architect, security reviewer, QA, deploy-bot) through an orchestration layer I built myself. Every product decision is mine — the AI handles execution speed.

**What that means if you hire me:**

- MVP in days, not months
- One person owns the entire stack — no coordination overhead
- I ship what I promise, in production, with security baked in
- I design for the build *and* for the handoff — every system ships with a runbook

Currently studying AI at FSCJ · Open for select freelance and full-time roles.

---

<div align="center">

**Portfolio → [lukita-portfolio.com](https://lukita-portfolio.com)** · **Call Nathan → [(904) 541-8192](tel:+19045418192)**

[![LinkedIn](https://img.shields.io/badge/Karim_Lukita-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://linkedin.com/in/karim-lukita-0282263a9)
[![Email](https://img.shields.io/badge/lukita@cleopatradelights.com-EA4335?style=flat-square&logo=gmail&logoColor=white)](mailto:lukita@cleopatradelights.com)
[![GitHub followers](https://img.shields.io/github/followers/loki128?style=flat-square&logo=github&color=0A0A0A)](https://github.com/loki128)

</div>
