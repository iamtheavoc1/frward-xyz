# Security Policy

**Last updated: 2026**

## Supported versions

| Version | Supported          |
| ------- | ------------------ |
| 1.x     | ✅ Currently supported |

## Reporting a vulnerability

If you believe you have found a security vulnerability, please do **not** open a public GitHub issue. Instead, email us directly.

**Please include:**
- Description of the vulnerability
- Steps to reproduce
- Potential impact
- Any suggested fixes (optional)

**Response timeline:** We aim to acknowledge within 48 hours and provide a status update within 7 days.

## Security model

frward.xyz handles sensitive credentials on behalf of users:

- **Provider API keys** are encrypted at rest using AES-256-GCM before storage.
- **OAuth tokens** (when implemented) are never stored by frward — they pass through via official OAuth flows only.
- **No credentials are logged.** frward does not log Authorization headers, token prefixes, or request bodies containing credentials.
- **frward does not pool or share credentials** across users. Each user's credentials are isolated to their own account.
- **Subscription quota passthrough** (Claude Max/Pro): The bearer token sent by Claude Code routes through frward unchanged. frward does not modify, store, or inspect the bearer token — it is forwarded transparently to Anthropic, who handles billing against the subscription quota.

## Credential storage

Provider credentials are encrypted at rest using AES-256-GCM with a per-installation key derived from `ENCRYPTION_KEY` environment variable. The key is never stored in the database.

## Dependency security

We keep dependencies updated and monitor for known vulnerabilities in our dependency tree.

## Limits

frward applies per-user rate limits to prevent abuse. Misuse of the service (e.g., credential sharing, proxying credentials you don't own) is a violation of the Terms of Service and may result in account termination.
