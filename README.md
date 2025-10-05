
# 🧠 FactForge-RAG

[![Python](https://img.shields.io/badge/Python-3.9%2B-blue.svg)](https://www.python.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![LangChain](https://img.shields.io/badge/LangChain-Framework-orange)](https://www.langchain.com/)
[![ChromaDB](https://img.shields.io/badge/ChromaDB-Vector%20Store-yellow)](https://www.trychroma.com/)
[![Groq LLM](https://img.shields.io/badge/Groq-LLM-red)](https://groq.com/)
[![HuggingFace](https://img.shields.io/badge/HuggingFace-Embeddings-yellow.svg)](https://huggingface.co/)

---

**FactForge-RAG** is a modular **Retrieval-Augmented Generation (RAG)** pipeline that combines  
**[LangChain](https://www.langchain.com/)**, **[ChromaDB](https://www.trychroma.com/)**, and **[Groq LLMs](https://groq.com/)**  
to retrieve factual information from trusted sources and generate accurate, context-aware responses.

---

## 📋 Table of Contents
- [Features](#-features)
- [Project Structure](#-project-structure)
- [Installation](#-installation)
- [Environment Variables](#-environment-variables)
- [Usage](#-usage)
- [Example Output](#-example-output)
- [Tech Stack](#-tech-stack)
- [Future Improvements](#-future-improvements)
- [License](#-license)

---

## ⚡ Features

- **🌐 Web Document Loader** – scrape and ingest web sources (e.g., Wikipedia, custom URLs)  
- **🧩 Text Chunking** – split long texts into semantically meaningful chunks  
- **🧠 Embeddings** – generate vector representations with HuggingFace’s `all-MiniLM-L6-v2`  
- **🗂️ Vector Store** – store and query embeddings efficiently using ChromaDB  
- **🔎 Retriever** – fetch the most relevant context for a user query  
- **🤖 LLM Integration** – use **Groq LLM (`gpt-oss-120b`)** for reasoning and answer generation  
- **🔁 RAG Pipeline** – full end-to-end retrieval and generation workflow  

---

## 🗂️ Project Structure

```bash
factforge-rag/
│── factforge_rag.py      # Main RAG pipeline
│── requirements.txt      # Python dependencies
│── README.md             # Documentation
└── examples/             # Example queries and usage
````

---

## ⚙️ Installation

```bash
# Clone the repository
git clone https://github.com/yourusername/factforge-rag.git
cd factforge-rag

# (Optional) Create a virtual environment
python -m venv .venv
source .venv/bin/activate   # On Windows: .venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt
```

---

## 🔐 Environment Variables

Create a `.env` file (or export manually):

```bash
export GROQ_API_KEY="your_groq_api_key"
export LANGCHAIN_API_KEY="your_langchain_api_key"
export LANGCHAIN_TRACING_V2="true"
export USER_AGENT="FactForgeRAG/1.0"
```

---

## 🚀 Usage

```python
from factforge_rag import ragu

response = ragu("What happened in the 2008 Noida double murder case?")
print(response)
```

---

## 🧾 Example Output

**Query:**

```
Who were the main accused in the 2008 Noida double murder case?
```

**Answer:**

```
The primary accused were Dr. Rajesh Talwar and Dr. Nupur Talwar, the parents of Aarushi Talwar.
They were initially convicted but later acquitted by the Allahabad High Court in 2017.
```

---

## 🧰 Tech Stack

| Component       | Description                                     |
| --------------- | ----------------------------------------------- |
| **LangChain**   | Framework for building modular LLM applications |
| **ChromaDB**    | Vector store for efficient embedding search     |
| **Groq LLM**    | High-speed reasoning and inference engine       |
| **HuggingFace** | Pre-trained embedding models                    |

---

## 🚧 Future Improvements

* [ ] Add support for multiple vector stores (Pinecone, Weaviate)
* [ ] REST API and CLI for production use
* [ ] Interactive dashboard for querying and visualization
* [ ] Add streaming responses and conversation memory

---

## 📜 License

Released under the [MIT License](LICENSE).
Feel free to use, modify, and contribute to **FactForge-RAG**.

---

### 💡 Contributing

Contributions, issues, and feature requests are welcome!
Open a pull request or file an issue on [GitHub Issues](https://github.com/yourusername/factforge-rag/issues).

---

### 🌟 Acknowledgements

Built with ❤️ using
[LangChain](https://www.langchain.com/) • [Groq](https://groq.com/) • [ChromaDB](https://www.trychroma.com/) • [HuggingFace](https://huggingface.co/)

---

```

---


```
