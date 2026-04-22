# DevBot AI — Web Version

AI-powered coding assistant. Code generation and decryption across 8 providers, all in the browser.  
Powered entirely by **puter.js** — no server, no build step, no configuration.

## One-Click Deploy

### Netlify
[![Deploy to Netlify](https://www.netlify.com/img/deploy/button.svg)](https://app.netlify.com/start/deploy?repository=https://github.com/YOUR_REPO)

1. Push this folder to a GitHub/GitLab repo
2. Go to [app.netlify.com](https://app.netlify.com) → "Add new site" → "Import an existing project"
3. Connect your repo — publish directory: `.` — no build command needed
4. Click Deploy ✓

### Vercel
[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https://github.com/YOUR_REPO)

1. Push to GitHub
2. Go to [vercel.com/new](https://vercel.com/new) → Import repo
3. Framework: **Other** — Output directory: `.`
4. Deploy ✓

### Cloudflare Pages
1. Push to GitHub
2. Go to [Cloudflare Dashboard](https://dash.cloudflare.com) → Pages → Create a project
3. Connect repo — Build command: *(empty)* — Build output directory: `.`
4. Deploy ✓

### GitHub Pages
1. Go to repo Settings → Pages
2. Source: Deploy from branch → `main` / `root`
3. Done ✓

### Manual (any static host)
Just upload `index.html` — that's the entire app. Nothing else required.

```bash
# Or serve locally
npx serve .
# or
python3 -m http.server 3000
```

---

## Features
- **8 AI providers** — Anthropic (Claude), OpenAI (GPT-4o), Mistral, Together AI, Fireworks, Cohere, SambaNova, Perplexity
- **2 modes** — Code Generation, Decode/Decrypt
- **puter.js auth** — Sign in once, keys and history persist across sessions
- **File upload** — Attach code or encoded data in Decrypt mode
- **Streaming responses** — Live token-by-token output for native providers
- **One-click copy + download** — Every code block has copy and download buttons
- **Persistent history** — Conversations saved per provider via puter.js KV

## Providers
| Provider | Type | Model |
|----------|------|-------|
| Anthropic | ✅ Native (no key) | claude-sonnet-4-20250514 |
| OpenAI | ✅ Native (no key) | gpt-4o |
| Mistral AI | ✅ Native (no key) | mistral-large-latest |
| Together AI | ✅ Native (no key) | Llama 3.1 70B Turbo |
| Fireworks AI | 🔑 API key | Llama 3.1 70B |
| Cohere | 🔑 API key | Command R+ |
| SambaNova | 🔑 API key | Llama 3.1 70B |
| Perplexity | 🔑 API key | Sonar Large (with web search) |

Native providers work immediately via puter.js with no API key needed.  
API keys for other providers are stored encrypted in puter.js KV storage.

## Files
```
devbot-web/
├── index.html       ← The entire app (single file)
├── netlify.toml     ← Netlify config
├── vercel.json      ← Vercel config
├── wrangler.toml    ← Cloudflare Pages config
├── _redirects       ← Netlify SPA redirects
└── README.md
```
