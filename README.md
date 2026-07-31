# Amjad — Backend Developer (NestJS)

Software Engineering student and NestJS backend developer based in Palestine, building production-grade systems in Arabic-language contexts: an accounting/inventory ERP, an agricultural marketplace, and a family-management platform.

[Email](mailto:amjad392q@gmail.com) · [LinkedIn](https://www.linkedin.com/in/amjad-abunasser-983195251/) · [GitHub](https://github.com/amjadOka)

---

## Stack

`NestJS` `TypeScript` `TypeORM` `PostgreSQL` `MongoDB / Mongoose` `Redis` `BullMQ` `WebSockets` `Stripe` `Docker` `React` `GraphQL` `Tailwind (RTL/Arabic UI)`

---

## Featured Projects

### 🧾 ERP System — Accounting & Inventory for Local Merchants

Multi-module ERP for local merchants to manage large-scale purchases, sales, and stock — built end-to-end (backend + Arabic RTL frontend).

- **FIFO lot-based inventory** (`StockLot`, `LotConsumption`, `FifoService`) with quantity/cost correction tooling
- **Double-entry ledger engine** (`LedgerService.append()`) with deterministic ordering via a Postgres sequence
- Full reporting suite: profitability (`lotProfitReport`), trial balance, account statements, stock summary, cash box, and party movement reports — with PDF export and Excel Detailed
- Invoice/payment voiding with full stock and ledger reversal, party reassignment, and profit distribution (draft/post/cancel workflow with partner share history)
- Frontend: React + Tailwind, Arabic RTL, shared `Table` / `Modal` / `KpiStrip` / `PrintDocument` components

**Stack:** NestJS · TypeORM · PostgreSQL · React · Tailwind

---

### 🌾 Mahaseel — Digital Agricultural Marketplace

Training project at Avatar Company for Training and Development — a marketplace connecting agricultural producers and buyers across Palestine.

- Auction system: bid-to-order flow with BullMQ background workers
- Stripe payment integration with webhook handling; wallet/escrow system
- Category tree management with Redis caching
- Full admin module audit and rewrite
- Ratings system with composite constraints and flag/report handling
- Event-driven notifications: in-app (WebSocket), push (FCM), and email, fanned out from a single dispatcher

**Stack:** NestJS · TypeORM · PostgreSQL · Redis · BullMQ · Stripe

---

### 👨‍👩‍👧 Smart Family — Family Management Backend

Main project of a back-end trainee program at BBD agency.

- NestJS/Fastify backend on MongoDB/Mongoose, deployed to a DigitalOcean VPS via Docker Compose (replica sets with keyfile auth, Redis, swap-tuned for low-RAM droplets)
- Google & Apple OAuth, JWT auth with refresh token rotation
- Rewards/points ledger with dashboard aggregation
- Realtime WebSocket gateway, FCM push notifications with multi-device token management, BullMQ reminder scheduling
- Statistics module with AI-generated insights (Anthropic/Groq)
- Led a code audit that caught duplicate routes, missing DI, ReDoS-vulnerable regex queries, and a routing bug

**Stack:** NestJS · Fastify · MongoDB · Docker · Redis

---

### 🏕️ WildStay — Cabin Rental Platform

Full-stack booking platform: frontend + backend built separately.

- Frontend: React 18/19, TypeScript, Vite, GraphQL, Zustand, React Query
- Backend: NestJS, GraphQL, MongoDB — booking scheduling, role-based access control, cron-based booking expiry

**Stack:** NestJS · GraphQL · MongoDB · React · Vite

---

## Currently

Looking for backend (NestJS) or full-stack remote opportunities — open to full-time and freelance/contract work.
