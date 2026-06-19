# IntelliSearch.ai

Local AI RAG-based file search with context-aware answers.

IntelliSearch.ai is a local, privacy-first search system that indexes files on your machine and answers natural-language questions about their contents. It supports documents, code, spreadsheets, PDFs, and images using local embeddings, FAISS, and an optional local LLM (Ollama). Data stays on your device.

## Features

- Semantic (meaning-based) file search
- Context-aware RAG (Retrieval Augmented Generation)
- File types: PDF, DOCX, PPTX, TXT, CSV, XLS/XLSX, and common code formats
- Image understanding via automatic captioning
- FAISS vector store for local retrieval
- Delta indexing (watchdog mode) for added, modified, and deleted files
- CLI chat and GUI chat (Tkinter)
- Fully local execution; no cloud upload required
- Modular project layout

Example queries:

- Which file talks about transformers?
- Open the file that contains authentication logic
- Summarize the PDF about machine learning

## How It Works

### 1. Indexing
- Files are parsed and chunked
- Text is summarized
- Images are captioned
- Embeddings are stored locally in FAISS

### 2. Search
- The user submits a natural-language query
- FAISS retrieves relevant chunks
- Context is assembled for the response

### 3. Answering
- If Ollama is available, the LLM generates an answer from retrieved context
- Otherwise, semantic search results are returned

## Setup

### 1. Clone the repository

```bash
git clone https://github.com/freeatom/IntelliSearch.ai.git
cd IntelliSearch.ai
