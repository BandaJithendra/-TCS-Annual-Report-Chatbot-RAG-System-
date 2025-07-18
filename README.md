# 🤖 TCS Annual Report Chatbot (RAG System)

This is a Retrieval-Augmented Generation (RAG) powered chatbot built using the **TCS Integrated Annual Report 2024–2025**. It enables users to ask natural language questions and get contextually accurate responses based on the content of the annual report.

The backend uses **FAISS for vector search**, **BAAI/bge-base-en-v1.5 for embeddings**, and a **locally hosted LLM via Ollama** for generating natural language answers.

---

## 🚧 Project Status

- ✅ **Backend completed**:
  - PDF loading and preprocessing
  - Semantic chunking with overlap
  - Embedding generation using `BAAI/bge-base-en-v1.5`
  - FAISS vector store setup for similarity search
  - Local LLM integration using **Ollama** (e.g. Mistral or LLaMA)
  - Retrieval pipeline and response generation

- 🔜 **Frontend (UI) in progress**:
  - Planned UI with **Flask**
  - Users will interact with the chatbot through a clean web interface

---

## 📚 Key Features

- 📄 Knowledge base built from the official TCS Annual Report 2024–25
- 🔍 Semantic search using FAISS and BGE embeddings
- 🧠 Local LLM powered by **Ollama** (e.g., `mistral`, `llama3`, etc.)
- ⚡ Fast document retrieval and context-aware answers
- 💬 Natural language interface (UI coming soon)

---

## 🔧 Tech Stack

- **Python**
- **LangChain**
- **SentenceTransformers** (`BAAI/bge-base-en-v1.5`)
- **FAISS** (Vector Similarity Search)
- **Ollama** (Local LLM server)
- **PyMuPDF** or **PDFMiner** for PDF parsing

---

## 📁 Project Structure
📁 tcs-rag-chatbot/ <br/>
│ <br/>
├── chatbot_backend.ipynb # Jupyter Notebook with backend logic <br/>
├── tcs-annual-report-2024.pdf # Source document <br/>
├── requirements.txt # Python dependencies <br/>
└── README.md # Project overview (this file) <br/>


---

## ▶️ How to Run (Backend)

1. Install Python dependencies:
```bash
pip install -r requirements.txt
```
2. Start Ollama and pull your preferred model (e.g., mistral, llama3, etc.):
```bash
ollama run mistral
```
3. Open the notebook chatbot_backend.ipynb, and run each cell to:

  - Load the PDF
  - Split and embed text
  - Store vectors in FAISS
  - Query via semantic search
  - Generate responses using your local Ollama LLM
---
## 🧠 Sample Queries

- "Who is the current chairman of TCS?"
- "Explain TCS’s board diversity policy."
- "What is their approach to values and ethics?"

---
## 🔮 Coming Soon: Frontend

A user-friendly chatbot UI will be added using Streamlit or Gradio, enabling easy interaction with the RAG system directly from your browser.

---
## 🧪 Model Configuration Notes

- Embedding Model: BAAI/bge-base-en-v1.5 (with query prefix and normalization)
- LLM Model: Served locally via Ollama, compatible with LangChain.llms.Ollama
- Chunking: ~300–500 tokens with 10–15% overlap for better context
