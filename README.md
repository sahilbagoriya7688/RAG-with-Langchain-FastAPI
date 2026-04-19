# RAG with LangChain & FastAPI

A production-ready **Retrieval-Augmented Generation (RAG)** system that enables intelligent Q&A over documents using LangChain, FAISS vector store, and FastAPI.

> Built at IIT Delhi | Processes 1,000+ documents | LLM responses in <2 seconds

---

## 🎯 Project Overview

The RAG pipeline integrates external document knowledge into the LLM response process. Instead of relying only on pretrained knowledge, the system retrieves relevant information from a document store and uses it to generate accurate, context-aware answers.

---

## 🛠️ Tech Stack

- **Python** — core language
- **LangChain** — orchestration and chain management
- **FAISS** — vector store for fast similarity search
- **FastAPI** — REST API deployment
- **OpenAI / Llama** — language model for response generation

---

## 🚀 System Architecture

```
Documents → Text Splitting → Embeddings → FAISS Vector Store
                                                  ↓
User Query → Query Embedding → Similarity Search → Retrieved Chunks
                                                  ↓
                                    LLM + Context → Final Response
```

---

## ✨ Features

- **Multi-format document loading** — text files, PDFs
- **Intelligent text splitting** — handles large documents efficiently
- **Semantic embedding generation** — for deep contextual understanding
- **FAISS vector storage** — fast similarity search at scale
- **Scalable REST API** — deployed with FastAPI
- **<2 second response time** — optimized pipeline

---

## 📁 Project Structure

```
RAG-with-Langchain-FastAPI/
├── main.py              # FastAPI app entrypoint
├── rag.py               # Core RAG pipeline logic
├── endpoints.py         # API endpoint definitions
├── requirements.txt     # Dependencies
└── README.md
```

---

## ▶️ How to Run

```bash
# Install dependencies
pip install -r requirements.txt

# Start the FastAPI server
uvicorn main:app --reload

# API will be available at http://localhost:8000
```

---

## 📡 API Usage

```bash
# Upload a document
POST /upload
Content-Type: multipart/form-data

# Ask a question
POST /query
{ "question": "What is the main topic of the document?" }
```
