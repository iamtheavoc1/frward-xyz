---
title: "Known Limitations"
labels: "pinned"
---

## Current known limitations

| # | Limitation | Impact | Workaround |
|---|-----------|--------|------------|
| 1 | Anthropic Max/Pro OAuth not yet available | Subscription quota passthrough requires official OAuth approval from Anthropic | Use API key mode (uses API credits) or Claude Code direct login until OAuth is approved |
| 2 | Ollama requires manual model config | frward can't auto-discover local Ollama models | Set `OLLAMA_HOST` to your Ollama endpoint manually |
| 3 | AWS Bedrock / Azure OpenAI require external credential setup | These use their cloud billing consoles | Configure credentials in AWS Bedrock or Azure portal |
| 4 | Live smoke tests require real API keys | CI runs only mocked tests | Set env vars locally to run `npm run test:live` |
| 5 | Provider model lists are not hardcoded | frward discovers models dynamically | Model catalog depends on provider API availability |

## How to report a new limitation

Open a bug report and label it `limitation`. Include:

- what you expected to work
- what happened instead
- provider and auth mode used
- approximate time of issue
