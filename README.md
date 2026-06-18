# 🏦 AI Bank Statement Document Automation with LLM & Personal Financial Analysis

[![Python](https://img.shields.io/badge/Python-3.10+-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org)
[![License](https://img.shields.io/badge/License-Apache_2.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)
[![CrewAI](https://img.shields.io/badge/Agent_Framework-CrewAI%20+%20LangGraph-green)](https://github.com/crewAIInc/crewAI)

**Automated extraction, structuring, RAG-powered querying, and AI-agent financial analysis of bank statement PDFs with strong PII protection.**

This project converts unstructured bank statement PDFs into structured data using computer vision (YOLO), OCR, and Large Language Models. It features **CrewAI Skills**, secure **PII handling**, and an enhanced RAG pipeline for natural language financial analysis.

---

## ✨ Key Features

- **Advanced Document Parsing** — Custom YOLOv8 layout detection + OCR + LLM table extraction
- **CrewAI Skills Support** — Domain-specific skills for bank statement parsing, PII handling, and financial analysis
- **Enhanced RAG Pipeline** — Secure retrieval with PII redaction before embedding
- **Autonomous AI Agents** — Built with **CrewAI + LangGraph** (with deepagents exploration)
- **Financial Intelligence** — Income/expense categorization, trend analysis, and monthly/yearly summaries
- **Strong PII Protection** — Automatic detection and redaction before vector storage
- **Multimodal & Local LLM Support** — Works with Gemini, Ollama, and local models
- **User Interface** — Streamlit web application
- **Evaluation** — DeepEval + Opik integration for quality monitoring

---

## 🛠 Technology Stack

- **Document Processing**: YOLOv8, PyMuPDF, pytesseract, pymupdf4llm
- **RAG & Vector Store**: LangChain, Chroma, FAISS, Qdrant
- **Agent Framework**: CrewAI + LangGraph
- **LLMs**: Google Gemini, Ollama (Qwen, DeepSeek, Llama, etc.)
- **Frontend**: Streamlit
- **Evaluation & Observability**: DeepEval, Opik, Weights & Biases
- **Security**: PII redaction before vector storage

---

## 📁 Project Structure

```bash
AI-Bank-Statement-Document-Automation/
├── backend/
│   ├── app/
│   │   ├── core/                  # Configuration & logging
│   │   ├── models/                # Pydantic schemas
│   │   ├── services/              # Business logic (Document, RAG, Agent, Financial)
│   │   ├── skills/                # CrewAI Skills (bank-statement, PII, financial, RAG)
│   │   ├── utils/
│   │   └── main.py
│   └── tests/
├── frontend/
│   └── streamlit_app/             # Streamlit UI
├── notebooks/                     # Development & experimentation
├── data/
│   ├── uploads/
│   ├── processed/
│   └── vector_stores/
├── docker/
├── scripts/
├── docs/
├── .env.example
├── .gitignore
├── README.md
└── pyproject.toml
```

---

## 🚀 Quick Start

### 1. Clone & Setup

```bash
git clone https://github.com/johnsonhk88/AI-Bank-Statement-Document-Automation-By-LLM-And-Personal-Finanical-Analysis-Prediction.git
cd AI-Bank-Statement-Document-Automation-By-LLM-And-Personal-Finanical-Analysis-Prediction

# Create virtual environment
python -m venv venv
source venv/bin/activate

# Install dependencies
pip install -r backend/requirements.txt
```

## Create a .env file and add your GOOGLE_API_KEY (for Gemini).

### 2. Run the Application
#### Streamlit Web UI

```bash
streamlit run frontend/streamlit_app/app.py
```

#### Development Notebooks

```bash
jupyter notebook notebooks/
```

## 🆕 Recent Improvements

- Added CrewAI Skills support (Bank Statement Parsing, PII Handling, Financial Analysis, RAG Query Handling)
- Implemented PII redaction before vector database storage
- Restructured project following modern architecture (AnythingLLM-inspired)
- Hybrid LangChain setup (exploring LangChain 1.x + deepagents)
- Improved agent workflow with better tool and skill integration


## 🗺 Roadmap

- Full production-ready pipeline with FastAPI backend
- Document Collections / Workspaces (AnythingLLM style)
- Advanced multi-bank statement support
- Docker + Kubernetes deployment
- Interactive dashboard with charts and insights
- Time-series forecasting for cash flow prediction


## 📄 License
This project is licensed under the Apache License 2.0.

---------------------------------------

Made with ❤️ for smarter personal finance automation in Hong Kong.
⭐ If you find this project useful, please consider giving it a star!

-------------------------------------



