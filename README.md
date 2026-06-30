# 🧠 Agentic AI Self-Study Roadmap

Welcome to my personal self-study repository for learning and experimenting with **Agentic AI** and modern LLM orchestration frameworks. This repository serves as a learning journal and codebase for building intelligent, agentic, and production-ready LLM applications.

---

## 🗺️ Study Topics & Progress

### 1. 🦜 LangChain
* **Description**: The foundational framework for building LLM applications via composable chains, prompts, templates, and structured integration layers.
* **Key Focus Areas**:
  - Chat models and prompting patterns
  - Streaming and tool calling mechanics
  - Unified model instantiation (`init_chat_model`)
* **Notebooks / Code**: See [updatedlangchain/1-langchainintro.ipynb](file:///a:/LLM%20Studies/updatedlangchain/1-langchainintro.ipynb) for an introduction to LangChain and basic model invocations.

### 2. 🕸️ LangGraph
* **Description**: An orchestration framework built on top of LangChain to design agentic workflows as circular, stateful graphs (DAGs and cyclic graphs).
* **Key Focus Areas**:
  - State management (`StateGraph`)
  - Human-in-the-loop (HITL) workflows and manual interrupts
  - Multi-agent coordination and supervisor architectures
  - Persistence and memory checkpoints

### 3. 🔍 Retrieval-Augmented Generation (RAG)
* **Description**: Enhancing LLM outputs by retrieving relevant context from external databases before generation.
* **Key Focus Areas**:
  - Document chunking and parsing strategies
  - Vector embeddings and vector databases (Chroma, Pinecone, etc.)
  - Hybrid search and re-ranking (Cohere, Cross-Encoders)

### 4. 🔗 Vectorless RAG (Graph RAG & Search-based RAG)
* **Description**: Alternative RAG techniques that bypass standard vector-similarity databases by utilizing knowledge graphs or direct web searches/document indexing structures.
* **Key Focus Areas**:
  - Knowledge Graphs for context retrieval (Neo4j, GraphRAG)
  - Search engine APIs for real-time web context (Tavily, Bing Search)

### 5. 🛡️ Guardrails
* **Description**: Designing safety, validation, and restriction layers around LLM inputs and outputs to prevent hallucination, prompt injection, and toxic content.
* **Key Focus Areas**:
  - NeMo Guardrails, Llama Guard, and Guardrails AI
  - Programmatic validators (regex, Pydantic outputs)
  - Input/Output sanitization

### 6. 📊 Evaluations (Evals)
* **Description**: Programmatic testing and measurement of LLM system performance, reliability, and accuracy.
* **Key Focus Areas**:
  - Ragas / TruLens frameworks (faithfulness, answer relevance)
  - LLM-as-a-judge patterns
  - Dataset curations for benchmarking agents

---

## 🛠️ Tech Stack & Setup

This repository uses:
* **Python**: `>=3.12`
* **Package Manager**: Managed with `uv` (lockfile: `uv.lock`)
* **Libraries**: LangChain, LangChain-Groq, LangChain-OpenAI, LangGraph, python-dotenv

### Running Locally

1. Install dependencies:
   ```bash
   uv sync
   ```
2. Create a `.env` file in the root directory (never commit this to GitHub!) and configure your API keys:
   ```env
   OPENAI_API_KEY="your-openai-api-key"
   GROQ_API_KEY="your-groq-api-key"
   GOOGLE_API_KEY="your-google-api-key"
   ```
3. Run the Jupyter notebooks in `updatedlangchain/` or scripts using the virtual environment:
   ```bash
   .venv/Scripts/python -m ipykernel install --user --name=llm-studies
   ```

---

*Keep learning and building! 🚀*
