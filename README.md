# 🎓 Virtual Assistant – RAG-based Support Bot

A Retrieval-Augmented Generation (RAG) powered virtual assistant designed to help students and users with academic and administrative queries. This assistant leverages content fetched from the **IIT Madras Discourse Platform** and the **IITM Content Portal**, enabling it to deliver relevant and accurate responses in natural language.

---

## 🚀 Features

- 🔍 **Context-Aware Question Answering**
  - Retrieves relevant chunks from IITM discourse and content pages before generating answers.
  
- 📚 **Knowledge-Base Integration**
  - Dynamically indexes IITM-specific content (e.g., course FAQs, announcements, resources).

- 🧠 **LLM + Vector Search**
  - Uses sentence-transformer embeddings for chunking and semantic search.
  - Integrates a local or cloud-hosted vector store (like FAISS or Chroma).

- 🛠️ **Built Using**
  - Python (FastAPI/Flask for backend)
  - LLM based embedding
  - Sqllite DB


---

## 📥 Data Sources

- **IITM Discourse(https://discourse.onlinedegree.iitm.ac.in/c/courses/tds-kb/34)**: Extracts threads, FAQs, and discussions relevant to courses and processes.
- **IITM Content Portal(https://tds.s-anand.net/#/2025-01/)**: Pulls course material metadata, links, schedules, and updates.

> Content is parsed, chunked with overlap, and stored in the vector database for similarity search during inference.

---

## 📦 Installation

```bash
git clone https://github.com/<your-username>/virtual-assistant-rag.git
cd virtual-assistant-rag
pip install -r requirements.txt
