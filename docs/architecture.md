# 🏗️ Architecture

DocGen.AI is a FastAPI and React application that answers questions about your code with retrieval-augmented generation (RAG) on top of hosted LLM providers.

## Components

- **Frontend**: React + shadcn/ui + Tailwind, built with Vite. Includes a provider picker, a model picker driven by the provider catalog and a key dialog that stores one API key per provider in the browser.
- **Backend**: FastAPI. Handles sign-in, chat sessions, codebase management and LLM requests. Streams replies to the browser over WebSockets.
- **LLM providers**: a small provider adapter interface with one adapter per provider, each on the official SDK with streaming:
    - OpenAI (Responses API)
    - Anthropic (Messages API)
    - Google Gemini (google-genai)
- **Provider catalog**: the model list and per-model parameter rules (which sampling settings each model accepts, plus token limits) are shared with ConfigKeep, so every request only carries settings the target model accepts.
- **Embeddings**: a small CPU embedding model (`nomic-embed-text` on Ollama) turns code chunks and messages into vectors. Embedding is best-effort: chat keeps working if it is slow or down.
- **Storage**: PostgreSQL with pgvector for users, chats, code chunks and embedding vectors.
- **Background jobs**: Redis with ARQ and Celery for cloning, chunking and embedding codebases.
- **Hosting**: Docker Compose behind Caddy (TLS, security headers and a strict Content Security Policy) on a dedicated server at docgen.4zam.dev.

## How a chat request flows

1. The browser sends the message plus the API key for the chat's provider, in one request header, over HTTPS.
2. The backend embeds the message, retrieves the most relevant code and chat chunks and builds a system prompt.
3. The provider adapter applies the model's parameter rules and streams the reply from the provider.
4. Text deltas reach the browser over a WebSocket. Errors become clear messages (bad key, rate limit, model not available) and never include the key.

The key is used for that one request and is never stored or logged on the server. All provider calls go through the backend, so the page itself only ever talks to its own origin.

## Coming next

- **Unified sign-in** through 4zam accounts (auth.4zam.dev), replacing the current guest-only sign-in.
- **ConfigKeep connector**: run a chat from an agent config (provider, model, system prompt, parameters) stored in ConfigKeep.
