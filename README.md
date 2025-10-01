# 🤖 MAT496: Advanced LLM Applications with LangChain
**Monsoon 2025 | Building Intelligent Research Assistants**

---

## 📚 Course Overview

This repository tracks my journey through building production-ready LLM applications using the LangChain ecosystem. The course culminates in a capstone project: developing an AI-powered research assistant.

### Core Learning Modules

| Module | Focus Area | Resource |
|--------|-----------|----------|
| 🔗 **LangChain Fundamentals** | Core concepts, chains, and agents | [Tutorials](https://python.langchain.com/docs/tutorials/) |
| 📊 **LangSmith** | Observability, testing, and evaluation | [Academy Course](https://academy.langchain.com/courses/intro-to-langsmith) |
| 🕸️ **LangGraph** | Building stateful, graph-based agents | [Academy Course](https://academy.langchain.com/courses/intro-to-langgraph) |
| 🎯 **Capstone Project** | Deep research with multi-agent systems | [Academy Course](https://academy.langchain.com/courses/deep-research-with-langgraph) |

---

## 🎯 Capstone Project Ideas

- 📝 **Scientific Research Review Assistant** - Help researchers synthesize literature and identify research gaps
- ⚖️ **Legal Case Builder** - Assist lawyers in gathering precedents and building arguments
- 📈 **Economic Policy Analyzer** - Generate policy implication reports with data-driven insights
- 💡 **Custom Application** - Your domain-specific intelligent assistant

---

## 📈 Progress Tracker

### ⏱️ Week 1 | Oct 01 - Oct 07, 2025

#### 🎯 Objectives
- [ ] Set up development environment
- [ ] Complete LangChain basics tutorial
- [ ] Initialize project repository

#### 💻 Daily Updates

<details>
<summary><b>📅 Day 1 (Oct 01)</b> - Environment Setup & First LangChain Models</summary>

**✅ Completed:**
- Initialized Git repository
- Set up SSH authentication with GitHub
- Configured Python virtual environment
- Installed core dependencies: `langchain`, `python-dotenv`, `langchain-groq`
- Successfully integrated Groq API for LLM access
- Implemented basic model invocation with `llama-3.3-70b-versatile`
- Explored streaming responses for real-time token generation
- Experimented with multi-turn conversations using SystemMessage and HumanMessage
- Tested multiple Groq models including `meta-llama/llama-4-maverick-17b-128e-instruct`

**🧪 Experiments Conducted:**
1. **Basic Model Calls** - Simple prompt-response interactions
2. **Context-aware Conversations** - System prompts for translation (English → Bengali)
3. **Code Generation** - Prompted model to generate Python code for algorithmic tasks
4. **Streaming Responses** - Implemented token-by-token streaming with time delays
5. **Multi-Model Comparison** - Initialized and compared different Llama models

**💡 Key Learnings:**
- LangChain abstracts model initialization across providers (Groq, OpenAI, etc.)
- `init_chat_model()` provides a unified interface for different LLM backends
- Streaming enables real-time user feedback for longer responses
- SystemMessage sets context/behavior, HumanMessage represents user input

**📝 Code Highlights:**
```python
# Model initialization with Groq
model = init_chat_model("llama-3.3-70b-versatile", model_provider="groq")

# Conversational pattern with context
messages = [
    SystemMessage("Generate python code for given tasks"),
    HumanMessage("Find max of given n numbers"),
]
response = model.invoke(messages)
```

**🔗 Commits:**
- `[hash]` - Initial project setup with SSH
- `[hash]` - First LangChain implementation with Groq models
- `[hash]` - Added streaming and multi-model experiments

**⏰ Time Spent:** 4 hours

</details>

<details>
<summary><b>📅 Day 2 (Oct 02)</b></summary>

**✅ Completed:**
- [Add your accomplishments here]

**🚧 In Progress:**
- [What you're currently working on]

**🔗 Commits:**
- `[hash]` - [Commit description]

**⏰ Time Spent:** [hours]

</details>

<details>
<summary><b>📅 Day 3 (Oct 03)</b></summary>

**✅ Completed:**

**🚧 In Progress:**

**🔗 Commits:**

**⏰ Time Spent:**

</details>

#### 📊 Week 1 Summary
**Key Achievements:**
- 

**Challenges Faced:**
- 

**Next Week Goals:**
- 

---

### ⏱️ Week 2 | Oct 08 - Oct 14, 2025

#### 🎯 Objectives
- [ ] Complete LangChain tutorials
- [ ] Build first simple chain
- [ ] Experiment with different LLM providers

#### 💻 Daily Updates

<details>
<summary><b>📅 Day 1 (Oct 08)</b></summary>

**✅ Completed:**

**🚧 In Progress:**

**🔗 Commits:**

**⏰ Time Spent:**

</details>

<!-- Add more days as needed -->

#### 📊 Week 2 Summary
**Key Achievements:**

**Challenges Faced:**

**Next Week Goals:**

---

### ⏱️ Week 3 | Oct 15 - Oct 21, 2025

[Copy Week 2 template]

---

## 🛠️ Tech Stack

```
├── LangChain          # Framework for LLM applications
├── LangSmith          # Monitoring and evaluation
├── LangGraph          # Stateful agent orchestration
├── Python 3.10+       # Core language
├── OpenAI API         # LLM provider
└── Git/GitHub         # Version control
```

---

## 📁 Repository Structure

```
MAT496-Monsoon2025/
├── week_01/           # Weekly project folders
├── week_02/
├── notebooks/         # Jupyter notebooks for experiments
├── src/              # Source code
├── docs/             # Documentation
├── tests/            # Unit tests
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
# Add your API keys to .env
```

---

## 📊 Learning Metrics

| Metric | Target | Current |
|--------|--------|---------|
| Tutorials Completed | 15 | 0 |
| Projects Built | 5 | 0 |
| Code Commits | 100+ | 1 |
| Documentation Pages | 10 | 1 |

---

## 🎓 Course Instructor

**Professor:** [Name]  
**Institution:** [University Name]  
**Semester:** Monsoon 2025

---

## 📝 License

This project is part of academic coursework for MAT496.

---

## 📞 Contact

**Student:** Soumy Hooda  
**Email:** hoodamailmi@gmail.com  
**GitHub:** [@hoodamailmi-arch](https://github.com/hoodamailmi-arch)

---

<div align="center">

**⭐ Last Updated:** October 01, 2025

*Building the future of AI-powered research, one commit at a time.*

</div>
