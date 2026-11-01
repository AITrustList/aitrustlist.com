<div align="center">

  <img src="https://aitrustlist.com/logo.svg" alt="AITrustList Logo" width="80" height="80" />

  # AITrustList.com

  **The Curated AI Tools Directory & Telemetry Radar Ranked by Real Traffic Signals**

  [![Website](https://img.shields.io/badge/Website-aitrustlist.com-10b981?style=for-the-badge&logo=google-chrome&logoColor=white)](https://aitrustlist.com)
  [![Next.js](https://img.shields.io/badge/Next.js_16-000000?style=for-the-badge&logo=next.js&logoColor=white)](https://nextjs.org/)
  [![Cloudflare Workers](https://img.shields.io/badge/Cloudflare_Workers-F38020?style=for-the-badge&logo=cloudflare&logoColor=white)](https://workers.cloudflare.com/)
  [![Drizzle ORM](https://img.shields.io/badge/Drizzle_ORM-C5F74F?style=for-the-badge&logo=drizzle&logoColor=black)](https://orm.drizzle.team/)
  [![TypeScript](https://img.shields.io/badge/TypeScript_5-3178C6?style=for-the-badge&logo=typescript&logoColor=white)](https://www.typescriptlang.org/)
  [![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=for-the-badge)](LICENSE)

  <p align="center">
    <a href="https://aitrustlist.com">Explore Directory</a> •
    <a href="https://aitrustlist.com/radar">Growth Radar</a> •
    <a href="https://aitrustlist.com/deals">Lifetime Deals</a> •
    <a href="https://aitrustlist.com/submit">Submit AI Product</a> •
    <a href="https://aihuntlist.com">AIHuntList Sister Hub</a>
  </p>

</div>

---

## 🌟 About AITrustList

Thousands of AI tools launch every month, but most directories either list everything indiscriminately or only surface whoever pays the highest ad fee. 

**[AITrustList](https://aitrustlist.com)** takes a principled, data-first approach: **Rank by independent traffic signals, benchmark by hand.** 

Every featured product is evaluated through real adoption metrics (monthly visits, growth rate, bounce rate, traffic source distribution), followed by editorial verification with objective pros and cons.

---

## 🚀 Key Features

### 📊 1. Verified Traffic Telemetry & Growth Radar
* Real-world traffic telemetry powered by independent traffic signals (Similarweb integration).
* Multi-dimensional rankings:
  * **Monthly Visits**: Absolute scale and adoption.
  * **Month-over-Month (MoM) Growth Radar**: Spot breakout AI innovations early.
  * **Geographic & Channel Breakdown**: Direct, organic search, and social referral distribution.

### 🎯 2. 3-Level Deep Workflow Taxonomy
* Over **300+ categorized workflow tasks** (e.g., `Coding Agents`, `Video Generation`, `AI SEO Automation`, `Voice Cloning`).
* Strict hierarchy (`Level 1 Category → Level 2 Capability → Level 3 Task`) ensuring targeted discovery instead of generic lists.

### ⚖️ 3. Editorial Reviews & Side-by-Side Alternatives
* Balanced editorial review with honest pros, cons, and real pricing models (`Free`, `Freemium`, `Paid`, `Open Source`).
* Algorithmic and editorial alternative engines (`Alternative to ChatGPT`, `Alternative to Cursor`, `Alternative to Midjourney`).

### 💰 4. Curated Software Lifetime Deals (LTD)
* Dedicated deals portal tracking active, verified lifetime discounts and founder early-bird pricing.
* Filter by discount rate, expiration date, and verified buyer reviews.

### 🛡️ 5. Official Trust Badge & Backlink Network
* Official lightweight embeddable badge generator with static SVGs (0 Worker CPU execution cost).
* Provides verified dofollow backlinks and instant founder verification badges for indexed products.
* Ecosystem distribution with sister directory **[AIHuntList](https://aihuntlist.com)**.

---

## 🏗️ Technical Architecture & Stack

AITrustList is built for extreme edge performance, sub-second global page loads, and multi-tenant high scalability:

| Layer | Technology | Description |
| :--- | :--- | :--- |
| **Framework** | [Next.js 16](https://nextjs.org/) (App Router) | React 19 Server Components, Streaming SSR, and Static Site Generation |
| **Runtime & Edge** | [Cloudflare Workers](https://workers.cloudflare.com/) via [OpenNext](https://opennext.js.org/cloudflare) | Sub-50ms global cold starts, zero-server maintenance, distributed edge caching |
| **Database** | [PostgreSQL (Neon Serverless)](https://neon.tech/) | Serverless connection pooling, transactional reliability, edge-ready latency |
| **ORM & Migrations** | [Drizzle ORM](https://orm.drizzle.team/) & Drizzle Kit | Fully type-safe schema definitions and zero-overhead queries |
| **Authentication** | [Better-Auth](https://better-auth.com/) | Email magic links, Google OAuth, GitHub OAuth, session management |
| **Styling & UI** | [Tailwind CSS v4](https://tailwindcss.com/) + Radix UI | Dark/light theme engine, responsive micro-animations, accessible primitives |
| **Internationalization** | [next-intl](https://next-intl-docs.vercel.app/) | Locale routing (`/en`, `/zh`, etc.) and structured i18n messages |
| **Payments & Billing** | [Stripe](https://stripe.com/) | Automated submission fee collection, sponsorships, and webhook fulfillment |

---

## ⚡ Quick Start for Developers

### Prerequisites
* **Node.js** >= 20.x
* **pnpm** >= 10.x (recommended: pnpm 12+)
* **Cloudflare Wrangler CLI** (for edge deployment)

### 1. Clone & Install

```bash
git clone https://github.com/aitrustlist/aitrustlist.com.git
cd aitrustlist.com
pnpm install
```

### 2. Configure Environment Variables

Copy the example environment file:

```bash
cp .env.example .env.local
```

Fill in your secrets:

```env
# Database
DATABASE_URL="postgres://user:password@host/database?sslmode=require"

# Authentication (Better-Auth)
BETTER_AUTH_SECRET="your-32-character-secret"
BETTER_AUTH_URL="http://localhost:3000"
GOOGLE_CLIENT_ID="your-google-oauth-client-id"
GOOGLE_CLIENT_SECRET="your-google-oauth-client-secret"
AUTH_GITHUB_CLIENT_ID="your-github-oauth-client-id"
AUTH_GITHUB_CLIENT_SECRET="your-github-oauth-client-secret"

# App & Public URLs
NEXT_PUBLIC_APP_URL="http://localhost:3000"

# Billing (Stripe)
STRIPE_API_KEY="sk_test_..."
STRIPE_WEBHOOK_SECRET="whsec_..."
```

### 3. Database Migration

```bash
# Push schema to development database
pnpm db:push

# Launch Drizzle Studio GUI (optional)
pnpm db:studio
```

### 4. Run Development Server

```bash
pnpm dev
```

Open [http://localhost:3000](http://localhost:3000) to view the application.

---

## 📦 Edge Build & Deployment (Cloudflare Workers)

AITrustList compiles to an ultra-efficient Cloudflare Worker bundle using OpenNext:

```bash
# Compile and build Next.js application for Cloudflare Workers
pnpm cfbuild

# Preview worker locally via workerd runtime
pnpm preview

# Deploy directly to Cloudflare edge
pnpm deploy
```

---

## 🏅 Official Badge Integration

If your product is listed on AITrustList, you can embed the official verified badge into your landing page or README:

### HTML Embed:

```html
<a href="https://aitrustlist.com/ai/your-product-slug" target="_blank" rel="noopener">
  <img 
    src="https://aitrustlist.com/badge-dark.svg" 
    alt="Featured on AITrustList" 
    height="54" 
  />
</a>
```

### Markdown Embed:

```markdown
[![Featured on AITrustList](https://aitrustlist.com/badge-dark.svg)](https://aitrustlist.com/ai/your-product-slug)
```

*(You can also use our NPM package: `pnpm add aitrustlist-badge`)*

---

## 🤝 Ecosystem & Partners

* 🌐 **[AITrustList Official](https://aitrustlist.com)** — Curated AI tools directory with verified traffic signals.
* 🚀 **[AIHuntList](https://aihuntlist.com)** — Comprehensive AI navigation portal with 3,000+ categorized AI apps.
* 📝 **[Submit Your AI](https://aitrustlist.com/submit)** — Apply for editorial review, traffic verification, and featured placement.
* 🤝 **[Partnership Inquiries](https://aitrustlist.com/partners)** — Joint marketing, data licensing, and link exchanges.

---

## 📄 License

This project is licensed under the [MIT License](LICENSE).

---

<div align="center">
  <sub>Built with ❤️ by the AITrustList Engineering & Editorial Team.</sub>
</div>

