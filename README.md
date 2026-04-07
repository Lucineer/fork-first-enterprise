# Fork-First Enterprise
You don't rent software. You build on it.

Enterprise software often prioritizes vendor lock-in over your operational needs. Fork-First Enterprise inverts that model. This is an open-source agent runtime and fleet protocol you deploy on your infrastructure. You own the code and data; you control updates and customization.

## The Problem
Vendor roadmaps change, prices increase, and critical features can be deprecated, leaving your team without solutions you relied on. Traditional SaaS gives you access, not ownership.

## The Solution
Fork this repository. Deploy it to your Cloudflare account. You own the entire instance—code, data, and deployment. We publish improvements; you choose if and when to merge them. There are no backdoors, kill switches, or mandatory upgrades.

## Quick Start
Deploy your own instance in minutes:
1.  Fork this repository.
2.  Log into your Cloudflare account and run `npx wrangler deploy`.
3.  Configure environment variables for your API keys.

Your instance is now live on your domain, using your Cloudflare resources (Workers, KV, R2). No one else has access.

## How It Works
This is a fork-first model. Your deployment is independent.
```
your-fork  ←→  upstream/main
    │               │
your changes   our improvements
    └───── merge when ready ─────┘
```
You maintain full control. Merge upstream updates on your schedule, adopting what's useful for your team.

## Core Features
All features are available in the open-source repository.
- **Complete Data Ownership**: Data resides solely in your Cloudflare KV and R2 storage.
- **BYOK (Bring Your Own Keys)**: All API keys remain in your environment variables.
- **Role-Based Access**: Built-in roles (Admin, Editor, Viewer) that you can extend.
- **Audit Logging**: Immutable action logs written to your KV store.
- **Custom Branding**: Use your domain, SSL certificates, and logos.
- **Multi-Tenancy**: Isolate data using separate KV namespaces.

## One Honest Limitation
As the maintainer of your fork, you are responsible for operational maintenance, security updates, and merging upstream changes. This grants you control but requires active stewardship.

## Attribution
Fork-First Enterprise is part of the Cocapn Fleet.  
Maintained by Superinstance & Lucineer (DiGennaro et al.).

---
<div>
  <a href="https://the-fleet.casey-digennaro.workers.dev">The Fleet</a> |
  <a href="https://cocapn.ai">Cocapn.ai</a>
</div>