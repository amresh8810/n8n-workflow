<div align="center">
  <img src="https://n8n.io/favicon.ico" alt="n8n logo" width="80" height="80">
  <h1 align="center">Advanced n8n Workflow Automations</h1>
  <p align="center">
    <strong>A collection of intelligent, Human-in-the-Loop (HITL), and AI-driven n8n workflows.</strong>
  </p>
  <p align="center">
    <a href="https://n8n.io/"><img src="https://img.shields.io/badge/Powered_by-n8n-FF6D5A?style=for-the-badge&logo=n8n&logoColor=white" alt="Powered by n8n"></a>
    <a href="https://opensource.org/licenses/MIT"><img src="https://img.shields.io/badge/License-MIT-blue.svg?style=for-the-badge" alt="License: MIT"></a>
  </p>
</div>

<hr />

## 📖 Overview

This repository provides production-ready, highly sophisticated [n8n](https://n8n.io/) workflows designed to bridge the gap between artificial intelligence and day-to-day operations. Whether you are looking for an AI research assistant, an autonomous email handler, or a full-fledged intelligent Telegram companion, these workflows serve as plug-and-play solutions to supercharge your productivity.

## 🚀 Key Features & Workflows

### 1. 🌐 Multi-Modal Omni-Assistant (Multi-Agent Workflow)
The ultimate, super-charged Telegram assistant utilizing multiple agents, a massive suite of tools, and deep web integration.
* **Core Technologies**: Telegram (Voice & Text), LangChain Agents, OpenRouter, Google Workspace, Custom APIs.
* **How it works**: Uses multi-step planning agents and handles complex capabilities like real-time weather forecasts, real-world place searches (cafes, hospitals), and direct YouTube video searches. It also includes all base Assistant capabilities (Calendar, Gmail, Docs).
* **File**: [`multi-Assistent.json`](./multi-Assistent.json)

### 2. 🧠 AI Research & Human Validation Agent
An automated research pipeline that integrates robust AI search capabilities with human fact-checking.
* **Core Technologies**: Telegram, Tavily Web Search, OpenRouter (AI), Gmail, Google Docs.
* **How it works**: Provide a topic via Telegram $\rightarrow$ AI conducts deep web research $\rightarrow$ AI summarizes findings $\rightarrow$ Sent via Email for Human Validation $\rightarrow$ Once approved, converted to PDF & saved to Google Docs.
* **File**: [`AI Research Human Validation Agent.json`](./superbase_n8n/AI%20Research%20Human%20Validation%20Agent.json)

### 3. 🤖 Intelligent Telegram Assistant (Omni-Channel)
A personal, multi-modal assistant embedded directly into Telegram capable of handling complex daily tasks.
* **Core Technologies**: Telegram (Voice & Text), OpenAI (Whisper), LangChain Agent, OpenRouter, SerpAPI, Google Workspace (Calendar, Gmail, Contacts, Docs, Tasks).
* **How it works**: Transcribes voice messages or reads text, maintaining contextual memory to act as a seamless assistant. It can read/reply to emails, schedule/delete calendar events, search the web, and manage your contacts—all via conversational AI.
* **Files**: [`Assistent.json`](./superbase_n8n/Assistent.json) / [`my_Assistent.json`](./superbase_n8n/my_Assistent.json)

### 4. 📧 Human-in-the-Loop (HITL) Email Agent
Never worry about manually drafting repetitive emails again, while still maintaining full control over your outbox.
* **Core Technologies**: Gmail, AI Draft Generator, Telegram.
* **How it works**: Monitors incoming emails $\rightarrow$ AI drafts a contextual reply $\rightarrow$ Sends the draft to Telegram $\rightarrow$ You click *Approve* or *Reject* $\rightarrow$ The email is sent automatically if approved.
* **File**: [`HITL Email Agent - Main Workflow.json`](./superbase_n8n/HITL%20Email%20Agent%20-%20Main%20Workflow.json)

### 5. 🗄️ RAG Chat Assistant (Vector Search)
A sophisticated Retrieval-Augmented Generation (RAG) assistant that grounds AI responses in your specific documentation.
* **Core Technologies**: OpenRouter, Supabase Vector Store, Postgres Chat Memory, OpenAI Embeddings.
* **How it works**: Ingests files, splits text into embeddings, and stores them in Supabase. When a question is asked, it searches the vector database and provides an accurate, context-aware answer.
* **File**: [`My workflow 2.json`](./superbase_n8n/My%20workflow%202.json)

### 6. 🎨 Image Generation Form Automator
A streamlined workflow to generate images dynamically from user form submissions.
* **Core Technologies**: Webhooks (Forms), OpenRouter, Image Generation API.
* **How it works**: User submits a form with details $\rightarrow$ AI crafts an optimized prompt $\rightarrow$ Image is generated and downloaded/saved automatically.
* **File**: [`ural.json`](./superbase_n8n/ural.json)

<hr />

## 🛠️ Setup & Installation

Follow these steps to deploy any of the workflows in your own n8n instance:

### Prerequisites
1. An active [n8n environment](https://docs.n8n.io/hosting/) (Self-hosted or Cloud).
2. API keys for the services utilized in your chosen workflow (e.g., OpenAI, OpenRouter, Tavily, SerpAPI, Telegram Bot Token).
3. Google Cloud Console App configured with OAuth2 (for Gmail, Calendar, Docs, and Contacts integrations).

### Deployment Steps
1. **Clone this repository** (or download the `.json` files):
   ```bash
   git clone https://github.com/amresh8810/n8n-workflow.git
   ```
2. **Import into n8n**:
   - Open your n8n workspace.
   - Go to **Workflows** > **Add Workflow**.
   - Click the options menu (top right) $\rightarrow$ **Import from File**.
   - Select the desired `.json` file from the repository.
3. **Configure Node Credentials**:
   - The imported workflow will highlight nodes lacking credentials.
   - Click each node and link or create the necessary connection (e.g., Google OAuth2, Telegram API).
4. **Activate**:
   - Toggle the switch at the top right to **Active**.

## 🤝 Contributing
Contributions are highly encouraged! If you have built an exciting new n8n automation or improved an existing one:
1. Fork the project.
2. Create your feature branch (`git checkout -b feature/AmazingWorkflow`).
3. Commit your changes (`git commit -m 'Add some AmazingWorkflow'`).
4. Push to the branch (`git push origin feature/AmazingWorkflow`).
5. Open a Pull Request.

## 📄 License
Distributed under the **MIT License**. See the `LICENSE` file for more information.
