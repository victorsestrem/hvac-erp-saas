# Multi-tenant ERP for HVAC Services (Kateka Clima): Case Study

> Multi-tenant ERP I designed and built for **Kateka Clima**, an HVAC installation and maintenance company.
> **Source code is private.** This repository documents the project; a live walkthrough is available on request.

![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?logo=typescript&logoColor=white)
![Next.js](https://img.shields.io/badge/Next.js-000?logo=nextdotjs)
![Prisma](https://img.shields.io/badge/Prisma-2D3748?logo=prisma)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?logo=postgresql&logoColor=white)
![Redis](https://img.shields.io/badge/Redis%20%2F%20BullMQ-DC382D?logo=redis&logoColor=white)

## What it covers

- **Sales**: quotes and orders.
- **HVAC maintenance plans**: recurring service contracts and scheduling.
- **Finance**, **HR** and **inventory**.
- **Client portal**: customers follow their services and plans online.
- **Multi-tenant**: one platform serving multiple companies with isolated data.

## Architecture

```mermaid
flowchart LR
  P[Client portal] --> APP[Next.js app<br/>UI + API routes]
  U[Staff] --> APP
  APP --> DB[(PostgreSQL<br/>tenant-isolated)]
  APP --> Q[Redis + BullMQ<br/>background jobs]
```

- Next.js full stack with Prisma and PostgreSQL; background jobs (reminders, recurring maintenance, notifications) on Redis/BullMQ.

## My role

Architecture, data modeling, full stack development and deployment.

---
Built by **Victor Sestrem** · [LinkedIn](https://www.linkedin.com/in/victor-sestrem/) · victor-sestrem@hotmail.com
