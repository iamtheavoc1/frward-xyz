---
title: "Provider Requests & Known Limitations"
labels: ["pinned"]
---

## 🗺️ frward roadmap — provider requests and known gaps

This issue is pinned to track requested providers and known limitations.

---

### 🔜 In progress

| Provider | Auth mode | Notes |
|----------|-----------|-------|
| Anthropic OAuth (Max/Pro) | OAuth | Waiting on Anthropic official OAuth approval |

---

### 📋 Provider request template

Want a new provider? Comment on this issue with:

```
Provider: [name]
Website: [URL]
Auth mode: [API key / OAuth / SAML / other]
Status: [public beta / general availability / invite-only]
Use case: [what you'd use it for]
```

---

### ⚠️ Known limitations

| Limitation | Impact | Workaround |
|-------------|--------|------------|
| Anthropic Max/Pro OAuth not yet available | Subscription quota passthrough requires API key (uses API credits instead) | Use Claude Code's direct login until OAuth is approved |
| Ollama requires manual model config | frward can't auto-discover local Ollama models | Set `OLLAMA_HOST` to your Ollama endpoint |
| AWS Bedrock / Azure OpenAI require manual credential setup | These providers use external billing consoles | Configure credentials in the respective cloud consoles |
| Live smoke tests require real API keys | CI runs only mocked tests | Set env vars locally to run live tests: `npm run test:live` |

---

*This issue is updated as providers are added and limitations are resolved.*
