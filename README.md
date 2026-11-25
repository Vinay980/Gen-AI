# Generative AI & LangChain Learning

A hands-on repository documenting my journey of learning **Generative AI, LangChain, LLM integrations, embeddings, document processing, and vector databases** through Python notebooks and practical experiments.

The repository is organized by topic so that each notebook focuses on a specific concept and its implementation.

## What I'm Learning

- Connecting LLM providers with LangChain
- Working with local models through Ollama
- Loading data from text files, PDFs, and web pages
- Splitting documents into manageable chunks
- Generating text embeddings with Ollama and Hugging Face
- Exploring vector databases and similarity search with FAISS
- Understanding the building blocks used in Retrieval-Augmented Generation (RAG)

## Repository Structure

```text
Gen-AI/
│
├── 1-Langchain/
│   ├── 1.1-OpenAI/
│   │   └── GettingStarted.ipynb
│   │
│   ├── 2-ollama/
│   │   └── 2.1-ollamaembedding.ipynb
│   │
│   ├── 3-DataIngestion/
│   │   ├── 3.1-DataIngestion.ipynb
│   │   ├── 3.2-textsplitter.ipynb
│   │   ├── 3.3-HTMLtextSplitter.ipynb
│   │   ├── 3.4-RecursiveJsonSplitter.ipynb
│   │   ├── Discover how ChatGPT is trained!.pdf
│   │   └── speech.txt
│   │
│   ├── 4-Huggingface/
│   │   └── 4.1HuggingFace.ipynb
│   │
│   ├── 5-VectorDB/
│   │   └── 5.1-Faiss.ipynb
│   │
│   └── embedding.ipynb
│
├── .env.example
├── .gitignore
└── requirements.txt
```

## Topics Covered

| Section | Concepts and hands-on work |
|---|---|
| **OpenAI** | Getting started with an LLM provider through LangChain |
| **Ollama** | Running local models and generating embeddings |
| **Data Ingestion** | Loading text, PDF, and web content with document loaders |
| **Text Splitting** | Character-based, HTML-aware, and recursive JSON splitting |
| **Hugging Face** | Creating text embeddings with Sentence Transformers |
| **Vector Databases** | Introduction to FAISS and vector similarity search |

> This is a work in progress. New notebooks and topics will be added as I continue learning.

## Tech Stack

- **Language:** Python
- **LLM framework:** LangChain
- **Model providers / runtimes:** OpenAI, Ollama, Hugging Face
- **Embeddings:** Ollama Embeddings, Hugging Face Sentence Transformers
- **Vector search:** FAISS, Chroma
- **Document processing:** LangChain document loaders and text splitters
- **Environment:** Jupyter Notebook, python-dotenv

## Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/Vinay980/Gen-AI.git
cd Gen-AI
```

### 2. Create and activate a virtual environment

**Windows PowerShell**

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
```

### 3. Install dependencies

```bash
python -m pip install --upgrade pip
pip install -r requirements.txt
```

### 4. Configure environment variables

Create a local `.env` file using `.env.example` as a template. Add only the credentials needed for the notebook you want to run.

Never commit your real `.env` file or API tokens to GitHub.

### 5. Start Jupyter

```bash
jupyter notebook
```

Open the notebook you want to explore and run its cells in order.

## Using Ollama (Local Models)

Some experiments use Ollama to run models locally.

1. Install Ollama from [ollama.com](https://ollama.com/).
2. Download a chat model when needed, for example:

   ```bash
   ollama pull llama3.2:1b
   ```

3. For embedding experiments, use a dedicated embedding model:

   ```bash
   ollama pull nomic-embed-text
   ```

4. Make sure the Ollama application/server is running before executing the notebook.

The model name in the notebook must match a model available in your local Ollama installation.

## Environment Variables

Use `.env.example` as a reference for the variable names used by the notebooks.

Typical setup:

```env
OPENAI_API_KEY=your_openai_api_key
LANGCHAIN_API_KEY=your_langsmith_api_key
HF_TOKEN=your_huggingface_token
```

Only add credentials for services you actually use. Keep `.env` local and private.

## Learning Roadmap

The repository currently focuses on LangChain fundamentals and its supporting components. The next learning areas include:

1. LangChain models and prompt templates
2. Chains and LangChain Expression Language (LCEL)
3. Document loaders and text splitters
4. Embeddings and vector stores
5. Retrievers and similarity search
6. Retrieval-Augmented Generation (RAG)
7. LangGraph and AI agents

## Notes

- These notebooks are for learning, experimentation, and practice.
- Some models may download automatically the first time they are used.
- API-based notebooks require valid credentials and may incur provider charges.
- Local model performance depends on your system hardware.
- Package APIs can change over time; refer to the official documentation when an integration changes.

## Useful Resources

- [LangChain Documentation](https://docs.langchain.com/)
- [Hugging Face Model Hub](https://huggingface.co/models)
- [Ollama Documentation](https://docs.ollama.com/)
- [FAISS Documentation](https://github.com/facebookresearch/faiss)

---

**Learning by building, experimenting, and documenting one concept at a time.**
