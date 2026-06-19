# frward.xyz

**Issues, roadmap, docs, and security reports for [frward.xyz](https://frward.xyz).**

frward.xyz is a hosted AI provider router — connect your own API keys and subscription accounts, route requests through one endpoint, with automatic failover and multi-provider aggregation.

## What this repo is for

- 🐛 **Bug reports** — Something's broken? Open an issue.
- 📡 **Provider requests** — Want support for a new AI provider? Open an issue.
- 🗺️ **Roadmap** — Feature planning and status lives here.
- 🔒 **Security** — See [SECURITY.md](./SECURITY.md) for our security policy and contact.

## What this repo is NOT

- ❌ **Source code** — The frward source code is proprietary and private.
- ❌ **Public API documentation** — For API docs, see [frward.xyz](https://frward.xyz).

## Quick links

| Topic | Link |
|-------|------|
| Website | [frward.xyz](https://frward.xyz) |
| Privacy Policy | [frward.xyz/privacy](https://frward.xyz/privacy) |
| Terms of Service | [frward.xyz/terms](https://frward.xyz/terms) |
| Security policy | [SECURITY.md](./SECURITY.md) |

## Supported providers

| Provider | Status | Auth mode | Billing |
|----------|--------|-----------|---------|
| Anthropic | ✅ Available | API key | API credits |
| Anthropic (Max/Pro OAuth) | 🔜 Coming soon | OAuth | Subscription quota |
| OpenAI | ✅ Available | API key | API credits |
| Google AI | ✅ Available | API key | API credits |
| Groq | ✅ Available | API key | API credits |
| DeepSeek | ✅ Available | API key | API credits |
| xAI (Grok) | ✅ Available | API key | API credits |
| MiniMax | ✅ Available | API key | API credits |
| z.ai (GLM) | ✅ Available | API key | API credits |
| Ollama (local) | ✅ Available | — | Self-hosted |
| AWS Bedrock | ✅ Available | API key | AWS billing |
| Azure OpenAI | ✅ Available | API key | Azure billing |
| + more | | | |

> **Note:** "Claude Max/Pro quota connect" via OAuth is coming soon — requires Anthropic's official OAuth approval. API key mode is available now and uses Anthropic API credits.
