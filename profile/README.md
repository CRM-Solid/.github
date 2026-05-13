<div align="center">

# CRM Solid

**Omnichannel AI CRM for modern customer-facing teams.**

Talk to customers on Telegram, X, Email, Live Chat and via Bot — from one inbox, one pipeline, one API.

[Website](https://crmsolid.com) · [App](https://app.crmsolid.com) · [API Docs](https://crmsolid.com/docs) · [Status](https://health.crmsolid.com)

</div>

---

## What CRM Solid is

CRM Solid is an omnichannel customer relationship platform that unifies five conversation channels behind one CRM:

- **Telegram** — multi-account, scraping, sequences, broadcasting
- **X / Twitter** — DMs and account management
- **Email** — per-user inbox, threading, templates
- **Live Chat** — embeddable web widget for your site
- **Bot** — programmable conversational workflows

On top of the inbox sit AI-powered lead scoring, automated outreach sequences, a public REST API, and an MCP server so AI agents can drive the CRM directly.

## Channels & capabilities

| Area | What ships today |
|---|---|
| Inbox | Telegram, X/Twitter, Email, Live Chat, Bot — all in one pane |
| Pipeline | Drag-and-drop stages, archive/restore, notes |
| Outreach | Sequences, broadcasting, spintax, scheduling |
| AI | Lead scoring, message analysis, reply suggestions |
| Billing | LemonSqueezy + WeePay, per-plan limits |
| Real-time | SignalR streams for inbox + job status |
| Reliability | Rate limiting with flood-wait backoff, proxy support |

## Developer surface

| Product | What it is | Status |
|---|---|---|
| Public REST API v1 | Bearer-key + scoped endpoints for contacts, messages, sequences, accounts | Stable |
| Webhooks | Outbound events for inbound messages, job status, billing | Stable |
| MCP server | Lets AI agents (Claude, custom agents) drive the CRM via the Model Context Protocol | Planned |
| OpenAPI spec | Machine-readable definition of the public API | Published in-product |

## SDKs

| SDK | Language | Status | Repo |
|---|---|---|---|
| `crmsolid-dotnet` | C# / .NET 8+ | Alpha | [CRM-Solid/crmsolid-dotnet](https://github.com/CRM-Solid/crmsolid-dotnet) |
| `crmsolid-python` | Python 3.10+ | Planned | _coming soon_ |
| `crmsolid-node` | TypeScript / Node 20+ | Planned | _coming soon_ |
| `crmsolid-mcp` | TypeScript (MCP server reference) | Planned | _coming soon_ |

## Get started

### 1. Create an API key

Sign in to https://app.crmsolid.com, open **Settings → Developers**, and generate a key. Each key is scoped — pick the smallest scope that matches your use case.

### 2. Install a SDK (example: .NET)

```bash
dotnet add package CrmSolid
```

```csharp
using CrmSolid;

var client = new CrmSolidClient("csk_live_...");

var page = await client.Contacts.ListAsync(limit: 50);

foreach (var c in page.Items)
{
    Console.WriteLine($"{c.Id}\t{c.Name}\t@{c.Username}");
}
```

> The .NET SDK is in alpha. The package name and exact API may change before v1.0.

### 3. Read the docs

Full REST reference, webhooks, and authentication: https://crmsolid.com/docs

## Open-source repositories

| Repo | Purpose | Status |
|---|---|---|
| [`.github`](https://github.com/CRM-Solid/.github) | Org profile, community health files | Live |
| [`crmsolid-dotnet`](https://github.com/CRM-Solid/crmsolid-dotnet) | Official .NET SDK | Alpha |
| `crmsolid-python` | Official Python SDK | Planned |
| `crmsolid-node` | Official Node.js / TypeScript SDK | Planned |
| `crmsolid-mcp` | MCP server reference implementation | Planned |
| `crmsolid-docs` | Public docs site source | Planned |
| `crmsolid-openapi` | OpenAPI spec mirror + generator | Planned |
| `crmsolid-examples` | End-to-end examples across SDKs | Planned |

Stars and issues on these repos are welcome once they ship.

## Stay in touch

- Website — https://crmsolid.com
- App — https://app.crmsolid.com
- Docs — https://crmsolid.com/docs
- Support — info@crmsolid.com
- Security — info@crmsolid.com _(dedicated security@ inbox coming soon)_
- X / Twitter — [@crmsolid](https://x.com/crmsolid)
