<div align="center">

# Karim Lukita

**One-Person Product Studio | Jacksonville, FL**

I turn ideas into shipped products — SaaS platforms, trading bots, AI pipelines, games. Design to deployment, solo. 10+ projects shipped across web, fintech, AI, and gaming.

[![Portfolio](https://img.shields.io/badge/lukita--portfolio.com-D4AF37?style=for-the-badge&logo=googlechrome&logoColor=black)](https://lukita-portfolio.com)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/karim-lukita-0282263a9)
[![Email](https://img.shields.io/badge/Contact_Me-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:lukita@cleopatradelights.com)

</div>

---

### What I Do

I'm a product builder who ships fast. I use AI-assisted development to move at the speed of a small team — but every decision, architecture choice, and design call is mine. I don't just write code. I scope the product, design the UI, build the backend, handle payments, deploy it, and maintain it.

**If you need an MVP built in a week, not a quarter — that's what I do.**

---

### Technical Skills

```
Frontend        React 19 · Next.js 16 (App Router) · TypeScript · Tailwind CSS v4
UI & Motion     Framer Motion 12 · Three.js · React Three Fiber · shadcn/ui · Recharts
Backend         Next.js API Routes · Server Actions · Node.js · Python · REST APIs · Stripe Connect
Database        PostgreSQL (Supabase) · Prisma 7.5 · SQLite · Connection Pooling · Row-Level Security
Auth & Security NextAuth v5 · Google OAuth · RBAC · Cloudflare Turnstile · Rate Limiting · SSRF Protection
AI/LLM          Claude API · OpenRouter · Ollama (local LLM) · Multi-LLM Pipelines · Prompt Engineering · fal.ai
Trading         Polymarket CLOB API · Orderbook Analysis · Risk Management · Position Sizing · Whale Detection
Infrastructure  Vercel · Git · GitHub · CI/CD · Discord.py · asyncio · Custom Domains · DNS
```

---

### Shipped Products

<table>
<tr>
<td width="50%">

**[MixedRight](https://mixedright.vercel.app)** — AI Recipe SaaS (Founder)

Full-stack AI-powered recipe platform with marketplace, social features, and Stripe payments.

- AI recipe formatter with 9-strategy URL scraper (YouTube, TikTok, Instagram, Reddit, blogs)
- AI-generated food photography per recipe and collection cover (fal.ai FLUX)
- Stripe Connect marketplace — sellers list, buyers purchase, platform splits payments
- Social layer: follows, saves, comments, collections with AI covers
- Tiered subscription (Free / Baker $10 / Seller $20) with atomic rate limiting
- 30+ API routes with CSRF protection, rate limiting, input sanitization, and RLS

`Next.js 16` `TypeScript` `Supabase` `Stripe Connect` `OpenRouter` `fal.ai` `Framer Motion` `Tailwind v4`

</td>
<td width="50%">

**[Cleopatra Delights](https://cleopatradelights.com)** — Client Project

Full-stack e-commerce platform and admin dashboard for an Egyptian-inspired food trailer business.

- 58-item menu with category filtering and custom order form
- Admin dashboard: Google OAuth, KPI charts, order management, customer CRM with lifetime value tracking
- Multi-layer anti-spam: Cloudflare Turnstile, per-IP rate limiting, honeypot fields, timing analysis
- SEO with JSON-LD structured data, Egyptian-inspired design system

`Next.js 16` `Prisma` `Supabase` `NextAuth v5` `Cloudflare Turnstile` `Zod`

</td>
</tr>
<tr>
<td width="50%">

**[Dr Dan's No BS Protein](https://dr-dans-protein.vercel.app)** — Client Project

Brand website for a protein supplement company, designed and deployed end-to-end.

- Conversion-focused landing page with scroll-driven animations
- Product showcase, trust marquee, waitlist capture
- Responsive across all breakpoints

`Next.js 16` `TypeScript` `Tailwind v4` `shadcn/ui` `Framer Motion`

</td>
<td width="50%">

**[ResumeAI](https://resume-rebuilder-cursor.vercel.app)** — Tool

AI-powered resume optimizer that rewrites resumes to match job descriptions without fabricating qualifications.

- Keyword matching and job description analysis
- Strict truth mode — enhances without inventing
- LLM integration via OpenRouter

`Next.js 14` `TypeScript` `OpenRouter` `Tailwind CSS`

</td>
</tr>
</table>

### Engineering Systems

<table>
<tr>
<td width="50%">

**ASGARD** — AI Trading Agent (16,000+ lines)

Production trading system with Discord interface that scans prediction markets, runs multi-LLM analysis, and executes real-money trades on Polymarket.

- **Multi-LLM pipeline**: local Ollama pre-filters before Claude deep analysis — production cost optimization
- **5-hook intelligence layer**: market classification, query optimization, news scoring, gap tracking, HNSW memory recall
- **Risk management**: circuit breaker, position sizer, stop loss, take profit, volatility gate
- **Live trading**: real money on Polymarket via CLOB API with safety cap, confirmation flow, 30s timeout
- **Security audited**: AI agents found 5 critical vulns (SSRF, race conditions, permission escalation) — all patched
- **MIMIR memory**: episodic + semantic memory with temporal supersession
- 9 slash commands, 4-tier RBAC, per-user portfolios, web scraping, fighter stats enrichment

`Python` `asyncio` `Discord.py` `Claude API` `Ollama` `Tavily` `Firecrawl` `SQLite` `Polymarket CLOB`

</td>
<td width="50%">

**Throne** — Multi-Agent AI Orchestration (14,000+ lines)

Self-evolving multi-agent system with genetic algorithm prompt evolution, swarm immune system, trust contagion networks, and constitutional evolution.

- TAQL quality assessment + democratic voting + trust tiers
- Prompt DNA: genetic algorithm evolving prompts using fitness scoring
- Swarm Immune System: 5-rule anomaly detection + quarantine
- Trust Contagion: social graph propagation with toxic pair detection
- HNSW vector search (pure JS, no external dependencies)
- 50+ MCP tools exposed via Model Context Protocol server

`Node.js` `SQLite` `better-sqlite3` `Zod` `Pino` `EventEmitter3`

</td>
</tr>
<tr>
<td width="50%">

**Sword Factory** — Roblox Game

Custom game with hand-built physics and VFX systems — no marketplace assets.

- Custom MathVector system, Perlin noise terrain, Bezier curve animations
- Spring physics impact system, trail VFX engine
- Hybrid animation track system, modern UI framework

`Luau` `Roblox Studio` `Custom Physics` `Custom VFX`

</td>
<td width="50%">

**LARPKit** — Dev Tool

Fake company generator for testing and prototyping. 6 fully functional tabs.

`React` `TypeScript` `Tailwind CSS`

</td>
</tr>
</table>

---

### How I Work

I use AI agents as force multipliers — not crutches. Every product decision, architecture choice, and design direction is mine. The AI handles execution speed. The result: solo output that matches a small team, with the coherence of a single vision.

**What that means for clients:**
- MVP in days, not months
- One person owns the entire stack — no coordination overhead
- I ship what I promise, and it works in production

---

### Services

| What | Deliverable | Range |
|------|-------------|-------|
| **SaaS MVP** | Full product — auth, payments, deploy | $5,000 – $15,000 |
| **Trading Bot / AI Pipeline** | Custom bot with live execution | $3,000 – $25,000 |
| **Business Website** | Design + build + deploy | $1,500 – $3,000 |
| **Discord/Telegram Bot** | AI-powered with custom pipeline | $3,000 – $8,000 |
| **Retainer** | AI builder on call | $3,000 – $5,000/mo |

---

<div align="center">

**Open for projects** — MVPs, trading systems, AI integrations, and anything that ships

[![Portfolio](https://img.shields.io/badge/lukita--portfolio.com-D4AF37?style=flat-square&logo=googlechrome&logoColor=black)](https://lukita-portfolio.com)
[![Email](https://img.shields.io/badge/lukita@cleopatradelights.com-EA4335?style=flat-square&logo=gmail&logoColor=white)](mailto:lukita@cleopatradelights.com)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Karim_Lukita-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://linkedin.com/in/karim-lukita-0282263a9)

</div>
