# DocGen.AI

Welcome to the public documentation for **DocGen.AI**, a generative AI workspace for **codebase documentation**, **unit test generation** and **context-aware Q&A** over your code.

👉 [Live Demo](https://docgen.4zam.dev/login)
<span id="app-status-indicator">Checking...</span>

The demo runs on a dedicated server at **docgen.4zam.dev** and is online around the clock. Bring your own API key from OpenAI, Anthropic or Google Gemini to chat.

---

## 📌 Overview

DocGen.AI is a developer-facing tool designed to streamline onboarding and documentation through intelligent code understanding and language models.

It supports:

- 🧠 **Multi-provider generative AI**: pick OpenAI, Anthropic or Google Gemini and any of their current models for docs, tests and Q&A
- 🔑 **Bring your own key**: one key per provider, stored only in your browser and never saved or logged by the server
- 📂 **Retrieval over your code**: repositories are chunked and embedded (pgvector) so answers draw on the relevant code
- 🧪 Unit test scaffolding for existing code
- 👤 Instant guest sessions (unified sign-in through 4zam accounts is coming soon)
- 🌐 A modern UI with dark and light modes

---

## 📷 Demo

??? message-circle-more "Live Demo Preview"
    <div style="display: flex; justify-content: center; margin: 1.5rem 0;">
        <a href="media/mp4/docgen_demo.mp4" class="glightbox" data-type="video">
            <video 
                src="media/mp4/docgen_demo.mp4" 
                autoplay 
                muted 
                playsinline 
                loop 
                style="max-width: 100%; border-radius: 12px;">
            </video>
        </a>
    </div>

---

## 📁 Docs

- [Features](features.md)
- [Architecture](architecture.md)
- [Setup Instructions](setup.md)
