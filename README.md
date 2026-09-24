# LangChain Learning & Experimentation

A hands-on Python project for learning and experimenting with **LangChain**, Large Language Models (LLMs), tools, messages, structured outputs, and model integrations.

The project contains a collection of Jupyter notebooks that progressively explore important LangChain concepts and practical implementations.

---

## Features

- LangChain fundamentals
- LLM model integration
- OpenAI model integration
- Message handling
- System, Human, and AI messages
- Tool calling
- Function/tool integration
- Structured outputs
- Typed data and schemas
- Environment variable management
- Python virtual environment using `uv`
- Jupyter Notebook based experimentation

---

## 📂 Project Structure

```text
langchainupdated/
│
├── .venv/                    # Python virtual environment
│
├── langchain/                # LangChain-related source/package files
│
├── langchainupdated/         # Project package
│
├── src/                      # Source code
│
├── 1-langchainintro.ipynb    # Introduction to LangChain
├── 2-modelintegration.ipynb  # LLM model integration
├── 3-tools.ipynb             # Tools and tool calling
├── 4-messages.ipynb          # LangChain message types
├── 5-structuredoutput.ipynb  # Structured output
│
├── .env                      # Environment variables (not committed)
├── .gitignore                # Git ignore configuration
├── pyproject.toml            # Project configuration and dependencies
├── requirements.txt          # Python dependencies
├── uv.lock                   # Locked dependencies managed by uv
└── README.md                 # Project documentation
```
## 📚 Notebooks
1. LangChain Introduction

1-langchainintro.ipynb

Introduces the basic concepts of LangChain and how it connects applications with LLMs.

Topics include:

LangChain basics
LLM interaction
Prompts
Basic chains
Invoking models
2. Model Integration

2-modelintegration.ipynb

Explores how different LLM providers can be integrated into LangChain applications.

Topics include:

Model initialization
LLM invocation
OpenAI integration
Gemini integration
Groq integration
Model configuration
Environment variables
3. Tools

3-tools.ipynb

Explores how tools can extend the capabilities of an LLM.

Topics include:

Creating tools
Calling tools
Tool arguments
Tool invocation
Tool results
LLM + tool workflows

Example workflow:

User
  ↓
LLM
  ↓
Tool
  ↓
Tool Result
  ↓
LLM
  ↓
Final Response
4. Messages

4-messages.ipynb

Explores the message system used by LangChain.

Main message types:

SystemMessage
HumanMessage
AIMessage
ToolMessage

Example:

from langchain_core.messages import (
    SystemMessage,
    HumanMessage,
    AIMessage
)

Messages allow applications to maintain structured conversations between users, models, and tools.

5. Structured Output

5-structuredoutput.ipynb

Explores how LLM responses can be converted into structured and predictable data.

Topics include:

Structured responses
Typed schemas
TypedDict
Pydantic models
JSON-style outputs
Tool-based structured responses

Example:

from typing import TypedDict

class Response(TypedDict):
    answer: str
    confidence: float

Structured outputs are useful when the LLM response needs to be consumed programmatically.

## 🛠️ Technologies Used
Python
LangChain
OpenAI
Google Gemini
Groq
Jupyter Notebook
uv
python-dotenv
Git
GitHub
⚙️ Requirements
Python 3.9+
uv
Git
API key for the LLM provider you want to use
## 🔧 Installation
1. Clone the repository
git clone https://github.com/ragul-1021/langchain.git
2. Navigate into the project
cd langchain
3. Create/sync the environment using uv
uv sync
4. Activate the virtual environment

Windows PowerShell:

.venv\Scripts\activate
🔑 Environment Variables

Create a .env file in the project root.

Example:

OPENAI_API_KEY=your_api_key
GOOGLE_API_KEY=your_api_key
GROQ_API_KEY=your_api_key

Only add the API keys for the providers you actually use.

Never commit .env to GitHub.

Your .gitignore should contain:

.env
.venv/
__pycache__/
.ipynb_checkpoints/
▶️ Running the Notebooks

Start Jupyter using:

uv run jupyter notebook

or:

uv run jupyter lab

You can then open the notebooks in order:

1 → 2 → 3 → 4 → 5
🧠 Concepts Covered

The project focuses on understanding the core building blocks of modern LLM applications:

                    LangChain
                       │
        ┌──────────────┼──────────────┐
        ↓              ↓              ↓
      Models         Tools         Messages
        │              │              │
        ↓              ↓              ↓
    OpenAI/Gemini     APIs       Human/AI/System
        │              │
        └──────────────┼──────────────┘
                       ↓
               Structured Output
                       │
                       ↓
                Application Logic
🔐 Security

API keys and other secrets should be stored in environment variables.

Do not commit:

.env
API keys
Passwords
Access tokens
Private credentials

If an API key has accidentally been committed to Git history, revoke/rotate the key immediately.

📌 Learning Goals

This project is designed to build a practical understanding of:

How LangChain works
How applications communicate with LLMs
How different LLM providers are integrated
How messages are represented
How tools are connected to LLMs
How tool calling works
How structured outputs are generated
How LLM responses can be consumed by Python applications
How to manage Python dependencies using uv
👨‍💻 Author

Ragul B

GitHub:
```
https://github.com/ragul-1021
```

📄 License

This project is intended primarily for learning, experimentation, and educational purposes.

One thing I would **change before pushing this README**: your `pyproject.toml` currently has a very generic description (`"Add your description here"`), so I'd change that to something like:

```toml
description = "Hands-on learning and experimentation with LangChain, LLMs, tools, messages, and structured outputs."
