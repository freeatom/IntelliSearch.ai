# 🧠 IntelliSearch.ai  
## Local AI RAG-based File Context–Aware Search Engine

IntelliSearch AI is a **local, privacy-first AI search system** that indexes files on your PC and lets you **ask natural-language questions** about their contents.

It supports **documents, code files, spreadsheets, PDFs, and images**, using **local embeddings + FAISS + an optional local LLM (Ollama)** to deliver context-aware answers — without sending your data to the cloud.

---

## 🚀 Key Features

- 🔍 Semantic (meaning-based) file search  
- 🧠 Context-aware RAG (Retrieval Augmented Generation)  
- 📄 Supports PDF, DOCX, PPTX, TXT, CSV, XLS/XLSX, code files  
- 🖼️ Image understanding via automatic captioning  
- ⚡ FAISS vector database for fast local search  
- 🔄 Delta indexing (watchdog mode) — updates only changed files  
- 💬 CLI Chat + 🖥️ GUI Chat (Tkinter)  
- 🛡️ Fully local & privacy-first  
- 🧩 Clean, modular, production-style project structure

- Ask questions like:
“Which file talks about transformers?”
“Open the file that contains authentication logic”
“Summarize the PDF about machine learning”
---

## 🧠 How It Works

1. **Indexing**
   - Files are parsed and chunked
   - Text is summarized
   - Images are captioned
   - Everything is embedded and stored locally using FAISS

2. **Search**
   - User asks a natural-language query
   - FAISS retrieves relevant chunks
   - Context is dynamically assembled

3. **Answering**
   - If Ollama is available → LLM synthesizes an answer
   - Otherwise → semantic search results are shown

---

## 🛠️ Setup

1. Clone the Repository

- git clone https://github.com/freeatom/IntelliSearch.ai.git
- cd IntelliSearch.ai

2️. Create Virtual Environment
- python -m venv .venv
- .venv\Scripts\activate     # Windows
- .venv/bin/activate  # Linux / macOS

3. Install Dependencies
- pip install -r requirements.txt
- First run may download models and take a few minutes.

4. Install Ollama for LLM Answers (Recommended)
- Download Ollama: https://ollama.com
- ollama pull tinyllama:1.1b
- (Without Ollama, IntelliSearch.ai still works in search-only mode.)

▶️ Running the App
-   python main.py "C:/" - Provide Storage Drive Paths


## 💬 Usage Modes
🔹 **Index** (Must Run First Time to build Index Once)
- Builds a fresh vector index for the folder.

🔹 **Chat (CLI)**
🔹 **Watchdog**
- Incrementally updates the index by detecting:
- Added files
- Modified files
- Deleted files

🔹 **Chat (GUI)**
- Desktop UI
-   Clickable results (Open / Reveal)

## 🔒 Privacy:
✅ Fully local execution
✅ No cloud uploads
✅ No telemetry
❌ No external APIs required

## 🧪 Tested Environment:
OS: Windows 11
Python: 3.10
Torch: 2.5.1 + CUDA 12.1
GPU: NVIDIA (optional)
LLM: Ollama (tinyllama:1.1b)

## 🧠 Why IntelliSearch.ai?
Most AI search tools Require cloud APIs, Expose private data, Are closed-source.

**IntelliSearch.ai is different:**
Fully local,
Transparent,
Hackable,
Built like a real system, not a demo

🙌 **Acknowledgements:**
HuggingFace,
LangChain,
FAISS,
Ollama,
PyTorch.
