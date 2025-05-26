# 🤖 AI-Powered Earnings Chatbot for Nike – n8n Workflow

This is an advanced [n8n](https://n8n.io/) workflow for building an **AI Agent chatbot** that responds to earnings-related questions about **Nike**, using vector store search (via **Pinecone**), OpenAI chat models, Wikipedia as a fallback, and memory support for conversation continuity.

---

## 🧠 How It Works

### 🎯 Goal:
Let users ask questions like:

> *"How did Nike perform in the last quarter?"*

The bot:
1. Searches a vector store of Nike's financial data (via Pinecone)
2. Uses OpenAI (GPT-4o) to interpret and respond
3. Uses Simple Memory to track context
4. Falls back to Wikipedia if data isn't found

---

## 🗺 Workflow Architecture

<pre> ``` [Chat Trigger] ➝ [AI Agent] ↴ ├── Chat Model: OpenAI GPT-4o ├── Memory: Simple Memory ├── Tool 1: Wikipedia Lookup └── Tool 2: Vector Store QA ├── Pinecone Index ("Nike") ├── Embedding via OpenAI └── Answer via GPT-4o-mini ``` </pre>

## 🛠 Tech Stack

| Component              | Tool / Provider         |
|------------------------|--------------------------|
| Chat Agent             | n8n AI Agent (Tools Agent) |
| LLM for reasoning      | OpenAI GPT-4o            |
| Embedding model        | OpenAI Embeddings        |
| Vector storage         | Pinecone (namespace: `Nike`) |
| Memory                 | n8n Simple Memory        |
| Knowledge base backup  | Wikipedia Tool           |


## 🚀 Getting Started

### 1. 🔁 Clone or Fork the Repo


git clone https://github.com/danneba/n8n-nike-ai-agent.git
cd nike-ai-agent


### 2. Import into n8n

- Open [n8n cloud](https://app.n8n.io/)
- Click **Import Workflow**
- Upload `nike-earnings-ai-agent.json`

---

### ✅ 3. Example Prompt

Help users see how interaction works:

## 🧪 Example Conversations

**👤 User:** How did Nike perform in the last quarter?  
**🤖 Bot:** Hey there, thanks for asking! 📊 Let's check out how Nike did last quarter... 🏃💰

---

**👤 User:** What was Nike's revenue in Q2?  
**🤖 Bot:** Great question! 💵 In Q2, Nike brought in some serious cash! Let me break it down for you... 📈

---

**👤 User:** Did Nike's profit go up this year?  
**🤖 Bot:** Let's take a look! 👀 From what I found, Nike’s profits are stepping up like a new pair of kicks! 👟💹

---

**👤 User:** Where can I find more info about Nike's financials?  
**🤖 Bot:** You got it! 📚 I can pull data from Nike's earnings reports and even check Wikipedia if you’d like. Just ask away! 🧠🔍


## 🧩 Workflow Files

| File                          | Description                                              |
|-------------------------------|----------------------------------------------------------|
| `nike-earnings-ai-agent.json` | Main exported workflow from n8n                         |
| `workflow.png` (optional)     | Visual diagram of the workflow (from n8n editor)        |
| `README.md`                   | Project documentation and usage instructions            |


