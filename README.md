# Agentic AI — Course Notebooks

A progressive 4-week curriculum covering Python fundamentals through production-grade multi-agent AI systems, using Google Gemini and the Google Agent Development Kit (ADK) on Vertex AI.

---

## Course Structure

| Week | Day | Date | Topic |
|------|-----|------|-------|
| 1 | 1 | Apr 13 | Python & Jupyter/Colab Fundamentals |
| 1 | 2 | Apr 15 | Control Flow, Functions, OOP & File Handling |
| 2 | 1 | Apr 20 | Context Engineering & LLM Internals |
| 2 | 2 | Apr 22 | Generation Parameters & RAG Pipelines |
| 3 | 1 | Apr 27 | Agentic AI & Tool Use with Google ADK |
| 3 | 2 | Apr 29 | Multi-Agent Systems |
| 4 | 1 | May 4  | Advanced Multi-Agent Patterns |

---

## Notebooks

### Week 1 — Python Foundations

**[Week_1_Day_1_(4_13).ipynb](Week_1_Day_1_(4_13).ipynb)**
- Google Colab setup and Jupyter interface walkthrough
- Variables and core data types: `str`, `int`, `float`, `bool`
- Implicit and explicit type conversion (`int()`, `float()`, `str()`)
- Collections: lists, tuples, dictionaries
- Practical example: shopping cart built from a list of product dictionaries

**[Week_1_Day_2(4_15) (1).ipynb](<Week_1_Day_2(4_15) (1).ipynb>)**
- Lists, conditionals (`if` / `elif` / `else`), and `for` loops
- Filtering lists and building licence eligibility checker
- Functions (`def`) and lambda expressions
- File handling: reading/writing `.txt` and `.csv` files with `DictWriter`
- Error handling: `try` / `except` / `finally`
- Object-Oriented Programming: classes, instance methods, inheritance, polymorphism

---

### Week 2 — AI & LLM Concepts

**[Week_2_Day_1_(4_20).ipynb](Week_2_Day_1_(4_20).ipynb)**
- What is "context" in AI — system instructions, conversation history, user messages
- Context windows, token counting, and cost implications
- AI evolution: Traditional Programming → Machine Learning → Deep Learning → Generative AI
- Types of Generative AI: LLMs, image, audio, video, multimodal, and code generation
- LLM internals: tokenization, embeddings, Transformer architecture, self-attention, auto-regression, decoding strategies
- First Gemini API call via Vertex AI (`gemini-2.5-flash`)

**[Week_2_Day_2(4_22).ipynb](Week_2_Day_2(4_22).ipynb)**
- LLM generation parameters: Temperature, Top-k, Top-p, Max Output Tokens, Stop Sequences, Frequency Penalty, Presence Penalty
- Parameter combination strategies for different use cases (factual, creative, conversational)
- **RAG (Retrieval-Augmented Generation)** from scratch
- PDF text extraction with `pypdf` and text chunking strategies (fixed-size, sentence-window, recursive-paragraph)
- Vertex AI text embeddings (`text-embedding-004`) and ChromaDB vector storage
- Google ADK agent with a `retrieve_pdf_context` tool for grounded Q&A over PDFs

---

### Week 3 — Agentic AI with Google ADK

**[Week_3_Day_1_(4_27).ipynb](Week_3_Day_1_(4_27).ipynb)**
- Agentic AI vs. traditional LLMs: planning, tool use, stateful memory, iterative reasoning
- Core agentic design patterns: Reflection, Tool Use, Planning, Multi-Agent, RAG
- Google ADK setup: `Agent`, `Runner`, `InMemorySessionService`
- Creating tools as Python functions with docstrings the agent reads
- Calculator agent with `add_numbers`, `multiply_numbers`, `calculate_percentage` tools
- Weather agent returning structured dictionaries
- Travel planning agent combining weather, travel time, and packing recommendation tools
- Multi-turn conversation memory via session IDs

**[Week_3_Day_2(4_29).ipynb](Week_3_Day_2(4_29).ipynb)**
- Multi-Agent Systems architecture and patterns
- Google ADK agent classes: `LlmAgent`, `SequentialAgent`, `ParallelAgent`, `BaseAgent`
- Specialized agents: math agent and research/knowledge-base agent
- Coordinator / dispatcher pattern for routing tasks between agents
- Parallel agent execution for concurrent independent tasks
- Inter-agent communication via session state (`output_key`)

---

### Week 4 — Advanced Patterns

**[Week_4_Day_1(5_4).ipynb](<Week_4_Day_1(5_4).ipynb>)**
- Advanced multi-agent system design
- Production deployment considerations for ADK agents

---

## Technologies

| Technology | Purpose |
|------------|---------|
| Python 3.x | Core language |
| Google Colab | Cloud notebook environment |
| Google Gemini (`gemini-2.5-flash`) | LLM for agents and generation |
| Vertex AI | GCP-hosted model inference and embeddings |
| Google ADK (`google-adk`) | Agent Development Kit |
| `google-genai` | Gemini SDK |
| ChromaDB | Local vector store for RAG |
| `pypdf` | PDF text extraction |
| NumPy | Embedding vector operations |

---

## Prerequisites

- Google account with access to [Google Colab](https://colab.research.google.com)
- Google Cloud Project with **Vertex AI API** enabled and billing configured
- Basic familiarity with Python (covered from scratch in Week 1)
