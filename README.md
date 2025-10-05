```markdown
# FactForge-RAG

FactForge-RAG is a modular **Retrieval-Augmented Generation (RAG)** pipeline that combines **LangChain**, **ChromaDB**, and **Groq LLMs**.  
It retrieves relevant knowledge from sources and augments it using a powerful reasoning model.

---

## Features
- **Web Document Loader**: scrape and ingest sources like Wikipedia or custom URLs  
- **Text Chunking**: split documents into semantically meaningful chunks  
- **Embeddings**: generate vector representations using HuggingFace's `all-MiniLM-L6-v2`  
- **Vector Store**: store and search embeddings efficiently using ChromaDB  
- **Retriever**: fetch the most relevant context for a query  
- **LLM Integration**: use Groq LLM (`gpt-oss-120b`) for reasoning and answer generation  
- **RAG Pipeline**: structured end-to-end retrieval and generation

---

## Project Structure
```

factforge-rag/
│── factforge_rag.py      # Main RAG pipeline
│── requirements.txt      # Python dependencies
│── README.md             # Documentation
└── examples/             # Example queries and usage

````

---

## Installation

```bash
# Clone the repository
git clone https://github.com/yourusername/factforge-rag.git
cd factforge-rag

# (Optional) Create a virtual environment
python -m venv .venv
source .venv/bin/activate   # On Windows: .venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt
````

---

## Environment Variables

Create a `.env` file or export manually:

```bash
export GROQ_API_KEY="your_groq_api_key"
export LANGCHAIN_API_KEY="your_langchain_api_key"
export LANGCHAIN_TRACING_V2="true"
export USER_AGENT="FactForgeRAG/1.0"
```

---

## Usage

```python
from factforge_rag import ragu

response = ragu("What happened in the 2008 Noida double murder case?")
print(response)
```

---

## Example Output

**Query:**

```
Who were the main accused in the 2008 Noida double murder case?
```

**Answer:**

```
The primary accused were Dr. Rajesh Talwar and Dr. Nupur Talwar, the parents of Aarushi Talwar. They were initially convicted but later acquitted by the Allahabad High Court in 2017.
```

---

## Tech Stack

* LangChain – framework for building LLM-based applications
* ChromaDB – vector database for embeddings
* Groq – high-speed LLM inference
* HuggingFace – embeddings models

---

## License

MIT License – free to use and modify.

---

## Future Improvements

* Support for multiple vector stores (Pinecone, Weaviate)
* API or CLI interface for easier deployment
* Interactive UI dashboard for querying

```

This version fixes:  
- Consistent bolding for section titles and feature names.  
- Proper inline code formatting using backticks.  
- Clean horizontal rules (`---`) separating sections.  
- Proper indentation for code blocks.  

If you want, I can also **optimize it further to be GitHub-ready with badges and links** for a professional look. Do you want me to do that?
```
