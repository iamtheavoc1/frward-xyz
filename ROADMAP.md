---
title: "Roadmap"
labels: ["pinned"]
---

## frward roadmap

This document tracks public roadmap items, requested provider areas, and known product gaps.

## Current focus

- Provider connector stability
- Secure credential connection flow
- Unified model registry
- Dashboard provider management
- Compatible routing surfaces
- Provider failover
- Live provider smoke tests
- Public beta preparation

## In progress

| Area | Status | Notes |
|---|---|---|
| Anthropic Max/Pro quota connect | Waiting | Requires an official subscription-compatible OAuth/gateway path. API-key mode is separate and uses API credits. |
| Provider model discovery | In progress | Model catalogs should be discovered or synced dynamically where providers support it. |
| Billing mode labels | In progress | Dashboard should clearly show API credits, subscription quota, external provider billing, or self-hosted mode. |

## Planned

- Usage analytics
- Model capability filters
- Provider health tracking
- Team accounts
- Billing tiers
- Local helper client
- Additional provider connectors
- Custom provider adapters

## Provider requests

Use the Provider Request issue template.

Helpful details:

```text
Provider: [name]
Website: [URL]
Auth mode: [API key / OAuth / SAML / other]
Status: [public beta / general availability / invite-only]
Required modalities: [text / image / STT / TTS / tools / other]
Use case: [what you'd use it for]
```

## Known limitations

Known limitations are tracked in [`KNOWN-LIMITATIONS.md`](./KNOWN-LIMITATIONS.md).

Key current limitation: Anthropic API-key mode does **not** prove or use Claude Max/Pro subscription quota. API-key mode uses Anthropic API credits/API billing. Subscription quota requires a valid subscription-compatible flow.
