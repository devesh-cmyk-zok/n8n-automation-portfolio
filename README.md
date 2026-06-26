# n8n Automation Workflows Portfolio:

A curated collection of production-ready automation workflows configured for local deployment. These workflows focus on data ingestion, API integration, and structuring backend pipeline automations.

# Tech Stack \& Features:

1. Core Engine: n8n (Localhost Instance)
2. Pipeline Structure: Dynamic webhooks, conditional routing logic, and raw data payload formatting.
3. Architecture: Designed as modular JSON blueprints ready for instant import and environmental scaling.

# How to Run Locally:

1. Ensure you have n8n running locally via npm or Docker.
2. Create a new workflow in your n8n dashboard.
3. Import the corresponding `.json` file from this repository using the UI menu (`Import from File`).

# Core Workflows Breakdown:

1. Production Webhook Triage Agent
* File Name: `api-mediquery-rag-agent.json`
* Core Tech: Webhook, LangChain Agent, Pinecone Vector Store, Gemini API, Sub-Workflow Tool
* Professional Description: Exposes a secure POST webhook endpoint (`Medi-query`) that routes incoming user payloads through a Gemini powered LangChain Agent with window memory. It leverages Pinecone vector stores to serve contextual data while dynamically invoking secondary automation tools based on user intent.

---

2. Automated Document Ingestion Pipeline
* File Name: `gdocs-to-pinecone-embedding-pipeline.json`
* Core Tech: Google Docs Trigger, Default Data Loader, Gemini Embeddings, Pinecone Vector Store
* Professional Description: An ETL (Extract, Transform, Load) utility designed to automatically fetch raw text files from Google Docs, chunk and vectorize the textual contents using Google Gemini Embeddings models, and upsert them systematically into an active Pinecone index for immediate retrieval.

---

3. Interactive Retrieval-Augmented Generation (RAG) Bot
* File Name: `chat-interface-rag-agent.json`
* Core Tech: Chat Trigger, LangChain Agent, Buffer Window Memory, Pinecone Index Node, Gemini Model
* Professional Description: Connects directly to localized user chat UI triggers. Implements system-level prompt boundaries to ensure strict context compliance while extracting internal insights from vectorized indexes using Gemini.

---

4. Sub-Workflow Automated Notification Tool
* File Name: `sub-workflow-gmail-agent-tool.json`
* Core Tech: Execute Workflow Trigger, LangChain Agent, Gmail Tool Node, Gemini API
* Professional Description: Engineered explicitly as a callable sub-workflow module. It runs asynchronously when triggered by a master agent, parsing dynamic parameters through an internal LLM layer to draft and send structured corporate Gmail messages automatically.

---

5. Polling-Based Messaging Assistant
* File Name: `telegram-polling-ai-assistant.json`
* Core Tech: Schedule Trigger, HTTP Request (Telegram API), LangChain Agent, Telegram Output Node
* Professional Description: Executes high-frequency API polling via native HTTP request blocks to intercept incoming Telegram channel metrics. Feeds the payloads into an agent layer constrained to brief output limits before programmatically returning contextual responses.

---



