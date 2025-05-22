# ⚙️ Setup Instructions

> NOTE: This documentation is for demonstration purposes only. The source code for DocGen.AI is currently private.

## Requirements

- Docker + Docker Compose
- Ollama installed locally or running via container
- Redis (used by ARQ for background tasks)
- Python 3.11+ (for FastAPI and local dev mode)

## Local Deployment (Recommended)

To spin up the full stack locally with GPU-enabled LLMs and real-time embedding:

```bash
git clone https://github.com/FarzamA/DocGen.AI
cd docgen.ai
docker compose up --build
```

This will launch:

- The React frontend (Vite + ShadCN)
- FastAPI backend
- Ollama model server
- Redis (for background jobs with ARQ)
- Caddy reverse proxy (serves all apps under one domain)

## Notes

- GPU support for Ollama is enabled by default; ensure your NVIDIA drivers and CUDA are installed.
- `.env` file is required in the root directory for configs and Redis connection.
- For code access, licensing, or enterprise deployment inquiries, please contact the author directly.
