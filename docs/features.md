# 🔍 Features

---

## 🔐 Authentication

!!! note "Sign-in update"
    The live demo currently offers **guest sessions only** while accounts move to unified sign-in through **4zam accounts** (coming soon). The flows below show the existing account system.

DocGen.AI provides a secure and seamless authentication system with support for:

??? o-auth "OAuth login via Google, Facebook or GitHub"
    <div style="display: flex; justify-content: center; margin: 1.5rem 0;">
        <a href="./../media/mp4/login_screen_docgen.mp4" class="glightbox" data-type="video">
            <video 
                src="./../media/mp4/login_screen_docgen.mp4" 
                autoplay 
                muted 
                playsinline 
                loop 
                style="max-width: 100%; border-radius: 12px;">
            </video>
        </a>
    </div>

??? e-mail-registration "Email-based registration"  
    <div style="display: flex; justify-content: center; margin: 1.5rem 0;">
        <a href="./../media/mp4/docgen_registration.mp4" class="glightbox" data-type="video">
            <video 
                src="./../media/mp4/docgen_registration.mp4" 
                autoplay 
                muted 
                playsinline 
                loop 
                style="max-width: 100%; border-radius: 12px;">
            </video>
        </a>
    </div>

??? e-mail-verification "Email verification for user to be activated "  
    <div style="display: flex; justify-content: center; margin: 1.5rem 0;">
        <a href="./../media/mp4/docgen_email_verification.mp4" class="glightbox" data-type="video">
            <video 
                src="./../media/mp4/docgen_email_verification.mp4" 
                autoplay 
                muted 
                playsinline 
                loop 
                style="max-width: 100%; border-radius: 12px;">
            </video>
        </a>
    </div>

??? qr-code "Two-Factor Authentication (2FA) for enhanced security (optional)"  
    <div style="display: flex; justify-content: center; margin: 1.5rem 0;">
        <a href="./../media/mp4/docgen_2fa.mp4" class="glightbox" data-type="video">
            <video 
                src="./../media/mp4/docgen_2fa.mp4" 
                autoplay 
                muted 
                playsinline 
                loop 
                style="max-width: 100%; border-radius: 12px;">
            </video>
        </a>
    </div>

??? e-mail-verification "Email-based password reset"  
    <div style="display: flex; justify-content: center; margin: 1.5rem 0;">
        <a href="./../media/mp4/docgen_email_pwd_reset.mp4" class="glightbox" data-type="video">
            <video 
                src="./../media/mp4/docgen_email_pwd_reset.mp4" 
                autoplay 
                muted 
                playsinline 
                loop 
                style="max-width: 100%; border-radius: 12px;">
            </video>
        </a>
    </div>

---

## 🧠 How It Works

- DocGen.AI connects to your codebase or documentation context.
- Users can chat with an LLM to generate unit tests, inline documentation or ask questions about code behavior.
- You can either connect a GitHub repo or chat with a blank model.
- The system streams results in real time and provides copyable output.
- If no codebase is loaded, DocGen.AI defaults to chat-only mode for exploration and experimentation.

??? message-circle-more "Interactive AI Workspace Demo"
    <div style="display: flex; justify-content: center; margin: 1.5rem 0;">
        <a href="./../media/mp4/docgen_demo.mp4" class="glightbox" data-type="video">
            <video 
                src="./../media/mp4/docgen_demo.mp4"
                autoplay
                muted
                playsinline
                loop s
                tyle="max-width: 100%; border-radius: 12px;">
            </video>
        </a>
    </div>

---

## 👤 Guest User Functionality

DocGen.AI offers guest sessions for quick testing or onboarding:

- Guests can explore model features without signing up
- All guest data (code snippets, chats, preferences) is temporary
- Guests cannot modify their profiles and have a limited time before their session expires (1 hour)
- Session data is automatically wiped after logout or timeout

---

## 🖥️ Main Interface

Once logged in, users are welcomed into a responsive, modern workspace built for seamless interaction and model experimentation.

- Toggle between sleek dark and light themes for a personalized experience
- Intuitive dashboards to browse installed models and codebases
- Real-time charts and usage metrics for insight into model/codebase activity
- Full chat management: rename, edit and delete conversations effortlessly

??? wrench "Demo"
    <div style="display: flex; justify-content: center; margin: 1.5rem 0;">
        <a href="./../media/mp4/full_interface_demo.mp4" class="glightbox" data-type="video">
            <video 
                src="./../media/mp4/full_interface_demo.mp4" 
                autoplay 
                muted 
                playsinline 
                loop 
                style="max-width: 100%; border-radius: 12px;">
            </video>
        </a>
    </div>

---

## ✍️ AI-Generated Code + Docs

The code generation panel allows you to request:

- Unit tests for specific functions or classes
- Inline comments for undocumented logic
- Refactored or simplified code
- JSDoc or docstring templates

---

## 📂 Codebase + Chunking Interface

Users can connect external repositories or upload local projects for embedding. DocGen.AI then:

- Parses files and chunks content intelligently (e.g. by function)
- Embeds code for retrieval-augmented generation (RAG)  
- Displays loading state and import logs
- Supports reprocessing individual files for updates

<!-- ??? receipt "Embedding + Chunking Demo"
    <div style="display: flex; justify-content: center; margin: 1.5rem 0;">
        <video 
            src="./../media/mp4/all_bets_demo.mp4" 
            autoplay 
            muted 
            playsinline 
            loop 
            style="max-width: 100%; border-radius: 12px;">
        </video>
    </div> -->

---

## 🔑 Bring Your Own Key

DocGen.AI works with your own provider account, so you stay in control of cost and data:

- Choose **OpenAI**, **Anthropic** or **Google Gemini**, then any of their current models
- Store one API key per provider, only in your browser
- Keys are sent over HTTPS with your chat requests for that provider and are never saved or logged on the server
- Clear errors tell you exactly what went wrong: a rejected key, a rate limit or quota, a model your key cannot use
- With no key, the app still works and shows a friendly prompt to add one

---

## 🧠 Models

DocGen.AI supports multiple generative models through a provider adapter layer. The model list and each model's parameter rules come from a shared provider catalog, so requests only carry settings the model accepts (for example, newer reasoning models reject `temperature`).

- **OpenAI**: GPT-6 Astra, GPT-6.1 Sol, GPT-6 Luna, GPT-5.6 Sol, GPT-4.1 (and mini), GPT-4o (and mini)
- **Anthropic**: Claude Opus 5.5, Claude Sonnet 5.5, Claude Fable 5.1, Claude Haiku 4.5
- **Google Gemini**: Gemini 3.8 Flash, Gemini 3.7 Flash, Gemini 3.1 Pro (preview)

Local Ollama models remain available on servers that install them.

---

## 🔒 Admin-Only Installation

To maintain a secure and controlled environment:

- Only admin users can pull or install models to the local environment
- A model pull dialog allows admins to select specific versions or tags
- Users without admin privileges will see a disabled or hidden pull button
- Install requests are tracked and reflected in the UI for transparency

This ensures that the system maintains model consistency and avoids unintentional overload of the host machine.

<!-- ??? bot "Model Overview + Pulling Interface"
    <div style="display: flex; justify-content: center; margin: 1.5rem 0;"> <video src="./../media/mp4/model_dashboard_demo.mp4" autoplay muted playsinline loop style="max-width: 100%; border-radius: 12px;"> </video> </div> -->