# 🤖 n8n AI Assistant Chatbot

![n8n](https://img.shields.io/badge/n8n-workflow-orange?style=flat-square)
![Groq](https://img.shields.io/badge/Groq-Compound_Beta-blue?style=flat-square)
![License](https://img.shields.io/badge/license-MIT-green?style=flat-square)
![Status](https://img.shields.io/badge/status-active-brightgreen?style=flat-square)

A **general-purpose AI chatbot** built with **n8n** and the **Groq API (Compound Beta)**. Fully customizable for any use case — customer support, HR policies, healthcare FAQs, education, and more. No coding required to set up and deploy.

---

## ✨ Features

- 💬 **Real-time AI chat** powered by Groq Compound Beta
- 🧠 **Conversation memory** — remembers context within a session using Window Buffer Memory
- ⚡ **Extremely fast responses** — Groq is one of the fastest LLM inference APIs available
- 🔧 **Easily customizable** — change the system prompt to fit any topic or domain
- 🖱️ **No-code setup** — import the workflow JSON and run in minutes
- 🔌 **Webhook-ready** — connect to WhatsApp, Telegram, Slack, or any other platform

---

## 🛠️ Tech Stack

| Tool | Purpose |
|------|---------|
| [n8n](https://n8n.io) | Workflow automation platform |
| [Groq API](https://console.groq.com) | Ultra-fast LLM inference |
| Groq Compound Beta | AI language model |
| Window Buffer Memory | Conversation context management |

---

## 💡 Use Cases

This bot is designed to be a starting template — swap the system prompt and you have a completely different assistant:

| Use Case | Description |
|----------|-------------|
| 🏢 **HR Policy Bot** | Answer employee questions about leave, benefits, and company policies |
| 🛒 **Customer Support** | Handle orders, returns, FAQs, and product inquiries |
| 🏥 **Medical FAQ Bot** | Provide general health information and direct users to professionals |
| 📚 **Education Assistant** | Help students with subject questions and study guidance |
| 🔧 **IT Helpdesk Bot** | Troubleshoot common technical issues for employees |

---

## 🚀 Getting Started

### Prerequisites

- [Node.js](https://nodejs.org) v18 or higher
- n8n installed (self-hosted or cloud)
- A free [Groq API key](https://console.groq.com)

---

### Installation

**Step 1 — Install n8n**

```bash
npm install -g n8n
```

**Step 2 — Start n8n**

```bash
n8n start
```

**Step 3 — Open n8n in your browser**

```
http://localhost:5678
```

**Step 4 — Import the workflow**

1. Go to **Workflows → Add Workflow**
2. Click the **⋯ menu → Import from File**
3. Select `AI Assistant Chatbot.json` from this repository

**Step 5 — Add your Groq API key**

1. Click the **Groq Chat Model** node
2. Click **Create new credential**
3. Paste your Groq API key from [console.groq.com](https://console.groq.com)
4. Save the credential

**Step 6 — Activate and test**

1. Toggle the workflow to **Active**
2. Click the **Chat** button at the bottom of the canvas
3. Start chatting! 🎉

---

## 🎨 Customization

To customize the bot for a specific topic, click the **AI Agent** node and update the **System Prompt** field.

### Example System Prompts

**HR Policy Bot:**
```
You are an HR assistant for [Company Name]. Answer employee questions about 
company policies, leave entitlements, benefits, and workplace guidelines. 
Be professional, concise, and always refer employees to HR for sensitive matters.
```

**Customer Support Bot:**
```
You are a customer support agent for [Company Name]. Help users with 
order tracking, product questions, returns, and refunds. 
Be friendly and resolve issues efficiently.
```

**Medical FAQ Bot:**
```
You are a medical information assistant. Provide general health information 
based on common medical knowledge. Always advise users to consult a 
qualified doctor for diagnosis or treatment.
```

**IT Helpdesk Bot:**
```
You are an IT support assistant. Help employees troubleshoot common issues 
with software, hardware, email, and network connectivity. 
Escalate complex issues to the IT team.
```

---

## ⚙️ How It Works

```
User Message
     │
     ▼
n8n Webhook (receives the message)
     │
     ▼
AI Agent Node (processes with system prompt)
     │
     ├──► Window Buffer Memory (stores conversation history)
     │
     └──► Groq API / Compound Beta (generates response)
                    │
                    ▼
            Response sent back to user
```

1. A message is sent to the n8n webhook endpoint
2. The **AI Agent** node processes it using the configured system prompt
3. **Window Buffer Memory** provides conversation history for context
4. **Groq Compound Beta** generates a fast, intelligent response
5. The response is returned to the user

---

## 🐞 Troubleshooting

| Problem | Solution |
|---------|----------|
| n8n won't start | Make sure Node.js v18+ is installed: `node --version` |
| Groq API key error | Double-check your key at [console.groq.com](https://console.groq.com) — make sure it's active |
| Workflow not activating | Check that all nodes are properly connected and credentials are saved |
| Chat button not appearing | Make sure the workflow is saved and the Chat Trigger node is present |
| Slow responses | Groq is very fast — if slow, check your internet connection |

---

## 📁 Project Structure

```
n8n-ai-assistant/
├── AI Assistant Chatbot.json   # n8n workflow — import this file
└── README.md                   # Project documentation
```

---

## 🔮 Roadmap / Future Improvements

- [ ] Add web search tool for real-time information retrieval
- [ ] Connect to a document/PDF knowledge base (RAG pipeline)
- [ ] WhatsApp integration via WAHA
- [ ] Telegram bot integration
- [ ] Deploy on a cloud server for 24/7 availability
- [ ] Add multi-language support

---

## 👤 Author

**Mirza Obaid**
AI Automation Enthusiast | Pakistan
[LinkedIn](https://www.linkedin.com/in/mirzaobaid) • [GitHub](https://github.com/mirza9037)

---

## 📄 License

This project is licensed under the **MIT License** — free to use, modify, and distribute.

---

> ⭐ If you found this useful, consider starring the repo — it helps others discover it!
