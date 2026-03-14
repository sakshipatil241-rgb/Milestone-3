# 💬 Conversational RAG Chatbot  
### Retrieval-Augmented Generation with Contextual Memory

![Python](https://img.shields.io/badge/Python-3.10+-blue.svg)
![LangChain](https://img.shields.io/badge/LangChain-Framework-green)
![ChromaDB](https://img.shields.io/badge/VectorDB-Chroma-orange)
![LLM](https://img.shields.io/badge/LLM-LLaMA%203.1-purple)
![License](https://img.shields.io/badge/License-Academic-lightgrey)

---

## 📌 Project Overview

The **Conversational RAG Chatbot** is an end-to-end AI system that allows users to interact with their documents using natural language.

This project implements:

- 📄 Document ingestion (PDF, TXT)
- ✂️ Intelligent text chunking
- 🔎 Semantic search using vector embeddings
- 🤖 Retrieval-Augmented Generation (RAG)
- 💬 Multi-turn conversational memory
- 📚 Source citation support

---

## 🏗️ System Architecture

User Query
↓
Chat Interface
↓
Retriever (Vector DB)
↓
Relevant Document Chunks
↓
LLM (LLaMA 3.1 via Groq)
↓
Context-Aware Answer
---

# 📦 Project Modules

---

## 🔹 Module 1: Document Ingestion & Indexing

### ✅ Features

- PDF & TXT loading
- Directory-based auto detection
- Recursive chunking strategy
- Metadata cleaning
- Local embedding generation
- Persistent vector storage

### ⚙️ Technical Details

- Chunk Size: 3000
- Chunk Overlap: 200
- Embedding Model: `sentence-transformers/all-MiniLM-L6-v2`
- Vector Store: Chroma (Persistent in `./chroma_db`)
- Startup cleanup to prevent context leakage

---

## 🔹 Module 2: Retrieval & RAG Pipeline

### ✅ Features

- Top-K retrieval (k=3)
- Context-grounded response generation
- Hallucination control
- Low temperature inference

### 🤖 LLM Configuration
model = ChatGroq(
model="llama-3.1-8b-instant",
temperature=0
)
### 🧠 Hallucination Prevention

- Strict prompt design
- Context-only answering
- Low temperature setting
- Limited retrieval window

AI Based Document Search and Knowledge Retrieval with Conversational Interface
Milestone 3 – Conversational Interface
📌 Project Overview

This milestone focuses on developing a conversational chatbot interface that allows users to interact with a knowledge base using natural language queries.

The system acts like an AI copilot where users can ask questions, receive context-aware responses, and continue the conversation with follow-up questions.

The chatbot interface is implemented using the Reflex Python framework, which enables building full-stack web applications using only Python.

🎯 Objectives

The main objectives of this milestone are:

Create a chatbot-style front-end interface.

Allow users to submit natural language queries.

Maintain conversation history.

Handle follow-up questions using previous context.

Provide a smooth and interactive user experience.

⚙️ Technologies Used
Technology	Purpose
Python	Backend logic
Reflex	Full-stack web framework
LangChain	LLM orchestration
FAISS	Vector similarity search
OpenAI API	Language model responses
HTML / CSS	Frontend styling
🏗 System Architecture

User → Chat Interface → Query Processing → Context Retrieval → LLM Response → Chat Display

User asks a question in the chatbot.

The system retrieves relevant document chunks from the vector database.

The language model generates a response using retrieved information.

The response is shown in the chat interface.

Conversation history is maintained for follow-up questions.

📁 Project Structure
full_stack_using_reflex
│
├── components
│   ├── __init__.py
│   ├── rag_navbar.py
│   └── code_review.py
│
├── full_stack_using_reflex.py
├── rxconfig.py
├── requirements.txt
├── .gitignore
└── README.md
💬 Conversational Features
Chat Interface

Users can type questions in a chat input box.

Messages appear in a chat format.

Conversation Memory

The system remembers previous questions and answers.

Enables context-aware responses.

Follow-up Question Handling

Example:

User:

What is machine learning?

User (follow-up):

What are its types?

The chatbot understands the follow-up using conversation context.

🚀 Installation and Setup
1️⃣ Clone the repository
git clone <repository-url>
cd full_stack_using_reflex
2️⃣ Create virtual environment
python -m venv venv

Activate environment

Windows

venv\Scripts\activate

Linux / Mac

source venv/bin/activate
3️⃣ Install dependencies
pip install -r requirements.txt
4️⃣ Run the application
python -m reflex run
5️⃣ Open the application

Open in browser

http://localhost:3000
📊 Expected Output

Interactive chatbot interface

Real-time conversation flow

Chat history displayed

Ability to ask multiple questions
