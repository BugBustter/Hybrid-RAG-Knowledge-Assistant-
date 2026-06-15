# 🧠Hybrid RAG Knowledge Assistant

### Secure Multi-Tenant Retrieval-Augmented Generation Platform for Intelligent Document Question Answering

![Python](https://img.shields.io/badge/Python-FastAPI-blue)
![Spring Boot](https://img.shields.io/badge/Spring%20Boot-3.x-brightgreen)
![LangChain](https://img.shields.io/badge/LangChain-RAG-orange)
![FAISS](https://img.shields.io/badge/FAISS-Vector%20Database-purple)
![MySQL](https://img.shields.io/badge/MySQL-Database-blue)
![Spring AI](https://img.shields.io/badge/Spring%20AI-Chatbot-success)
![License](https://img.shields.io/badge/License-MIT-lightgrey)

---

# 🌐 Live Demo

**🔗 Deployment:** https://your-deployment-link.com

**🎥 Demo Video:** https://your-demo-video-link.com

---

# 📌 Project Overview

**DocuMind AI** is a secure, enterprise-grade Hybrid Retrieval-Augmented Generation (RAG) platform that enables users to upload documents, perform semantic search, and receive context-aware answers powered by Large Language Models (LLMs).

The platform combines:

* Vector Search (FAISS)
* Keyword Search (BM25)
* Cross-Encoder Reranking
* Multi-LLM Support
* Spring AI Chatbot
* RAG Evaluation Framework

to deliver accurate, grounded, and hallucination-resistant responses.

Built using a microservice architecture, DocuMind AI ensures scalability, user isolation, and flexible deployment across local and cloud environments.

---

# 🎯 Problem Statement

Traditional AI chatbots often suffer from:

* Hallucinated responses
* Lack of source grounding
* Poor retrieval quality
* Inability to understand domain-specific documents
* Security and privacy concerns

DocuMind AI solves these challenges by combining intelligent retrieval techniques with robust guardrails and secure document management.

---

# 🚀 Key Features

## 📄 Intelligent Document Processing

* PDF Upload & Indexing
* Automatic Text Chunking
* Metadata Extraction
* Multi-document Support

---

## 🔍 Hybrid Retrieval System

Combines:

### Vector Search

* FAISS Vector Database
* Semantic Similarity Search

### Keyword Search

* BM25 Retrieval
* Exact Match Lookup

### Cross Encoder Reranking

* Context Re-ranking
* Improved retrieval precision

---

## 🤖 Multi-LLM Support

Switch seamlessly between:

### Local Models (Offline)

* Mistral
* Qwen 2.5

### Cloud Models (Online)

* Groq
* OpenAI GPT
* Anthropic Claude

---

## 🛡️ Hallucination Prevention

### Two-Stage Guardrails

* Context Verification
* Response Validation

Benefits:

* Reduced hallucinations
* Improved answer reliability
* Context-grounded responses

---

## 👥 Multi-Tenant Security

Each user receives:

* Isolated document storage
* Separate FAISS indexes
* Independent chat history
* Secure authentication

---

## 💬 Spring AI Companion Chatbot

A standalone conversational assistant built using Spring AI.

Features:

* Persistent chat history
* Context-aware conversations
* OpenAI Integration
* Secure user sessions

---

## 📊 RAG Evaluation Suite

Integrated evaluation using RAGAS metrics:

* Faithfulness
* Answer Relevancy
* Context Precision
* Context Recall
* Answer Correctness

---

# 🏗️ System Architecture

```text
CLIENT TIER
│
├── Browser UI
│
▼
SPRING BOOT UI GATEWAY (Port 8080)
│
├── Spring Security
├── Thymeleaf
└── OpenFeign
│
├─────────────► Backend Service (8081)
│                │
│                ├── MySQL
│                ├── Spring Data JPA
│                └── Spring AI Chatbot
│
└─────────────► FastAPI AI Service (8000)
                 │
                 ├── LangChain
                 ├── FAISS
                 ├── BM25
                 ├── Cross Encoder
                 └── RAG Pipeline
```

---

# 🧠 RAG Pipeline Flow

```text
User Question
      │
      ▼
Document Retrieval
      │
      ├── BM25 Search
      ├── FAISS Search
      │
      ▼
Hybrid Retriever
      │
      ▼
Cross Encoder Reranker
      │
      ▼
Guardrail Layer
      │
      ▼
LLM Generation
      │
      ▼
Response Validation
      │
      ▼
Final Answer
```

---

# 🛠️ Technology Stack

## Frontend

* HTML5
* CSS3
* JavaScript
* Thymeleaf

## Backend

* Spring Boot
* Spring Security
* Spring Data JPA
* OpenFeign

## AI Layer

* FastAPI
* LangChain
* Sentence Transformers
* Rank-BM25
* PyPDF

## Vector Database

* FAISS

## Database

* MySQL

## Chat Framework

* Spring AI
* ChatClient

## Evaluation

* RAGAS

## LLM Providers

* Ollama
* OpenAI
* Groq
* Anthropic

---

# 🔐 Security Features

* Spring Security
* Role-Based Authentication
* User Data Isolation
* Multi-Tenant Architecture
* Secure API Communication
* Protected Vector Stores

---

# 📂 Project Structure

```text
DocuMind-AI/
│
├── frontend/
│
├── frontenddoc/
│   ├── Controllers
│   ├── Security
│   └── Feign Clients
│
├── Documind_At/
│   ├── Spring AI
│   ├── JPA Entities
│   ├── Services
│   └── Repositories
│
├── ai_service/
│   ├── RAG Pipeline
│   ├── Vector Store
│   ├── Retriever
│   ├── Reranker
│   └── Evaluation
│
└── vector_store/
```

---

# ⚙️ Environment Configuration

## FastAPI Environment

Create `.env`

```env
LLM_PROVIDER=offline

ONLINE_PROVIDER=groq

GROQ_API_KEY=YOUR_KEY

OPENAI_API_KEY=YOUR_KEY

ANTHROPIC_API_KEY=YOUR_KEY

OLLAMA_MODEL=mistral

OLLAMA_REQUEST_TIMEOUT=60
```

---

## Spring Boot Database Configuration

```properties
server.port=8081

spring.datasource.url=jdbc:mysql://localhost:3306/documind_db

spring.datasource.username=root

spring.datasource.password=YOUR_PASSWORD

spring.jpa.hibernate.ddl-auto=update

spring.jpa.show-sql=true

spring.ai.openai.api-key=YOUR_OPENAI_KEY
```

---

# 🚀 Installation & Setup

## Step 1: Create Database

```sql
CREATE DATABASE documind_db;
```

---

## Step 2: Run FastAPI AI Service

```bash
cd code/ai_service

python -m venv .venv

# Windows
.venv\Scripts\activate

pip install -r requirements.txt

uvicorn main:app --reload --host 0.0.0.0 --port 8000
```

---

## Step 3: Run Spring Boot Backend

```bash
cd code/Documind_At

mvnw.cmd spring-boot:run
```

Runs on:

```text
http://localhost:8081
```

---

## Step 4: Run UI Gateway

```bash
cd code/frontenddoc

mvnw.cmd spring-boot:run
```

Runs on:

```text
http://localhost:8080
```

---

## Step 5: Access Application

Open:

```text
http://localhost:8080
```

Then:

* Register a new account
* Login securely
* Upload documents
* Configure retrieval settings
* Start asking questions

---

# 📊 Evaluation Metrics

| Metric             | Purpose                          |
| ------------------ | -------------------------------- |
| Faithfulness       | Measures factual grounding       |
| Answer Relevancy   | Query-answer alignment           |
| Context Precision  | Relevant retrieved chunks        |
| Context Recall     | Coverage of required information |
| Answer Correctness | Overall answer quality           |

---

# 🌟 Future Enhancements

* Multi-PDF Collections
* Document Summarization
* Voice-based Querying
* Agentic RAG Workflows
* GraphRAG Integration
* Multi-modal RAG (Images + Documents)
* Kubernetes Deployment
* Enterprise SSO Authentication

---

# 👨‍💻 Developed By

**Amit Yadav**

Hybrid RAG • Generative AI • Spring Boot • FastAPI • LangChain • Vector Databases

---

# 📜 License

This project is licensed under the MIT License.

---

⭐ If you found this project useful, please consider starring the repository!
