
# 🧭 Target Onboarding Assistant Bot (n8n + Telegram + OpenAI)

This project delivers a smart, conversational onboarding experience for **new hires and HR teams at Target** using a **Telegram chatbot** powered by **n8n**, **OpenAI**, and **Pinecone vector search**. The assistant answers frequently asked onboarding questions based on a structured knowledge base.

---

## 🚀 Key Features

- 🤖 Telegram chatbot for real-time Q&A
- 📄 Uses a structured [Onboarding FAQ PDF](./Target_OnBoardingAssistance_FAQ.pdf)
- 🧠 Answers are generated only from uploaded context (no hallucinations)
- 🌐 Supports vector search with Pinecone + OpenAI embeddings
- 🛠️ Built entirely in **n8n** (low-code/no-code automation)

---

## 📲 Live Demo

> 🔗 **Try it now on Telegram**: [@SriramAIOnboardingAssist_bot](https://web.telegram.org/k/#@SriramAIOnboardingAssist_bot)

📌 **Sample Questions to Try**:
- What documents do I need for my I-9 verification?
- When will I receive my schedule?
- How do I set up or change my direct deposit?
- What is the dress code for store employees?
- Who do I contact if I have a payroll issue?

  And the quick demo with Telegram is here ---> [Target Onboarding Assist Bot - Demo](https://youtu.be/gAWO5dfMdh8)

---

## 📁 Project Files

| File                                 | Purpose                                              |
|--------------------------------------|------------------------------------------------------|
| `Onboarding Assist.json`            | n8n workflow for Telegram-triggered FAQ bot          |
| `Vector Creation Onboarding Assistant.json` | n8n workflow to vectorize the onboarding FAQ PDF    |
| `Target_OnBoardingAssistance_FAQ.pdf` | Official onboarding questions and answers (data source) |

---

## 🧱 Tech Stack

- **n8n** – Workflow automation
- **Telegram Bot API** – User interface
- **OpenAI (GPT-4.1)** – Language understanding
- **Pinecone** – Semantic vector database
- **Google Drive** – Document hosting & triggering

---

## 🧠 How It Works

### 1️⃣ Vector Creation (Content Ingestion)
- Watches Google Drive for the onboarding PDF
- Splits content into chunks
- Generates OpenAI embeddings
- Stores chunks as vectors in **Pinecone**

### 2️⃣ Telegram Assistant Workflow
- Listens for new messages on Telegram
- Matches query against vector store (contextual search)
- Uses OpenAI to summarize matching answer
- Replies in chat or responds:  
  `"Sorry! I can't find relevant information from the knowledge base."`

---

## 🔐 Prerequisites

- Telegram Bot Token  
- OpenAI API Key  
- Pinecone API Key  
- Google Drive OAuth2 credentials  
- n8n self-hosted or cloud account

---

## 🛠️ How to Set It Up

1. Clone this repo
2. Import the `.json` workflows into your n8n instance
3. Set up credentials for:
   - Telegram
   - OpenAI
   - Pinecone
   - Google Drive
4. Upload the onboarding FAQ PDF to the specified Drive folder
5. Start chatting on Telegram!

---

## 📄 License

MIT License

---

## ✨ Credits

Developed as part of an automation assignment for onboarding support using a real-world use case inspired by **Target's HR process**.
