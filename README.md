<h1 align="center">Arben Kurti</h1>
<p align="center">
  <b>Full-stack developer · Stockholm 🇸🇪</b><br>
  <i>Next.js and TypeScript on the front, Python and Node behind it, Postgres underneath.</i>
</p>

<p align="center">
  <a href="https://www.arbenkrt.se"><img src="https://img.shields.io/badge/Portfolio-arbenkrt.se-0A0A0A?style=for-the-badge&logo=vercel&logoColor=white" alt="Portfolio"></a>
  <a href="https://www.linkedin.com/in/arben-k-3216633a6/"><img src="https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"></a>
  <a href="mailto:arbenkurti42@gmail.com"><img src="https://img.shields.io/badge/Email-Contact-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Email"></a>
  <img src="https://img.shields.io/badge/Open%20to-Junior%20Full--Stack%20Roles-2ea44f?style=for-the-badge" alt="Open to work">
</p>

---

### 👋 About

I still drive a delivery truck full time. The code started in the hours around that job — Codecademy first, then the **Front End Developer** programme at Jensen Education, then a cloud and DevOps internship at **NationDev**, where I found out what happens to code after it leaves my laptop.

I also own a small transport company. That is how I know what small-business paperwork actually costs you, and it is the reason MinBiz exists.

- 🚀 **Live in production:** [minbiz.se](https://minbiz.se) — multi-tenant SaaS for Swedish trade businesses, and [Atelier Eri](https://eris-nails.vercel.app), a booking platform running a real Stockholm studio's schedule
- ☁️ **Cloud:** AWS with CloudFormation and Terraform — infrastructure as code, not console clicking
- 🧪 **Testing:** Vitest and pytest behind CI, because the invariant belongs in the database and the proof belongs in a test
- 🌍 I work in **Swedish and English**, and grew up with **Albanian and Greek**
- 🎯 Open to **junior full-stack roles in Stockholm**

---

### 📌 Selected work

#### 🧾 [MinBiz](https://minbiz.se) — multi-tenant B2B SaaS
`Next.js 15` `TypeScript` `Supabase (Postgres + RLS + Auth)` `Stripe` `Google Gemini` `Vitest` `GitHub Actions`

Live on its own domain for Swedish trade businesses: a quote is accepted by the customer from a public link without an account, becomes an invoice, and the VAT period comes out ready for Skatteverket — with ROT/RUT deduction modelled in.

Tenant isolation is enforced in Postgres by **row-level security** rather than in the application layer, with a role plus seven permission booleans per user. Plan limits live in both the code and a migration, and a test compares the two so the pricing page and the database cannot drift apart. **430 Vitest tests** run behind a GitHub Actions pipeline — `tsc → lint → tests → build`. Four locales (sv · en · el · sq), with GDPR export, deletion requests and retention purges built in.

> 🔒 Private repo — it holds customer and business data I can't publish. Happy to walk through the code in an interview.

#### 🗓️ [Atelier Eri](https://eris-nails.vercel.app) — production booking SaaS · [source](https://github.com/benKrt1/ErisNails)
`Next.js 16` `TypeScript` `Supabase (Postgres + RLS + Auth)` `date-fns-tz` `Resend` `next-intl` `Vitest`

A booking platform for a one-person nail studio in Stockholm that was losing appointments to Instagram DMs. Nobody maintains a list of free times — availability is **derived on request** from her weekly hours, minus time off, minus what is already booked.

Double-booking is impossible by construction: a Postgres **exclusion constraint over a `tstzrange`** rejects overlapping confirmed bookings, so two concurrent requests for the same slot cannot both succeed. The invariant lives in the database, not in an application check that races. The engine itself is one pure function over half-open intervals, which is what puts DST-shifting days and partial time-off under unit tests instead of manual clicking.

#### 🛒 [NordCart](https://nordcart.vercel.app) — full-stack e-commerce · [source](https://github.com/benKrt1/NordCart)
`Next.js 16` `TypeScript` `Express 5` `MongoDB Atlas` `Stripe` `Cloudinary` `JWT (httpOnly)`

Shipped as two separate deployables — a Next.js frontend on Vercel against an Express 5 REST API on Render. The frontend holds no database access at all.

Checkout runs inside a **MongoDB transaction**, so the order, the stock decrement and the cart clear either all land or none do. It is **idempotent on the Stripe payment id**, and a concurrent duplicate resolves to the order that won rather than charging twice. The cart is priced on the server from stored prices — the client can ask to check out, but never says what things cost. Admin image uploads go browser→Cloudinary on a short-lived signature, so file bytes never touch the API.

#### 🕹️ [RETRO CADE](https://goodretro-game.vercel.app) — browser arcade platform · [source](https://github.com/benKrt1/retroGame)
`Next.js` `TypeScript` `HTML5 Canvas` `Web Audio API` `Groq (Llama 3.3)` `Redis` `AWS EC2` `Terraform`

Eleven arcade games hand-built from scratch on Canvas — Pac-Man ghost AI, Tetris, Asteroids physics — around 13,000 lines with no game framework underneath. Deployed as **infrastructure-as-code** with Terraform, nginx and systemd on EC2, with a Redis-backed global leaderboard and a server-side Groq hint system that keeps the API key off the client.

#### ✈️ [Swedavia Flight Tracker](https://github.com/benKrt1/SwedaviaFlightInfo) — REST API service
`FastAPI` `Pydantic` `httpx (async)` `TTL cache` `pytest`

An API wrapper around Swedish airport flight data that hides the upstream key and uses TTL caching to cut downstream calls. One shared service layer powers three surfaces: a REST API, a CLI tool and an interactive terminal menu. The pytest suite mocks the external API, so the tests run with no network at all.

#### 🚆 [Departure Board](https://github.com/benKrt1/train_API_Project) — real-time train departures
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
  <img src="https://img.shields.io/badge/Supabase-3FCF8E?style=flat-square&logo=supabase&logoColor=white">
  <img src="https://img.shields.io/badge/MongoDB-47A248?style=flat-square&logo=mongodb&logoColor=white">
  <img src="https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white">
  <img src="https://img.shields.io/badge/SQLite-003B57?style=flat-square&logo=sqlite&logoColor=white">
  <img src="https://img.shields.io/badge/Tailwind-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white">
  <img src="https://img.shields.io/badge/Stripe-635BFF?style=flat-square&logo=stripe&logoColor=white">
</p>
<p>
  <img src="https://img.shields.io/badge/AWS-232F3E?style=flat-square&logo=amazonwebservices&logoColor=white">
  <img src="https://img.shields.io/badge/Terraform-7B42BC?style=flat-square&logo=terraform&logoColor=white">
  <img src="https://img.shields.io/badge/GitHub%20Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white">
  <img src="https://img.shields.io/badge/Nginx-009639?style=flat-square&logo=nginx&logoColor=white">
  <img src="https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black">
  <img src="https://img.shields.io/badge/Vercel-000000?style=flat-square&logo=vercel&logoColor=white">
  <img src="https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white">
  <img src="https://img.shields.io/badge/Vitest-6E9F18?style=flat-square&logo=vitest&logoColor=white">
  <img src="https://img.shields.io/badge/pytest-0A9EDC?style=flat-square&logo=pytest&logoColor=white">
</p>

<sub>Every badge here is backed by one of the projects above, by <a href="https://www.arbenkrt.se">arbenkrt.se</a>, or by the NationDev diploma. If it is on this list, I can be asked about it.</sub>

---

### 💬 How I work

Put the rule in the database instead of trusting the app to remember it. Write the test before you trust the fix. Secrets go in environment variables and `.gitignore` gets written before the first commit, not after the leak. Tests mock the network so they still pass on a train.

<p align="center">
  <sub>Byggd i Stockholm · <a href="https://www.arbenkrt.se">arbenkrt.se</a></sub>
</p>

