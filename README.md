<h1 align="center">Arben "Ben" Kurti</h1>
<p align="center">
  <b>Full-stack developer · Stockholm 🇸🇪</b><br>
  <i>Four languages, two careers, one stack.</i>
</p>

<p align="center">
  <a href="https://arbenkrt.se"><img src="https://img.shields.io/badge/Portfolio-arbenkrt.se-0A0A0A?style=for-the-badge&logo=vercel&logoColor=white" alt="Portfolio"></a>
  <a href="https://www.linkedin.com/in/arben-k-3216633a6/"><img src="https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"></a>
  <img src="https://img.shields.io/badge/Open%20to-Junior%20Full--Stack%20Roles-2ea44f?style=for-the-badge" alt="Open to work">
</p>

---

### 👋 About

I run a taxi company, **JenBen Transport AB**, and I drive a delivery truck for **Menigo Foodservice AB**. Logistics, deadlines, and no tolerance for things that break at 4am. The code happens in the hours around both, and it is held to the same standard.

I finished the **Front End Developer** programme at Jensen Education, the **Codecademy Full Stack Developer** career path, and a cloud/DevOps internship at **NationDev** that ended in an Applied Tech Diploma. I don't build tutorials. I build things with auth, payments, a database that holds real data, and a deploy pipeline behind them.

- 🚀 **Live with real users:** `minbiz.se`, a multi-tenant SaaS for Swedish trade businesses, and Atelier Eri, a booking platform running a real salon's calendar
- ☁️ AWS three ways: **console → CLI → Terraform**, because knowing *why* the button does what it does matters
- 🐧 At home in Linux, Docker and a terminal — self-hosted servers, VMs, backup-over-SSH, the lot
- 🌍 I work in **Albanian, Greek, Swedish and English** — including Swedish legal and tax documentation
- 🎯 Open to **junior full-stack roles in Stockholm**

---

### 📌 Selected work

#### 🧾 [MinBiz](https://minbiz.se) — multi-tenant SaaS for Swedish trade businesses
`Next.js` `TypeScript` `Supabase (Postgres + RLS + Auth)` `Stripe` `Google Gemini` `@react-pdf/renderer` `Vitest`

Write a quote, the customer accepts it from a public link without an account, it becomes an invoice, and the VAT period comes out ready for Skatteverket — with ROT/RUT deductions modelled in. Tenant isolation is enforced in Postgres by row-level security rather than in application code, with a role plus seven permission booleans per user. Stripe Checkout across three plans, where the plan limits live in both the code and a migration and a test compares the two so the pricing page and the database cannot drift apart. 430 Vitest tests behind a GitHub Actions pipeline (tsc → lint → tests → build), four locales, and GDPR export, deletion and retention purges built in.

#### 🗓️ [Atelier Eri](https://eris-nails.vercel.app) — production booking platform
`Next.js 16` `TypeScript` `Supabase (Postgres + RLS)` `date-fns-tz` `Resend` `next-intl` `Vitest`

Built for a real client who was losing bookings to Instagram DMs. Nobody maintains a list of free times: availability is derived on request from her weekly hours, minus time off, minus what is already booked. Double-booking is impossible by construction — a Postgres exclusion constraint over a `tstzrange` rejects overlapping bookings, so two concurrent requests for the same slot cannot both win. Times are salon-local and converted to UTC only at the boundary, which is the step naive implementations skip before quietly dropping or duplicating an hour twice a year. Confirmations carry an `.ics` invite; Swedish/English throughout.

#### 🛒 [NordCart](https://nordcart.vercel.app) — full-stack e-commerce
`Next.js 16` `TypeScript` `Express 5` `MongoDB Atlas` `Stripe` `Cloudinary` `JWT (httpOnly)`

Two separate deployables: a Next.js frontend on Vercel against an Express 5 REST API on Render. The frontend holds no database access at all. Checkout runs inside a MongoDB transaction, so the order, the stock decrement and the cart clear either all land or none do — idempotent on the Stripe payment id, so a concurrent duplicate resolves to the order that won instead of charging twice. The cart is priced on the server from stored prices, VAT included. Admin uploads go browser→Cloudinary on a short-lived signature with the allowed formats inside the signed payload, so file bytes never touch the API and the signature cannot be replayed for arbitrary types.

#### 🕹️ [RETRO CADE](https://goodretro-game.vercel.app) — browser arcade platform
`Next.js` `TypeScript` `HTML5 Canvas` `Web Audio` `Groq (Llama 3.3)` `Redis` `AWS EC2` `Terraform`

Eleven arcade games hand-built from scratch on Canvas — Pac-Man ghost AI, Tetris, Asteroids physics — around 13,000 lines with no game framework underneath. Server-side AI hint system through the Groq API with the secret key kept off the client. Deployed as infrastructure-as-code with Terraform, nginx and systemd on EC2, with a Redis-backed global leaderboard.

#### ✈️ [Swedavia Flight Tracker](https://github.com/benKrt1/SwedaviaFlightInfo) — REST API service
`FastAPI` `Pydantic` `httpx (async)` `TTL cache` `pytest`

A clean API wrapper around Swedish airport flight data that hides the upstream key and uses TTL caching to cut downstream calls. One shared service layer powers three surfaces: a REST API, a CLI tool and an interactive terminal menu. Full pytest suite with the external API mocked, so the tests run with no network at all.

#### 🚆 [Departure Board](https://github.com/benKrt1/train_API_Project) — live transit board
`Node.js` `Express` `node:sqlite` `XML + REST integration`

Departures and arrivals for Swedish trains from Trafikverket's XML API, and for bus, metro and tram from Trafiklab's ResRobot — one board, each row tagged with its mode. Delay statistics that follow the filtered view, search history in SQLite through Node's built-in driver (no native compilation, no extra packages), and a mock-data fallback so the app still runs without an API key.

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
  <img src="https://img.shields.io/badge/Supabase-3FCF8E?style=flat-square&logo=supabase&logoColor=white">
  <img src="https://img.shields.io/badge/MongoDB-47A248?style=flat-square&logo=mongodb&logoColor=white">
  <img src="https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white">
  <img src="https://img.shields.io/badge/SQLite-003B57?style=flat-square&logo=sqlite&logoColor=white">
  <img src="https://img.shields.io/badge/Tailwind-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white">
  <img src="https://img.shields.io/badge/Stripe-635BFF?style=flat-square&logo=stripe&logoColor=white">
  <img src="https://img.shields.io/badge/Cloudinary-3448C5?style=flat-square&logo=cloudinary&logoColor=white">
</p>
<p>
  <img src="https://img.shields.io/badge/AWS-232F3E?style=flat-square&logo=amazonwebservices&logoColor=white">
  <img src="https://img.shields.io/badge/Terraform-7B42BC?style=flat-square&logo=terraform&logoColor=white">
  <img src="https://img.shields.io/badge/GitHub%20Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white">
  <img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white">
  <img src="https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black">
  <img src="https://img.shields.io/badge/Nginx-009639?style=flat-square&logo=nginx&logoColor=white">
  <img src="https://img.shields.io/badge/Vercel-000000?style=flat-square&logo=vercel&logoColor=white">
  <img src="https://img.shields.io/badge/Render-000000?style=flat-square&logo=render&logoColor=white">
  <img src="https://img.shields.io/badge/Vitest-6E9F18?style=flat-square&logo=vitest&logoColor=white">
  <img src="https://img.shields.io/badge/pytest-0A9EDC?style=flat-square&logo=pytest&logoColor=white">
</p>

---

### 💬 How I work

Secrets go in environment variables. `.gitignore` gets written before the first commit, not after the leak. The invariant goes in the database, not in an application check that races. Tests mock the network so they still pass on a train. If I don't understand something I take it apart until I do — that's the same instinct that had me rebuilding engines before it had me reading stack traces.

<p align="center">
  <sub>Byggd i Stockholm. Open to opportunities — <a href="https://arbenkrt.se">arbenkrt.se</a></sub>
</p>
