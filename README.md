# frward — universal AI router

frward is a closed-source hosted AI router that lets users connect their own provider accounts and access them through one unified endpoint.

This public repository is **not the source code repository**. It exists for bug reports, provider requests, roadmap tracking, public documentation, and security reports.

## What frward does

```
Your app / CLI / agent harness
        ↓
      frward
        ↓
Anthropic | OpenAI-compatible providers | speech providers | image providers | custom providers
```

frward provides:

- one unified API endpoint
- provider account connection
- model routing
- streaming support
- tool/function-call compatibility where supported
- 429/error failover where configured
- provider capability metadata
- multimodal routing where supported
- dashboard-based credential management

## Source code

frward is proprietary and closed-source.

The private source repository contains:

- routing engine
- provider connectors
- credential storage
- billing and limits
- dashboard backend
- deployment configuration
- security-sensitive implementation details

No source code license is granted from this public repository.

## Public repository purpose

Use this repository for:

- bug reports
- provider requests
- feature requests
- roadmap discussion
- security disclosure coordination
- documentation feedback

Do not use this repository for pull requests against the core product. The implementation is private.

## Provider support

frward supports providers through connector modules.

Provider availability depends on:

- the user's connected accounts
- provider API availability
- provider authentication mode
- model capabilities exposed by the provider
- current provider limits and terms

Model lists are not hardcoded in this README because provider catalogs change frequently. frward discovers or syncs available models dynamically where the provider supports it.

## Authentication modes

frward supports multiple connection modes depending on the provider:

| Mode              | Description                                                                  |
| ----------------- | ---------------------------------------------------------------------------- |
| API key           | User connects a provider API key. Usage follows that provider's API billing. |
| OAuth             | User connects through an official provider OAuth flow where available.        |
| Local gateway     | Optional local helper mode for tools that need local credential handling.    |
| Custom credential | Provider-specific auth method where supported.                               |

Provider connection pages inside frward show which billing pool or quota type each mode uses.

## Important Anthropic note

Anthropic API-key mode and Claude subscription quota are not the same thing.

- Anthropic API key mode uses Anthropic API credits or API billing.
- Claude subscription quota requires the appropriate official Claude Code / subscription-compatible flow.
- frward does not ask users to paste local Claude credentials, browser cookies, or copied OAuth tokens.

If a connection mode uses API credits instead of subscription quota, frward labels that clearly in the dashboard.

## Endpoints

frward exposes compatible API surfaces for supported clients and harnesses.

Common endpoint types include:

```
/v1/chat/completions
/v1/messages
/v1/models
```

Exact compatibility depends on the connected provider, selected model, and requested modality.

## Modalities

frward is designed to route across multiple capability types:

- text generation
- chat completion
- streaming responses
- tool/function calling
- speech-to-text
- text-to-speech
- image models
- vision models
- future provider-specific modalities

Not every provider supports every modality.

## Roadmap

Public progress is tracked in the Issues tab.

Current focus:

- provider connector stability
- secure credential connection flow
- unified model registry
- dashboard provider management
- OpenAI-compatible routing
- Anthropic-compatible routing
- provider failover
- live provider smoke tests
- public beta preparation

Planned:

- usage analytics
- model capability filters
- provider health tracking
- team accounts
- billing tiers
- local helper client
- additional provider connectors
- custom provider adapters

## Reporting bugs

Use the Bug Report template and include:

- what you tried to do
- what happened instead
- provider used
- model selected, if relevant
- auth mode used
- request type
- whether streaming was enabled
- approximate time of the issue

Do not include API keys, OAuth tokens, cookies, session IDs, or request contents containing private data.

## Requesting providers

Use the Provider Request template.

Helpful details:

- provider name
- provider docs link
- auth method
- supported API format
- required modalities
- why the provider matters for your workflow

## Security

Do not open public issues for vulnerabilities.

See [`SECURITY.md`](./SECURITY.md) for responsible disclosure.

Never post:

- API keys
- OAuth tokens
- refresh tokens
- browser cookies
- Claude Code credentials
- session IDs
- private request/response bodies

## Status

- Dashboard: https://frward.xyz
- API health: https://frward.xyz/api/health
- Status page: planned

## Legal

frward is proprietary software.

This public repository does not grant permission to copy, redistribute, reverse engineer, resell, or modify the private frward source code.
