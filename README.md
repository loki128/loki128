<div align="center">

# Karim Lukita

**Full-Stack Developer & AI Systems Engineer | Jacksonville, FL**

I build production web platforms and AI systems for real businesses — e-commerce, SaaS products, trading infrastructure, multi-agent orchestration, and the security architecture to protect them. 7+ shipped projects — all designed, built, and maintained by me.

[![Portfolio](https://img.shields.io/badge/lukita--portfolio.com-D4AF37?style=for-the-badge&logo=googlechrome&logoColor=black)](https://lukita-portfolio.com)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/karim-lukita-0282263a9)
[![Email](https://img.shields.io/badge/Contact_Me-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:lukita@cleopatradelights.com)

</div>

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

### Portfolio — lukita-portfolio.com

<table>
<tr>
<td width="50%">

**[MixedRight](https://mixedright.vercel.app)** — AI Recipe SaaS (Founder)

Full-stack AI-powered recipe platform with marketplace, social features, and Stripe payments. Users paste any recipe or URL and the AI formats, enhances, and generates food photography.

- AI recipe formatter with 9-strategy URL scraper (YouTube transcripts, TikTok, Instagram, Reddit, blogs)
- AI-generated food photography per recipe and collection cover (fal.ai FLUX)
- Stripe Connect marketplace — sellers list recipes, buyers purchase, platform splits payments
- Social layer: follows, saves, comments, collections with AI covers
- Tiered subscription model (Free / Baker $10 / Seller $20) with atomic rate limiting
- 30+ API routes with CSRF protection, rate limiting, input sanitization, and RLS

`Next.js 16` `TypeScript` `Supabase` `Stripe Connect` `OpenRouter` `fal.ai` `Framer Motion` `Tailwind v4`

</td>
<td width="50%">

**[Cleopatra Delights](https://cleopatradelights.com)** — Freelance Client

Full-stack e-commerce platform and admin dashboard for an Egyptian-inspired food trailer business.

- 58-item menu with category filtering and custom order form
- Admin dashboard: Google OAuth, KPI charts, order management, customer CRM with lifetime value tracking
- Multi-layer anti-spam: Cloudflare Turnstile, per-IP rate limiting, honeypot fields, timing analysis, content-based spam detection
- SEO with JSON-LD structured data, Egyptian-inspired design system

`Next.js 16` `Prisma` `Supabase` `NextAuth v5` `Cloudflare Turnstile` `Zod`

</td>
</tr>
<tr>
<td width="50%">

**[Dr Dan's No BS Protein](https://dr-dans-protein.vercel.app)** — Freelance Client

Brand website for a protein supplement company, designed and deployed end-to-end.

- Conversion-focused landing page with scroll-driven animations
- Product showcase, trust marquee, waitlist capture
- Responsive across all breakpoints

`Next.js 16` `TypeScript` `Tailwind v4` `shadcn/ui` `Framer Motion`

</td>
<td width="50%">

**[ResumeAI](https://resume-rebuilder-cursor.vercel.app)** — Personal Project

AI-powered resume optimizer that rewrites resumes to match job descriptions without fabricating qualifications.

- Keyword matching and job description analysis
- Strict truth mode — enhances without inventing
- LLM integration via OpenRouter

`Next.js 14` `TypeScript` `OpenRouter` `Tailwind CSS`

</td>
</tr>
</table>

### Engineering Projects

<table>
<tr>
<td width="50%">

**ASGARD** — AI Trading Agent (16,000+ lines)

Production trading system with a Discord interface that scans prediction markets, runs multi-LLM analysis, and executes real-money trades on Polymarket. Built from scratch — trading engine, CLI terminal, and Discord bot.

- **Multi-LLM pipeline**: local Ollama (qwen2.5 7b) pre-filters markets before Claude deep analysis — cost optimization pattern used by production AI companies
- **5-hook intelligence layer**: market classification, query optimization, news relevance scoring (0-10), VRDM gap tracking, cross-session HNSW memory recall
- **Risk management suite**: circuit breaker, position sizer, stop loss, take profit, volatility gate
- **Live trading**: real money on Polymarket via CLOB API with $50 safety cap, confirmation flow, 30s timeout
- **Security audited**: AI agents audited the codebase, found 5 critical vulns (SSRF, race conditions, permission escalation) — all patched
- **MIMIR memory**: episodic + semantic memory with temporal supersession — the bot remembers previous scans and evolves its analysis
- 9 Discord slash commands, 4-tier RBAC, per-user portfolios, Firecrawl web scraping, fighter stats enrichment

`Python` `asyncio` `Discord.py` `Claude API` `Ollama` `Tavily` `Firecrawl` `SQLite` `Polymarket CLOB`

</td>
<td width="50%">

**Throne** — Multi-Agent AI Orchestration (14,000+ lines)

Self-evolving multi-agent orchestration system with genetic algorithm prompt evolution, swarm immune system, trust contagion networks, and constitutional evolution. 47 source files, 7 SQLite tables, 53+ tests.

- TAQL quality assessment + democratic voting + trust tiers
- Prompt DNA: genetic algorithm evolving prompts using fitness scoring
- Swarm Immune System: 5-rule anomaly detection + quarantine
- Trust Contagion: social graph propagation with toxic pair detection
- HNSW vector search (pure JS, no external dependencies)
- 50+ MCP tools exposed via Model Context Protocol server

`Node.js` `SQLite` `better-sqlite3` `Zod` `Pino` `EventEmitter3`

</td>
</tr>
</table>

---

### What I Bring

- **Production track record** — every project listed serves real businesses with real users or trades real money
- **Full-stack ownership** — I handle design, frontend, backend, database, auth, deployment, and security
- **Trading systems** — built a 16K-line trading agent with multi-LLM pipelines, risk management, and live execution on prediction markets
- **SaaS architecture** — subscription billing, tiered rate limiting, marketplace payments, atomic RPCs, row-level security
- **Web security** — Cloudflare Turnstile CAPTCHA, per-IP rate limiting, honeypot spam traps, timing-based bot detection, content analysis, disposable email blocking. Built and battle-tested against a 43k+ spam attack on a live production site
- **AI integration** — multi-LLM cost optimization (local pre-filter + cloud deep analysis), AI-generated imagery, recipe formatting, resume optimization
- **AI orchestration** — built two separate orchestration systems totaling 30K+ lines: genetic algorithms, immune systems, trust networks, episodic memory
- **3D & interactive** — Three.js, React Three Fiber, WebGL scene management, spring physics animations
- **Custom design systems** — Egyptian dark theme, Frost admin theme, pink glassmorphism, dark void aesthetic
- **Modern tooling** — Next.js 16 App Router, Tailwind v4, Prisma, Auth.js v5, Python asyncio, Discord.py

---

<div align="center">

**Open to opportunities** — junior dev roles, freelance projects, and collaborations

[![Portfolio](https://img.shields.io/badge/lukita--portfolio.com-D4AF37?style=flat-square&logo=googlechrome&logoColor=black)](https://lukita-portfolio.com)
[![Email](https://img.shields.io/badge/lukita@cleopatradelights.com-EA4335?style=flat-square&logo=gmail&logoColor=white)](mailto:lukita@cleopatradelights.com)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Karim_Lukita-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://linkedin.com/in/karim-lukita-0282263a9)

</div>
