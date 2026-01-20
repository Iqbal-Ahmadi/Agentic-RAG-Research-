# Agentic RAG for Research (PDF Q&A)

An **agentic Retrieval-Augmented Generation (RAG)** project for research.  
Upload a **PDF** and ask questions to get **relevant, grounded answers** from the document (with citations when available).

---

## Features
- 📄 Upload PDF(s) and build an index automatically
- 🔎 Semantic retrieval to find the most relevant passages
- 🧠 Agentic flow (search → refine → answer) for better accuracy
- 🧾 Answers grounded in the PDF context (citations/snippets if enabled)
- ⚡ Fast repeated queries using cached embeddings / vector store

---

## How it works
1. Extract text from PDF and split it into chunks
2. Generate embeddings for chunks and store them in a vector database
3. On a user question, retrieve top relevant chunks (optionally rerank)
4. The agent may perform multiple retrieval steps
5. The LLM generates a final answer using only retrieved context

---

## Tech Stack
> Update these lines to match your project.
- **Backend:** Python
- **UI/API:** (Streamlit / FastAPI / Gradio)
- **Embeddings:** (OpenAI / SentenceTransformers / etc.)
- **Vector DB:** (FAISS / Chroma / Pinecone / etc.)
- **PDF Parsing:** (PyMuPDF / pdfplumber / unstructured)

---

## Requirements
- Python **3.10+**
- (Optional) API key if using hosted LLM/embeddings

---

## Installation
```bash
git clone <YOUR_REPO_URL>
cd <YOUR_REPO_FOLDER>

python -m venv .venv
# Windows:
.venv\Scripts\activate
# Linux/macOS:
source .venv/bin/activate

pip install -r requirements.txt
