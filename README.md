# Retrieval-Augmented Generation (RAG) using Groq LLaMA-3

This project demonstrates a **Retrieval-Augmented Generation (RAG)** pipeline built using
LangChain and a **cloud-hosted LLaMA-3 model served via Groq**.

The system retrieves relevant context from local documents and uses a large language model
to generate grounded, context-aware answers — **without any local LLM dependencies**.


## Key Highlights

- LLaMA-3 inference via Groq API
- Document chunking and semantic retrieval
- Chroma vector database for persistence
- End-to-end RAG pipeline in a Jupyter Notebook


## Architecture Overview

1. Load documents from disk  
2. Split documents into overlapping chunks  
3. Generate embeddings for chunks  
4. Store embeddings in a Chroma vector database  
5. Retrieve relevant chunks for a query  
6. Generate an answer using Groq-hosted LLaMA-3  

### 1. Clone the Repository

```
git clone https://github.com/SamBro481/rag-demo.git
cd <your-repo>
```

### 2. Download Dependencies

```
pip install -r requirements.txt
```

### 3. Create .env file

Create a .env file with the following contents

```
GROQ_API_KEY=your_groq_api_key_here
LLM_MODEL=llama-3.1-8b-instant
CHUNK_SIZE=500
CHUNK_OVERLAP=50
```

### 4. Run the Notebook

```
jupyter notebook
```






