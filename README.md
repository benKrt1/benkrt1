<h1 align="center">Arben "Ben" Kurti</h1>
<p align="center">
  <b>Full-stack developer · Stockholm 🇸🇪</b><br>
  <i>Four languages, two careers, one stack.</i>
</p>

<p align="center">
  <a href="https://arbenkrt.se"><img src="https://img.shields.io/badge/Portfolio-arbenkrt.vercel.app-0A0A0A?style=for-the-badge&logo=vercel&logoColor=white" alt="Portfolio"></a>
  <a href="https://linkedin.com/in/YOUR-HANDLE"><img src="https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"></a>
  <img src="https://img.shields.io/badge/Open%20to-Junior%20Full--Stack%20Roles-2ea44f?style=for-the-badge" alt="Open to work">
</p>

---

### 👋 About

I spent years running a transport company and driving trucks across Sweden — logistics, deadlines, and no tolerance for things that break at 4am. Now I build software with the same standard.

I'm finishing the **Full-Stack Engineer program at JENSEN komvux** and shipping production-shaped projects while I do it. I don't build tutorials. I build things with auth, payments, a database that actually holds real data, and a deploy pipeline behind them.

- 🚀 **Live in production:** Atelier Eri, a booking SaaS running on Vercel with real users' schedules in it
- 🔭 **Currently building:** `minbiz.se` — multi-tenant SaaS for small Swedish businesses, in four languages
- ☁️ AWS three ways: **console → CLI → Terraform**, because knowing *why* the button does what it does matters
- 🐧 At home in Linux, Docker and a terminal — self-hosted servers, VMs, GPU boxes, backup-over-SSH, the lot
- 🌍 I work in **Albanian, Greek, Swedish and English** — including Swedish legal and tax documentation
- 🎯 Open to **junior full-stack roles in Stockholm**

---

### 📌 Selected work

#### 🗓️ [Atelier Eri](https://eris-neils.vercel.app) — production booking SaaS
`Next.js` `TypeScript` `Supabase` `PostgreSQL` `Resend` `next-intl` `Vitest`

A live booking platform built around a timezone-aware availability engine — interval math, lead-time buffers and time-off blocks, all covered by unit tests. Admin dashboard for schedule, services and time-off management, automated email confirmations with ICS calendar attachments, and full English/Swedish internationalization with locale routing. ~3k lines of TypeScript, deployed on Vercel.

#### 🧾 [minbiz.se] — multi-tenant SaaS for small businesses *(in development)*
`Next.js App Router` `TypeScript` `PostgreSQL` `Prisma` `Better Auth` `Stripe` `next-intl`

Business administration for small Swedish firms in their own language. Employment contract and quote generation as PDFs, accounting integrations (Fortnox), and an articles section explaining Swedish tax rules. Postgres with Row-Level Security for tenant isolation, decimal types for VAT and amounts, four-language i18n architecture from day one, GDPR-aware EU hosting.

#### 🛒 NordCart — MERN e-commerce platform
`MongoDB` `Express` `React` `Node.js` `Stripe` `Cloudinary` `MongoDB Atlas`

Full storefront: catalogue, cart, Stripe checkout, Cloudinary image uploads, product reviews, wishlist and an admin dashboard. Built in structured phases with strict environment-variable and `.gitignore` discipline throughout.

#### 🕹️ Retro Cade — browser arcade platform
`Next.js` `TypeScript` `HTML5 Canvas` `Web Audio API` `Groq (Llama 3.3)` `Redis` `AWS EC2` `Terraform`

Eleven arcade games hand-built from scratch on Canvas — Pac-Man ghost AI, Tetris, Asteroids physics — around 13,000 lines with no game framework underneath. Server-side AI hint system through the Groq API with the secret key kept off the client. Deployed as infrastructure-as-code with Terraform, nginx and systemd on EC2, with a Redis-backed global leaderboard.

#### ✈️ Swedavia Flight Tracker — REST API service
`FastAPI` `Pydantic` `httpx (async)` `TTL cache` `pytest`

A clean API wrapper around Swedish airport flight data that hides the upstream key and uses TTL caching to cut downstream calls. One shared service layer powers three surfaces: a REST API, a CLI tool and an interactive terminal menu. Full pytest suite with the external API mocked, so the tests run with no network at all.

#### 🚆 Departure Board — real-time train departures
`Node.js` `Express` `SQLite` `XML API integration`

Live departures and delay statistics from Trafikverket's open data. Parses their XML protocol into clean domain objects, keeps a SQLite-backed search history, and falls back gracefully to mock data so the app still runs without an API key.

---

### 🛠️ Tech

<p>
  <img src="https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white">
  <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black">
  <img src="https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black">
  <img src="https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=nextdotjs&logoColor=white">
  <img src="https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white">
  <img src="https://img.shields.io/badge/Express-000000?style=flat-square&logo=express&logoColor=white">
  <img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white">
  <img src="https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white">
  <img src="https://img.shields.io/badge/PHP-777BB4?style=flat-square&logo=php&logoColor=white">
</p>
<p>
  <img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white">
  <img src="https://img.shields.io/badge/MongoDB-47A248?style=flat-square&logo=mongodb&logoColor=white">
  <img src="https://img.shields.io/badge/Supabase-3FCF8E?style=flat-square&logo=supabase&logoColor=white">
  <img src="https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white">
  <img src="https://img.shields.io/badge/SQLite-003B57?style=flat-square&logo=sqlite&logoColor=white">
  <img src="https://img.shields.io/badge/Tailwind-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white">
  <img src="https://img.shields.io/badge/Stripe-635BFF?style=flat-square&logo=stripe&logoColor=white">
</p>
<p>
  <img src="https://img.shields.io/badge/AWS-232F3E?style=flat-square&logo=amazonwebservices&logoColor=white">
  <img src="https://img.shields.io/badge/Terraform-7B42BC?style=flat-square&logo=terraform&logoColor=white">
  <img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white">
  <img src="https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black">
  <img src="https://img.shields.io/badge/Nginx-009639?style=flat-square&logo=nginx&logoColor=white">
  <img src="https://img.shields.io/badge/Vercel-000000?style=flat-square&logo=vercel&logoColor=white">
  <img src="https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white">
  <img src="https://img.shields.io/badge/pytest-0A9EDC?style=flat-square&logo=pytest&logoColor=white">
</p>

---

### 💬 How I work

Secrets go in environment variables. `.gitignore` gets written before the first commit, not after the leak. Tests mock the network so they still pass on a train. If I don't understand something I take it apart until I do — that's the same instinct that had me rebuilding engines before it had me reading stack traces.

<p align="center">
  <sub>Byggd i Stockholm. Open to opportunities — <a href="https://arbenkrt.vercel.app/sv">arbenkrt.vercel.app</a></sub>
</p>
