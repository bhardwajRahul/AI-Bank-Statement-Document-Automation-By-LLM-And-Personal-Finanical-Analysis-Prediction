# 🏦 AI Bank Statement Automation with LLM & Personal Financial Analysis

[![Python](https://img.shields.io/badge/Python-3.12-3776AB?style=for-the-badge&logo=python)](https://www.python.org)
[![CrewAI](https://img.shields.io/badge/CrewAI-Agents-green?style=for-the-badge)](https://github.com/crewAIInc/crewAI)
[![LiteLLM](https://img.shields.io/badge/LiteLLM-Local%20%2B%20Cloud-orange?style=for-the-badge)](https://github.com/BerriAI/litellm)
[![License](https://img.shields.io/badge/License-Apache_2.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)

> **Intelligent document automation for bank statements** — Extract, structure, analyze, and query financial data from PDFs using **YOLO + OCR + LLM**, powered by **CrewAI agents** and **local LLMs** (LM Studio / Ollama).

---

## ✨ Key Features

- **Advanced PDF Parsing** — YOLO layout detection + OCR + LLM-based table extraction
- **CrewAI Agents & Skills** — Specialized skills for bank statement parsing, PII redaction, financial analysis, and RAG querying
- **Local LLM First** — Full support for **LM Studio** and **Ollama** via LiteLLM (with async `acompletion`)
- **Reasoning Model Support** — Automatically handles models that return content in `reasoning_content`
- **Secure RAG Pipeline** — PII redaction **before** embedding into vector database (Qdrant / Chroma)
- **Financial Intelligence** — Income/expense categorization, trend analysis, and natural language querying
- **Async Ready** — Modern async LLM calls for better performance with CrewAI
- **Development Notebook** — Rich Jupyter notebook for experimentation and rapid iteration

---

## 🛠 Tech Stack

| Component              | Technology                              |
|------------------------|-----------------------------------------|
| **LLM Orchestration**  | LiteLLM (LM Studio, Ollama, OpenAI, DeepSeek, etc.) |
| **Agent Framework**    | CrewAI + Skills                         |
| **Document Processing**| PyMuPDF, YOLO, OCR                      |
| **Vector Database**    | Qdrant, Chroma                          |
| **RAG**                | LangChain + PII redaction               |
| **Frontend (Optional)**| Streamlit                               |
| **Evaluation**         | DeepEval, Opik (optional)               |

---

## 📁 Project Structure


```bash
AI-Bank-Statement-Document-Automation/
├── backend/
│   └── app/
│       ├── core/
│       │   └── ai_agent_skills_dev.ipynb   # ← Main development notebook
│       ├── skills/                         # CrewAI Skills
│       │   ├── bank-statement-parsing/
│       │   ├── financial-analysis/
│       │   ├── pii-handling/
│       │   └── rag-query-handling/
│       └── ...
├── data/
│   ├── bank-statement-document/            # Sample PDFs
│   └── uploads/
├── requirements.txt
└── README.md
```

---


---

## 🚀 Quick Start (Local LLM Recommended)

### 1. Setup Environment

```bash
git clone https://github.com/johnsonhk88/AI-Bank-Statement-Document-Automation-By-LLM-And-Personal-Finanical-Analysis-Prediction.git
cd AI-Bank-Statement-Document-Automation-By-LLM-And-Personal-Finanical-Analysis-Prediction

python -m venv venv
source venv/bin/activate
pip install -r requirements.txt
```
## 2. Start LM Studio (Recommended)

Open LM Studio
Load a chat model (e.g. qwen2.5-7b-instruct or gemma-2-9b-it)
Start the local server on http://localhost:1234

## 3. Run the Main Notebook

```bash
jupyter notebook backend/app/core/ai_agent_skills_dev.ipynb
```

The notebook includes:

- CrewAI agent setup with LM Studio
- Async LLM calls
- Vector DB (Qdrant) with PII protection
- Bank statement analysis workflow

--------------


## 🔧 Key Configuration
### Using LM Studio (Default in notebook)

```python
llm = LLM(
    model="openai/qwen2.5-7b-instruct",
    base_url="http://localhost:1234/v1",
    api_key="lm-studio",
    temperature=0.6,
    max_tokens=1024,
)

```

### Async Direct Calls

```python
from litellm import acompletion

response = await acompletion(
    model="openai/your-model",
    base_url="http://localhost:1234/v1",
    api_key="lm-studio",
    messages=[{"role": "user", "content": prompt}]
)


```


## 🗺 Roadmap

- Production FastAPI backend
- Multi-document collections / workspaces
- Advanced financial forecasting
- Docker + Kubernetes deployment
- Improved Streamlit dashboard with charts


## 📄 License
This project is licensed under the Apache License 2.0.

---------------------------------------

Made with ❤️ for smarter personal finance automation in Hong Kong.
⭐ If you find this project useful, please consider giving it a star!

-------------------------------------



