# 🏗️ Architecture

DocGen.AI combines modern AI infrastructure with a local-first, real-time developer experience optimized for performance, modularity, and privacy.

## Components

- **Frontend**: React + ShadCN + Tailwind
A clean, performant UI powered by Vite, supporting dark mode, dynamic theming, and responsive layout.
- **Backend**: FastAPI
Handles authentication, chat sessions, codebase management, and serves LLM requests with secure routing.
- **LLM Runtime**: Ollama (locally-hosted models)
Used to run and stream responses from models like LLaMA 3 and Mistral in a local, containerized environment.
- **Task Queue**: ARQ
Manages background jobs such as codebase embedding, chunking, token counting, and async file processing with Redis as the queue backend.
- **Realtime Engine**: WebSockets (FastAPI)
Streams chat messages, background task updates, and live system feedback.
- **Reverse Proxy**: Caddy + Docker Compose
Handles routing across containers (frontend, backend, Ollama), SSL termination, and proxy rules for API calls.
- **Embeddings + Storage**: PostgreSQL + pgvector
Stores tokenized code chunks, embedding vectors, and model/chat metadata for RAG-based prompts and retrieval.

<!-- ## Diagram

*Insert architecture diagram here (optional)* -->
