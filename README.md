# 🤖 n8n AI Assistant Chatbot

A general-purpose AI chatbot built with **n8n** and **Groq API (LLaMA 3)**. Fully customizable for any topic — customer support, HR, healthcare, education, and more.

---

## ✨ Features

- 💬 Real-time AI chat powered by LLaMA 3 (via Groq)
- 🧠 Conversation memory — remembers context within a session
- ⚡ Extremely fast responses (Groq is one of the fastest LLM APIs)
- 🔧 Easily customizable system prompt for any use case
- 🖱️ No-code setup — import and run in minutes

---

## 🛠️ Tech Stack

| Tool | Purpose |
|------|---------|
| [n8n](https://n8n.io) | Workflow automation platform |
| [Groq API](https://console.groq.com) | LLM inference (LLaMA 3) |
| LLaMA 3 (8B) | AI language model |
| Window Buffer Memory | Conversation context management |

---

## 🚀 Getting Started

### Prerequisites
- [Node.js](https://nodejs.org) v18 or higher
- n8n installed globally
- Free [Groq API key](https://console.groq.com)

### Installation

**1. Install n8n**
```bash
npm install -g n8n
```

**2. Start n8n**
```bash
n8n start
```

**3. Open n8n in your browser**
```
http://localhost:5678
```

**4. Import the workflow**
- Go to Workflows → Add Workflow
- Click ⋯ → Import from File
- Select `ai-assistant-workflow.json`

**5. Add your Groq API key**
- Click the **Groq Chat Model** node
- Create a new credential and paste your Groq API key
- Save and activate the workflow

**6. Test it**
- Click the **Chat** button at the bottom of the workflow
- Start chatting! 🎉

---

## 🎨 Customization

To customize the bot for a specific topic, click the **AI Agent** node and update the system prompt. For example:

**Customer Support Bot:**
```
You are a customer support agent for [Company Name]. 
Help users with order tracking, returns, and product questions.
```

**HR Policy Bot:**
```
You are an HR assistant. Answer employee questions about 
company policies, leave, and benefits.
```

**Medical FAQ Bot:**
```
You are a medical information assistant. Provide general 
health information and advise users to consult a doctor for 
serious concerns.
```

---

## 📁 Project Structure

```
n8n-ai-assistant/
├── ai-assistant-workflow.json   # n8n workflow (import this)
└── README.md                    # Project documentation
```

---

## 🔮 Future Improvements

- [ ] Add web search tool for real-time information
- [ ] Connect to a document/PDF knowledge base (RAG)
- [ ] Deploy on a cloud server for 24/7 availability
- [ ] Add WhatsApp or Telegram integration

---

## 👤 Author

**Mirza Obaid**  
AI Automation Enthusiast | Pakistan  
[LinkedIn](https://www.linkedin.com/in/mirzaobaid) • [GitHub](https://github.com)

---

## 📄 License

MIT License — free to use and modify.
