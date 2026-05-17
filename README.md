

# CineRAG — Movie Recommender

A movie recommendation app built with Retrieval-Augmented Generation (RAG). It searches a database of IMDB's Top 1000 movies using vector similarity and generates personalized recommendations using Llama 3.3 70B via Groq.

---

## How it works

1. The user types a request or picks a quick prompt from the sidebar.
2. The app encodes the query using the `all-MiniLM-L6-v2` sentence embedding model.
3. FAISS searches the movie database for the most relevant matches.
4. The top results are passed to Llama 3.3 70B, which generates a detailed recommendation.

---

## Project structure

```
project/
├── app.py                  # Main Streamlit app
├── requirements.txt        # Python dependencies
├── movie_rag_pipeline.ipynb  # Notebook to build the RAG data
└── rag_data/
    ├── movies.index        # FAISS vector index
    ├── documents.pkl       # Movie text documents
    └── metadata.pkl        # Movie metadata (title, year, genre, etc.)
```

---

## Setup

### 1. Install dependencies

```bash
pip install -r requirements.txt
```

### 2. Build the RAG data

Run the notebook `movie_rag_pipeline.ipynb` from top to bottom. This generates the `rag_data/` folder with the FAISS index and movie documents.



## Tech stack

- Streamlit — web interface
- FAISS — vector similarity search
- sentence-transformers (`all-MiniLM-L6-v2`) — text embeddings
- Groq — LLM inference
- Llama 3.3 70B — answer generation
- IMDB Top 1000 — movie dataset

# Demo
<img width="296" height="168" alt="ScreenRecording" src="https://github.com/user-attachments/assets/8b2d0767-2c2b-4448-977a-60f4054ce163" />


To display the video: upload the recording file to your GitHub repo, then replace the link above with the actual raw URL.
