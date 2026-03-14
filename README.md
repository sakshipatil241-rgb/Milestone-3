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

---"# Milestone-3-" 
"# Milestone-3" 
