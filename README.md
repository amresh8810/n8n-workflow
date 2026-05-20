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

### 1. 🌐 Multi-Modal Omni-Assistant (`multi-Assistent.json`)
The ultimate, super-charged Telegram assistant with a massive suite of tools and deep web integration.
* **Core Technologies**: Telegram (Voice & Text), LangChain Agents, OpenRouter, Google Workspace, Custom APIs.
* **Capabilities**:
  - **Weather & Places**: Fetches real-time weather forecasts and searches for real-world places (cafes, hospitals, hotels).
  - **YouTube Search**: Directly searches and returns YouTube videos/links.
  - **Google Workspace**: Reads/replies to Gmail, schedules Google Calendar events, and queries Google Docs.
  - **Advanced Processing**: Uses multi-step planning agents and handles complex file conversion/transcription via OpenAI.

### 2. 🧠 AI Research & Human Validation Agent (`AI Research Human Validation Agent.json`)
An automated research pipeline that integrates robust AI search capabilities with human fact-checking.
* **How it works**: Provide a topic via Telegram $\rightarrow$ AI conducts deep web research $\rightarrow$ AI summarizes findings $\rightarrow$ Sent via Email for Human Validation $\rightarrow$ Once approved, converted to PDF & saved to Google Docs.

### 3. 🤖 Standard Telegram Assistant (`Assistent.json` / `my_Assistent.json`)
A streamlined conversational assistant embedded directly into Telegram capable of handling daily tasks, web searches (SerpAPI), and calendar management.

### 4. 📧 Human-in-the-Loop (HITL) Email Agent (`HITL Email Agent - Main Workflow.json`)
Never worry about manually drafting repetitive emails again, while still maintaining full control over your outbox.
* **How it works**: Monitors incoming emails $\rightarrow$ AI drafts a contextual reply $\rightarrow$ Sends the draft to Telegram $\rightarrow$ You click *Approve* or *Reject* $\rightarrow$ The email is sent automatically if approved.

### 5. 🗄️ RAG Chat Assistant (`My workflow 2.json`)
A sophisticated Retrieval-Augmented Generation (RAG) assistant that grounds AI responses in your specific documentation using **Supabase Vector Store**, **Postgres Chat Memory**, and **OpenAI Embeddings**.

### 6. 🎨 Image Generation Form Automator (`ural.json`)
A streamlined workflow that receives form submissions via Webhook, crafts an optimized AI prompt using OpenRouter, and automatically generates/downloads the image.

<hr />

## 🛠️ Setup & Installation

Follow these steps to deploy any of the workflows in your own n8n instance:

### Prerequisites
1. An active [n8n environment](https://docs.n8n.io/hosting/) (Self-hosted or Cloud).
2. API keys for the services utilized in your chosen workflow (e.g., OpenAI, OpenRouter, Tavily, SerpAPI, Telegram).
3. Google Cloud Console App configured with OAuth2 (for Gmail, Calendar, Docs, and Contacts integrations).

### Deployment Steps
1. **Clone this repository** (or download the `.json` files):
   ```bash
   git clone https://github.com/amresh8810/n8n-workflow.git
