# TDS Virtual Teaching Assistant

An intelligent assistant that answers student questions based on scraped content from the TDS Jan 2025 course and Discourse posts.

## 🔧 Features
- Uses Ollama + `nomic-embed-text` for text embeddings.
- Stores embeddings in ChromaDB.
- Answers questions using Groq's `llama3-70b-8192` model.
- FastAPI backend with `/` POST endpoint.

## 📁 Files
- `scrape_tds_content.py` – Scrapes TDS website.
- `scrape_discourse.py` – Scrapes Discourse posts.
- `embed_and_store.py` – Embeds data & stores in ChromaDB.
- `app.py` – API that uses vector search + Groq to answer questions.

## 🚀 How to Run

```bash
# activate virtual env
.\venv\Scripts\activate

# Start API
uvicorn app:app --reload
