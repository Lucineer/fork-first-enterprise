# Fork-First Enterprise

> Self-hosted deployment. You own the instance. We provide the hull.

## The Thesis

Enterprise software shouldn't require trust in a vendor. Fork the repo, deploy it yourself, customize it for your organization. The vendor provides updates via upstream merges, not access controls.

## Why Fork-First?

1. **You own the data.** It's in your Cloudflare account, your KV, your R2.
2. **You own the code.** Fork it. Modify it. Break it. Fix it.
3. **You own the deployment.** Your Workers, your domain, your SSL.
4. **Updates are pull, not push.** Merge upstream when you want, how you want.
5. **Exit is trivial.** You already have the code. There's nothing to migrate.

## The Managed Service Fallacy

Most SaaS companies sell you access to your own data on their infrastructure. You pay monthly for the privilege of not looking at the code. When they fail, your business fails.

Fork-first inverts this:
- The code IS the product
- Deployment IS the setup
- Your infrastructure IS the platform
- We provide the pattern, not the prison

## How It Works

```
1. Fork the repo
2. Set up Cloudflare account
3. Run: npx wrangler login && npx wrangler deploy
4. Add your API keys
5. Customize for your organization
6. You're live. You own everything.
```

## The Upgrade Path

```
your-fork/  ←→  upstream/main
     ↑              ↑
     │              │
  your changes    our improvements
     │              │
     └── merge ────┘
         (when you choose)
```

You decide when to merge upstream. You decide what to keep. You decide what to discard.

## Enterprise Features (Built Into the Code)

- **BYOK v2**: Your API keys, your providers. Zero keys in our code.
- **Role-based access**: Admin, editor, viewer. All in the code.
- **Audit logging**: Every action logged to KV. Queryable.
- **Data export**: JSON and Markdown. Always. No lock-in.
- **Custom domains**: Your domain, your SSL, your brand.
- **Multi-tenant**: One fork, many organizations. KV namespaces per tenant.

## The Business Model

We don't sell software. We sell **the ability to stop worrying about software.**

- **Free**: Fork it. Run it. It's open source.
- **Standard ($10/mo)**: Priority support, early features, equipment marketplace access
- **Gold ($50/mo)**: At-cost LLM routing, SLA guidance, architecture consulting
- **Enterprise ($200/mo)**: White-label setup, custom equipment, managed upgrades

The free tier IS the product. If it works for you, great. If you want help, we're here.

## Comparison

| | Traditional SaaS | Fork-First |
|---|---|---|
| Data ownership | Vendor | **You** |
| Code access | No | **Yes** |
| Customization | Limited | **Unlimited** |
| Exit cost | High | **Zero** |
| Vendor lock-in | By design | **Impossible** |
| Updates | Forced | **Optional** |
| Uptime SLA | Their promise | **Your infrastructure** |
| Cost ceiling | Their pricing | **Your compute** |

## The Cocapn Stack

All fleet vessels are fork-first:

- **dmlog-ai**: AI Dungeon Master. Fork → deploy → your DM instance.
- **studylog-ai**: AI classroom. Fork → deploy → your school.
- **makerlog-ai**: Coding agent. Fork → deploy → your dev team.
- **fleet-orchestrator**: Coordination hub. Fork → deploy → your fleet.
- **git-agent**: Autonomous worker. Fork → deploy → your agent.

Each one is a complete, self-contained system. Each one can run independently or together.

## Real-World Examples

### A Professional DM
Forks dmlog-ai. Deploys on their Cloudflare account. Adds their own campaign worlds. Invites players via custom domain. Runs a D&D business on $5/month infrastructure + $0.30/month AI.

### A School District
Forks studylog-ai. Deploys one instance per school. Each school has its own KV namespace (data isolation). Teachers customize curriculum. District manages via fleet-orchestrator.

### A Dev Team
Forks makerlog-ai. Connects to their GitHub org. Each developer gets a personal instance. Team lead gets the orchestrator view. Code review + AI assistance in one workflow.

---

## The Promise

> "If our service goes down, your service doesn't — because it was never our service. It's yours."

That's fork-first. That's the future.

---

*Superinstance & Lucineer (DiGennaro et al.)*

*Part of the Cocapn Architecture series: [Ground Truth](https://github.com/Lucineer/ground-truth) → [The Bridge](https://github.com/Lucineer/the-bridge) → [The Keeper](https://github.com/Lucineer/keepers-architecture) → [The Kernel](https://github.com/Lucineer/kernel-model) → [VESAS](https://github.com/Lucineer/vessel-equipment-agent-skills) → [Kung Fu](https://github.com/Lucineer/I-know-kung-fu) → [Boot Camp](https://github.com/Lucineer/boot-camp) → [Training](https://github.com/Lucineer/training-architecture) → Fork-First*
