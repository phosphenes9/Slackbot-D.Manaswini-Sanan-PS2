StageCraft Studio Knowledge Assistant
An enterprise-grade, real-time **Retrieval-Augmented Generation (RAG)** platform designed for fast-paced studio production environments. StageCraft seamlessly links an administrative web control portal with a conversational Slack workspace layer, utilizing state-of-the-art context isolation to prevent data leakage between cross-functional teams.
---
## 🎯 Project Highlights & Core Features
### 1. Multi-Content Document Upload & Ingestion
Accepts and processes technical document vectors across multiple formats—including **PDFs, Word documents (`.docx`), CAD schematics (`.dwg`), and multi-track audio sheets (`.wav`/`.mp3`)**—indexing them cleanly into targeted memory pools.
### 2. Context-Isolated Natural Language Q&A
Allows end-users to issue conversational, free-text queries inside Slack threads, returning hyper-focused responses grounded strictly in the underlying dataset using **Gemini 2.5 Flash**.
### 3. Native Document Summarization
Extracts structural layout data in real-time. Users can upload a physical file attachment directly inside a Slack message window and instantly request an analytical summary thread.
### 4. Multi-Turn Conversational Tracking
Maintains deep thread memory state across chat windows, enabling fluent, contextual follow-up questions instead of rigid, one-shot lookups.
### 5. Scoped Knowledge & Fine-Grained Access Controls
Implements a dynamic pre-filtering data matrix layer. Administrators can selectively assign assets to specific security tiers (**Global Workspace, Team: Dance Troupe, Team: Production Crew, or Private Executive**), strictly dictating what the generative AI model is permitted to see at any given second.
### 6. Live Re-indexing Telemetry
Features a real-time event-streaming telemetry feed driven by Server-Sent Events (SSE), immediately flashing system logs on the administrative hub whenever access permissions are modified.
---

## 🛠️ Tech Architecture Matrix
* **Frontend Dashboard:** React.js, styled with a high-fidelity, designer-centric aesthetic featuring real-time telemetry streaming views.
* **Backend Application Gateway:** FastAPI (Python 3.11), handling ingestion schemas and serving high-speed API state synchronization routes.
* **Async Interface Handler:** Slack Bolt Framework operating over highly stable **Socket Mode WebSockets**, patched for thread-safe background processing on Windows.
* **Core Orchestrator:** Google GenAI SDK, bound to deterministic execution weights ($Temperature = 0.1$) to enforce a strict **zero-hallucination guardrail**.
---
## 🚀 Getting Started
### 1. Environment Configurations
Clone the workspace repository and establish your local credentials block:
```bash
# Clone the repository
git clone https://github.com/your-username/stagecraft-studio-bot.git
cd stagecraft-studio-bot
# Install required runtime packages
pip install fastapi uvicorn pydantic google-genai slack-bolt python-docx requests
```
### 2. Active Script Environment Variable Pointers
Ensure your API tokens are configured inside `bot.py`:
```python
SLACK_BOT_TOKEN = "xoxb-your-bot-token"
SLACK_APP_TOKEN = "xapp-your-app-token"
GEMINI_API_KEY  = "your-gemini-api-key"
```
### 3. Launching the Multi-Threaded Engine
Execute the core backend server gateway to bind network sockets onto port `8000`:
```bash
python bot.py
```
In a separate terminal thread pane, boot up your administrative React node:
```bash
cd client
npm install
npm run dev
```
## 📊 Live Pitch Demo Walkthrough Guide
To perfectly showcase the system architecture to the evaluation jury, execute this standard verification sequence:
1. **The Lockdown:** Set `Costume_Asset_Ref_001.pdf` or `Music_Track_Asset_Ref_04.wav` to **Private Executive** on the web hub dropdown. Tag the bot in Slack asking for details. The bot will flag it immediately with a defensive `❌ Context Insufficient` shield.
2. **The Live Ingestion Pass:** Change that same asset's dropdown menu to **Global Workspace**. Watch the Live Telemetry panel scroll.
3. **The Grounded Response:** Re-run the exact same query in Slack. The bot will effortlessly extract the target specification strings and deliver a verified answer appended with a confidence metric: `📊 Semantic Confidence: 94%`.
