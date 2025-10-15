# 🤖 MAT496: Advanced LLM Applications with LangChain
**Monsoon 2025 | Building Intelligent Research Assistants**

---

## 📚 Course Overview

This repository tracks my journey through building production-ready LLM applications using the LangChain ecosystem. The course culminates in a capstone project: developing an AI-powered research assistant.

### Core Learning Modules

| Module | Focus Area | Status |
|--------|-----------|--------|
| 🔗 **LangChain Fundamentals** | Core concepts, chains, and agents | In Progress |
| 📊 **LangSmith** | Observability, testing, and evaluation | Planned |
| 🕸️ **LangGraph** | Building stateful, graph-based agents | Planned |
| 🎯 **Capstone Project** | Deep research with multi-agent systems | Planned |

---

## 🎯 Capstone Project Ideas

- 📝 **Scientific Research Review Assistant** - Help researchers synthesize literature and identify research gaps
- ⚖️ **Legal Case Builder** - Assist lawyers in gathering precedents and building arguments
- 📈 **Economic Policy Analyzer** - Generate policy implication reports with data-driven insights
- 💡 **Custom Application** - Domain-specific intelligent assistant

---

## 📈 Progress Tracker

### ⏱️ Week 1 | Oct 01 - Oct 07, 2025

#### 🎯 Objectives
- [x] Set up development environment
- [x] Complete LangChain basics tutorial
- [x] Initialize project repository

#### 💻 Daily Updates

<details>
<summary><b>📅 Day 1 (Oct 01)</b> - Environment Setup & First LangChain Models</summary>

**✅ Completed:**
- Initialized Git repository with SSH authentication
- Configured Python virtual environment (Python 3.9)
- Installed core dependencies: `langchain`, `python-dotenv`, `langchain-groq`
- Successfully integrated Groq API for LLM access
- Implemented basic model invocation with `llama-3.3-70b-versatile`
- Explored streaming responses for real-time token generation
- Experimented with multi-turn conversations using SystemMessage and HumanMessage
- Tested multiple Groq models including `meta-llama/llama-4-maverick-17b-128e-instruct`

**🧪 Experiments Conducted:**
1. **Basic Model Calls** - Simple prompt-response interactions with various prompts
2. **Context-aware Conversations** - System prompts for translation (English → Bengali, Haryanvi)
3. **Code Generation** - Prompted model to generate Python code for algorithmic tasks (e.g., finding max of n numbers)
4. **Streaming Responses** - Implemented token-by-token streaming with time delays
5. **Multi-Model Comparison** - Initialized and tested different Llama models
6. **Complex Prompts** - Generated visual constellation representations using ASCII art

**💡 Key Learnings:**
- LangChain abstracts model initialization across providers (Groq, OpenAI, etc.)
- `init_chat_model()` provides a unified interface for different LLM backends
- Streaming enables real-time user feedback for longer responses
- SystemMessage sets context/behavior, HumanMessage represents user input
- LLMs can handle complex reasoning tasks including logic puzzles (snail climbing problem)
- Model performance varies with prompt complexity and question type

**📝 Code Highlights:**
```python
# Model initialization with Groq
from langchain.chat_models import init_chat_model
model = init_chat_model("llama-3.3-70b-versatile", model_provider="groq")

# Conversational pattern with context
from langchain_core.messages import HumanMessage, SystemMessage
messages = [
    SystemMessage("Generate python code for given tasks"),
    HumanMessage("Find max of given n numbers"),
]
response = model.invoke(messages)

# Streaming responses
for token in model.stream("hello"):
    print(token.content, end="", flush=True)
```

**⏰ Time Spent:** 4 hours

</details>

<details>
<summary><b>📅 Day 2-7 (Oct 02 - Oct 07)</b> - Prompt Engineering & RAG Basics</summary>

**✅ Completed:**
- Explored prompt templating and formatting best practices
- Implemented RAG (Retrieval Augmented Generation) prompt patterns
- Practiced question-answering with context
- Worked with external documents (PDF, TXT files) using pdfplumber
- Experimented with news articles and document summarization
- Built semantic search and retrieval foundations

**🧪 Experiments Conducted:**
1. **Prompt Templates** - Created reusable prompt structures for translations and Q&A
2. **RAG Pattern** - Implemented retrieval-augmented generation for context-aware responses
3. **Document Processing** - Loaded and processed PDFs and text files as context
4. **Multi-format Context** - Tested with news articles, books, and structured documents
5. **Context Summarization** - Generated summaries of documents within prompt constraints
6. **MLA Formatting** - Generated academically formatted responses with citations

**💡 Key Learnings:**
- RAG is fundamentally about "shoving relevant information in the prompt"
- Prompt templates enable reusable, parameterized prompts
- Token limits require strategic context selection
- Document chunking and retrieval improve response relevance
- Model performance improves with well-structured context
- Different question types require different context strategies

**📝 Code Highlights:**
```python
# Prompt template pattern
prompt_template = """You are an assistant for question-answering tasks. 
Use the following pieces of retrieved context to answer the question. 
If you don't know the answer, just say that you don't know. 
Use three sentences maximum and keep the answer concise.
Question: {question} 
Context: {context} 
Answer:"""

# Using template
prompt = prompt_template.format(
    context="Ajit was born in 1984, the current year is 2025", 
    question="How old is Ajit?"
)
response = model.invoke(prompt)
```

**⏰ Time Spent:** 6-8 hours total

</details>

#### 📊 Week 1 Summary
**Key Achievements:**
- Successfully set up LangChain development environment
- Mastered basic model invocation and streaming
- Understood and practiced RAG fundamentals
- Learned prompt engineering principles
- Experimented with multiple document formats and retrieval patterns

**Challenges Faced:**
- Google Generative AI embeddings quota limitations (encountered during vector store implementation)
- Token limits when processing large documents
- Managing API credentials securely across notebooks

**Next Week Goals:**
- Resolve Google Cloud credentials setup for semantic search
- Implement semantic search with embeddings
- Build a functional RAG system with vector stores
- Begin exploring LangChain chains and more complex pipelines

---

### ⏱️ Week 2 | Oct 08 - Oct 14, 2025

#### 🎯 Objectives
- [ ] Complete LangChain tutorials
- [ ] Build first semantic search system
- [ ] Implement working RAG pipeline
- [ ] Experiment with different LLM providers

#### 💻 Daily Updates

<details>
<summary><b>📅 Day 1-7 (Oct 08 - Oct 14)</b></summary>

**Status:** In Progress

</details>

---

### ⏱️ Week 3 | Oct 15 - Oct 21, 2025

[Coming Soon]

---

## 🛠️ Tech Stack

```
├── LangChain          # Framework for LLM applications
├── LangSmith          # Monitoring and evaluation
├── LangGraph          # Stateful agent orchestration
├── Python 3.9+        # Core language
├── Groq API           # Fast LLM inference
├── Google Generative AI # Embeddings (quota limits noted)
├── OpenAI API         # Backup LLM provider
└── Git/GitHub         # Version control
```

---

## 📁 Repository Structure

```
MAT496-Monsoon2025/
├── mod01_langchain_basics/
│   ├── nb01_langchain_basic_chatbot.ipynb
│   ├── nb01a_models_IQ_testing.ipynb
│   └── nb02_prompts.ipynb
├── mod02_semanticSearch_RAG/
│   ├── nb01_simple_RAG.ipynb
│   └── genai_key_2.json
├── notebooks/         # Additional experiments
├── src/              # Source code (to be organized)
├── docs/             # Documentation
└── capstone/         # Final capstone project
```

---

## 🚀 Quick Start

```bash
# Clone the repository
git clone git@github.com:hoodamailmi-arch/MAT-LLM-2025.git

# Navigate to project
cd MAT496-Monsoon2025

# Create virtual environment
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt

# Set up environment variables
cp .env.example .env
# Add your API keys to .env:
# GROQ_API_KEY=your_key
# OPENAI_API_KEY=your_key
# GOOGLE_APPLICATION_CREDENTIALS=path_to_json
```

---

## 🔑 Key Concepts Learned

### LangChain Basics
- **Chat Models**: Using `init_chat_model()` for provider-agnostic model access
- **Messages**: SystemMessage, HumanMessage, AIMessage for conversation flow
- **Streaming**: Real-time token generation for interactive applications
- **Providers**: Groq (fast), OpenAI (capable), Google Generative AI (embeddings)

### Prompt Engineering
- **Prompt Templates**: Parameterized prompts for reusability
- **Few-shot Learning**: Examples improve model output quality
- **Context Windows**: Strategic context placement within token limits
- **Structured Output**: Formatting requests for specific response types

### RAG (Retrieval Augmented Generation)
- **Semantic Search**: Finding relevant documents using embeddings
- **Vector Stores**: In-memory and persistent document storage
- **Chunking**: Strategic document splitting for optimal retrieval
- **Context Injection**: Feeding retrieved documents into prompts

---

## 📊 Learning Metrics

| Metric | Target | Current |
|--------|--------|---------|
| Tutorials Completed | 15 | 3 |
| Projects Built | 5 | 0 |
| Code Commits | 100+ | ~5 |
| Documentation Pages | 10 | 1 |

---

## 🎓 Course Instructor

**Professor:** [Name]  
**Institution:** [University Name]  
**Semester:** Monsoon 2025

---

## 📚 Resources

- [LangChain Official Docs](https://python.langchain.com/docs/)
- [LangSmith Academy](https://academy.langchain.com/courses/intro-to-langsmith)
- [LangGraph Tutorials](https://academy.langchain.com/courses/intro-to-langgraph)
- [Groq API Documentation](https://console.groq.com)
- [Google Generative AI Docs](https://ai.google.dev)

---

## ⚠️ Known Issues & Notes

1. **Google Cloud Credentials**: Encountering `DefaultCredentialsError` and quota limits on free tier embeddings. Planning to either upgrade account or switch to alternative embedding service.
2. **Large Document Processing**: Token limits require careful context selection and document chunking strategies.
3. **API Rate Limits**: Groq and Google APIs have usage limits on free tier accounts.

---

## 📝 License

This project is part of academic coursework for MAT496.

---

## 📞 Contact

**Student:** Soumya Hooda  
**Email:** hoodamailmi@gmail.com  
**GitHub:** [@hoodamailmi-arch](https://github.com/hoodamailmi-arch)

---

<div align="center">

**⭐ Last Updated:** October 16, 2025

*Building the future of AI-powered research, one commit at a time.*

</div>
