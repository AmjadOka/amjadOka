[github-README.md](https://github.com/user-attachments/files/28444298/github-README.md)
<div align="center">

# Amjad AbuNasser

**Senior Software Engineer · Backend Systems · Palestine 🇵🇸**

[![Email](https://img.shields.io/badge/amjad392q@gmail.com-EA4335?style=flat&logo=gmail&logoColor=white)](mailto:amjad392q@gmail.com)
[![GitHub](https://img.shields.io/badge/@AmjadOka-181717?style=flat&logo=github&logoColor=white)](https://github.com/AmjadOka)

</div>

---

I build **production-grade backend systems** — the kind where correctness matters, concurrency is real, and the codebase still makes sense six months later.

My focus is distributed architecture, financial-grade data integrity, and real-time systems. I care about things most engineers skip: cache invalidation strategies, pessimistic lock placement, decimal precision in financial columns, token lifecycle management, and the difference between a well-designed module boundary and one that will rot.

Currently building [**Mahaseel**](https://github.com/AmjadOka) — a full-stack B2C agricultural marketplace connecting Palestinian farmers directly with buyers, with live auctions, a merchant wallet with hold-and-release payout logic, and a multi-channel real-time notification system.

---

## What I Work With

**Core**

![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat&logo=typescript&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat&logo=nodedotjs&logoColor=white)
![NestJS](https://img.shields.io/badge/NestJS-E0234E?style=flat&logo=nestjs&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat&logo=postgresql&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat&logo=redis&logoColor=white)

**Infrastructure & Tooling**

![BullMQ](https://img.shields.io/badge/BullMQ-FF6B6B?style=flat)
![Socket.io](https://img.shields.io/badge/Socket.io-010101?style=flat&logo=socketdotio&logoColor=white)
![Stripe](https://img.shields.io/badge/Stripe-635BFF?style=flat&logo=stripe&logoColor=white)
![Cloudinary](https://img.shields.io/badge/Cloudinary-3448C5?style=flat&logo=cloudinary&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white)

**Frontend**

![React](https://img.shields.io/badge/React-61DAFB?style=flat&logo=react&logoColor=black)
![Next.js](https://img.shields.io/badge/Next.js-000000?style=flat&logo=nextdotjs&logoColor=white)

---

## Featured Work

### Mahaseel — Agricultural Marketplace Platform
> Full-stack B2C platform · NestJS · PostgreSQL · Redis · Stripe · Socket.io

A production-level marketplace built for Palestinian farmers and buyers. The system handles two sale models (fixed-price and live auctions), a three-balance merchant wallet with hold-and-release payout logic, and a real-time notification system across WebSocket, SSE, and email channels.

**Architecture highlights:**
- **Auth system** — JWT access + refresh token rotation, Redis blacklisting per `jti`, `tokenVersion` for global session invalidation, Google OAuth with `httpOnly` cookie flow
- **Wallet engine** — `pendingBalance → availableBalance` release cycle, all mutations under `pessimistic_write` locks, full transaction audit trail, double-processing prevention on withdrawal approval/rejection
- **Cache layer** — version-key pattern for paginated caches (no key scanning), targeted bust-and-rewarm on every write, cross-module cache invalidation (ratings bust user stats)
- **Notification pipeline** — EventEmitter2 → Listener → Dispatcher → WebSocket + SSE + Email in parallel via `Promise.allSettled`, unread badge count re-warmed as a cache side-effect
- **Admin module** — 9 sub-controllers covering full platform oversight: farm approval workflow, user suspension, force order actions, withdrawal processing, broadcast notifications, revenue reports, and an immutable audit log

---

## Things I Think About

**Data integrity over convenience.**
Financial columns need transformers. Nullable decimals should stay null. A `0` where `null` belonged has broken more payout logic than any off-by-one error.

**Concurrency is not an edge case.**
Any write to shared state that doesn't hold a pessimistic lock is a race condition waiting for production load to find it.

**Cache invalidation is an architecture decision.**
TTL alone is a bet that staleness won't matter. Version-key patterns, targeted bust-and-rewarm, and short TTLs on paginated data are deliberate choices — not afterthoughts.

**Security is in the defaults.**
`select: false` on sensitive columns. `ParseUUIDPipe` on every `:id`. Raw body for Stripe webhooks — never `JSON.stringify(req.body)`. `@Max()` on pagination limits. The goal is to make the insecure path harder than the secure one.

---

## Currently

- 🔨 Shipping Mahaseel to production
- 📖 Going deeper on distributed systems and event-driven architecture
- 🌍 Building technology that serves underrepresented communities

---

<div align="center">

*Based in Nablus, Palestine · Open to remote opportunities*

</div>
