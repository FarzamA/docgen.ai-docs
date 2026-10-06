# ⚙️ Setup Instructions

> NOTE: The DocGen.AI source code is currently private. This page describes how the stack is run, for reference.

## Using the live demo

1. Open [docgen.4zam.dev](https://docgen.4zam.dev/login) and continue as a guest.
2. Click **API keys** and add a key for at least one provider:
    - OpenAI: platform.openai.com/api-keys
    - Anthropic: console.anthropic.com
    - Google Gemini: aistudio.google.com/apikey
3. Start a new chat, pick a provider and model and ask away.

Keys stay in your browser (cleared when the tab closes unless you choose "Remember on this device") and are removed when you log out.

## Requirements (self-hosting)

- Docker + Docker Compose
- A CPU-only host is enough: LLM inference runs at the providers and embeddings use a small CPU model

## Production stack

```bash
cp .env.example .env    # fill in POSTGRES_PASSWORD, SECRET_KEY, BASE_URL and CORS_ORIGINS
docker compose -f docker-compose.prod.yml -p docgen up -d --build
```

This launches PostgreSQL (pgvector), Redis, a CPU Ollama for embeddings, the FastAPI backend with its background workers plus a one-shot frontend build. The long-running services restart automatically once Docker starts on boot.

Then install `deploy/docgen.caddy` into the host Caddy (validate, then reload) so it serves the built frontend and proxies the API, and check that `https://<host>/api/health` returns `{"status":"ok"}`.

## Environment variables

| Variable | Purpose |
|---|---|
| `POSTGRES_USER`, `POSTGRES_PASSWORD`, `POSTGRES_DB` | Database credentials |
| `SECRET_KEY` | Session signing |
| `BASE_URL`, `CORS_ORIGINS` | Public origin of the app |
| `REDIS_URL`, `OLLAMA_HOST` | Internal service addresses (set by the compose file) |
| `OPENAI_API_KEY`, `ANTHROPIC_API_KEY`, `GEMINI_API_KEY` | Optional server-side fallback keys, empty by default. Guests never use them |
| `SERVER_KEY_DAILY_LIMIT` | Daily message allowance per registered user on the server keys |
| `DOCGEN_API_PORT` | Port the API binds on 127.0.0.1 |

Leaving the provider keys empty is the safe default: every user brings their own key.

## Notes

- For code access, licensing or deployment inquiries, please contact the author directly.
