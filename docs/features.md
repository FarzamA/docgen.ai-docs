# 🔍 Features

---

## 🔐 Authentication

DocGen.AI provides a secure and seamless authentication system with support for:

??? o-auth "OAuth login via Google, Facebook, or Github"
    <div style="display: flex; justify-content: center; margin: 1.5rem 0;">
        <video 
            src="./../media/mp4/login_modal_btc.mp4" 
            autoplay 
            muted 
            playsinline 
            loop 
            style="max-width: 400px; border-radius: 12px;">
        </video>
    </div>

??? e-mail-registration "Email-based registration with background loading screen"  
    <div style="display: flex; justify-content: center; margin: 1.5rem 0;">
        <video 
            src="./../media/mp4/email_signup_btc.mp4" 
            autoplay 
            muted 
            playsinline 
            loop 
            style="max-width: 100%; border-radius: 12px;">
        </video>
    </div>

??? e-mail-verification "Email verification for user to be activated "  
    <div style="display: flex; justify-content: center; margin: 1.5rem 0;">
        <video 
            src="./../media/mp4/email_verification_btc.mp4" 
            autoplay 
            muted 
            playsinline 
            loop 
            style="max-width: 100%; border-radius: 12px;">
        </video>
    </div>

??? user-login "Username based login"  
    <div style="display: flex; justify-content: center; margin: 1.5rem 0;">
        <video 
            src="./../media/mp4/username_login_btc.mp4" 
            autoplay 
            muted 
            playsinline 
            loop 
            style="max-width: 100%; border-radius: 12px;">
        </video>
    </div>

??? qr-code "Two-Factor Authentication (2FA) for enhanced security (optional)"  
    <div style="display: flex; justify-content: center; margin: 1.5rem 0;">
        <video 
            src="./../media/mp4/2fa_setup_btc.mp4" 
            autoplay 
            muted 
            playsinline 
            loop 
            style="max-width: 100%; border-radius: 12px;">
        </video>
    </div>

??? e-mail-verification "Email-based password reset"  
    <div style="display: flex; justify-content: center; margin: 1.5rem 0;">
        <video 
            src="./../media/mp4/forgot_pass_btc.mp4" 
            autoplay 
            muted 
            playsinline 
            loop 
            style="max-width: 100%; border-radius: 12px;">
        </video>
    </div>

---

## 🧠 How It Works

- DocGen.AI connects to your codebase or documentation context.
- Users can chat with an LLM to generate unit tests, inline documentation, or ask questions about code behavior.
- You can either connect a GitHub repo, upload a file, or chat with a blank model.
- The system streams results in real time and provides copyable output.
- If no codebase is loaded, DocGen.AI defaults to chat-only mode for exploration and experimentation.

??? rocket "Interactive AI Workspace Demo"
    <div style="display: flex; justify-content: center; margin: 1.5rem 0;"> <video src="./../media/mp4/codegen_demo.mp4" autoplay muted playsinline loop style="max-width: 100%; border-radius: 12px;"> </video> </div>

---

## 👤 Guest User Functionality

DocGen.AI offers guest sessions for quick testing or onboarding:

- Guests can explore model features without signing up
- All guest data (code snippets, chats, preferences) is temporary
- Guests cannot modify their profiles and have a limited time before their session expires (1 hour)
- Session data is automatically wiped after logout or timeout

---

## 🖥️ Main Interface

After logging in, users land in a responsive workspace designed for productivity and model experimentation.

??? sun-moon "Sleek dark and light mode themes for visual flexibility"
    <div style="display: flex; justify-content: center; margin: 1.5rem 0;">
        <video 
            src="./../media/mp4/dark_mode_demo_btc.mp4" 
            autoplay 
            muted 
            playsinline 
            loop 
            style="max-width: 100%; border-radius: 12px;">
        </video>
    </div>

??? chart-line "Chat-based model interface for documentation, tests, and Q&A"
    <div style="display: flex; justify-content: center; margin: 1.5rem 0;">
        <video 
            src="./../media/mp4/chart_demo.mp4" 
            autoplay 
            muted 
            playsinline 
            loop 
            style="max-width: 100%; border-radius: 12px;">
        </video>
    </div>

??? message-circle-more "Support for chatting with or without a loaded codebase"
    <div style="display: flex; justify-content: center; margin: 1.5rem 0;">
        <video 
            src="./../media/mp4/live_chat_demo.mp4" 
            autoplay 
            muted 
            playsinline 
            loop 
            style="max-width: 400px; border-radius: 12px;">
        </video>
    </div>

---

## ✍️ AI-Generated Code + Docs

The code generation panel allows you to request:

- Unit tests for specific functions or classes
- Inline comments for undocumented logic
- Refactored or simplified code
- JSDoc or docstring templates

??? banknote "Code + Test Generation Demo"
    <div style="display: flex; justify-content: center; margin: 1.5rem 0;">
        <video 
            src="./../media/mp4/betting_interface_demo.mp4" 
            autoplay 
            muted 
            playsinline 
            loop 
            style="max-width: 100%; border-radius: 12px;">
        </video>
    </div>

---

## 📂 Codebase + Chunking Interface

Users can connect external repositories or upload local projects for embedding. DocGen.AI then:

- Parses files and chunks content intelligently (e.g. by function)
- Embeds code for retrieval-augmented generation (RAG)  
- Displays loading state and import logs
- Supports reprocessing individual files for updates

??? receipt "Embedding + Chunking Demo"
    <div style="display: flex; justify-content: center; margin: 1.5rem 0;">
        <video 
            src="./../media/mp4/all_bets_demo.mp4" 
            autoplay 
            muted 
            playsinline 
            loop 
            style="max-width: 100%; border-radius: 12px;">
        </video>
    </div>

---

## 🔐 Privacy + Local-First Deployment

DocGen.AI is designed for privacy-first use cases:

- All processing can be done locally or in a containerized environment
- Supports Ollama and other LLM backends for offline LLM inference  
- Codebases never leave your machine in local mode 
- Ideal for internal company projects and enterprise security needs
Together, these features ensure that trust is not assumed—it’s *provable*.

??? lock "Local Deployment with Ollama + GPU Support"
    <div style="display: flex; justify-content: center; margin: 1.5rem 0;">
        <video 
            src="./../media/mp4/provable_fairness.mp4" 
            autoplay 
            muted 
            playsinline 
            loop 
            style="max-width: 100%; border-radius: 12px;">
        </video>
    </div>

---

## 🧠 Models

DocGen.AI supports multiple generative models via a modular architecture. Models can be used for chat, test generation, documentation, and search — with flexible backend integration via Ollama, OpenAI, or other compatible APIs.

Key features include:

- Users can view a searchable list of all available and installed models
- Usage statistics and last-seen data help track model engagement
- Tags indicate whether a model is installed locally or just available to pull
- Status indicators show loading, pulling, or ready state in real time

---

## 🔒 Admin-Only Installation

To maintain a secure and controlled environment:

- Only admin users can pull or install models to the local environment
- A model pull dialog allows admins to select specific versions or tags
- Users without admin privileges will see a disabled or hidden pull button
- Install requests are tracked and reflected in the UI for transparency

This ensures that the system maintains model consistency and avoids unintentional overload of the host machine.

??? bot "Model Overview + Pulling Interface"
    <div style="display: flex; justify-content: center; margin: 1.5rem 0;"> <video src="./../media/mp4/model_dashboard_demo.mp4" autoplay muted playsinline loop style="max-width: 100%; border-radius: 12px;"> </video> </div>