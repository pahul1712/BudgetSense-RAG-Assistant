# 📊 BudgetSense-RAG Assistant

**BudgetSense-RAG** is an intelligent **Retrieval-Augmented Generation (RAG)** application built with **LangChain** and **AstraDB** that allows users to **query complex financial or government documents** — like the *Union Budget 2025–26* — and get precise, context-aware answers.

---

## 🔍 Features

- 🧾 **PDF-based Querying** – Upload any PDF (e.g., government, finance, or research reports) and ask natural-language questions.  
- 🧠 **RAG Pipeline** – Combines retrieval + generation to produce fact-grounded, concise answers.  
- ☁️ **AstraDB Vector Store** – Efficient semantic search powered by Cassandra & embeddings.  
- 🦜 **LangChain Integration** – Manages the document loading, embedding, retrieval, and LLM response workflow.  
- 🧩 **Google Colab Friendly** – Easily executable in notebooks for testing and demonstration.

---

## 🗂️ Dataset / Document Used

- **Document:** [Budget Speech 2025–26, Government of India (PDF)](./budget_speech.pdf)  
- **Source:** Ministry of Finance, Government of India.  
- **Content Highlights:** Agriculture reforms, MSME credit growth, AI in education, tax reforms, and fiscal strategy.

---

## ⚙️ Tech Stack

| Component | Tool |
|------------|------|
| Language Model | `ChatGroq` or any OpenAI-compatible LLM |
| Framework | `LangChain` |
| Vector Store | `AstraDB (Cassandra)` |
| Embeddings | `HuggingFace` / `OpenAI Embeddings` |
| Notebook | Google Colab (`.ipynb`) |
| File Type | PDF documents |

---

## 🚀 How It Works

1. **Load the PDF** using `PyPDFLoader` or `UnstructuredPDFLoader`.
2. **Split text** into chunks for embedding.
3. **Generate embeddings** and store them in **AstraDB**.
4. **Query** the document using natural language.
5. The **RAG chain** retrieves the most relevant chunks and generates context-grounded responses.

```python
from langchain.vectorstores import AstraDB
from langchain.chains import RetrievalQA
from langchain.embeddings import HuggingFaceEmbeddings
```

---

## 🧪 Example Queries

| ❓ Question                                     | 💬 Model’s Answer                                                                |
| ---------------------------------------------- | -------------------------------------------------------------------------------- |
| *What are the key goals of Budget 2025–26?*    | Accelerate growth, promote inclusivity, boost MSMEs, and enhance spending power. |
| *What is the focus of the agriculture engine?* | Launch of “Prime Minister Dhan-Dhaanya Krishi Yojana” covering 100 districts.    |
| *What changes are proposed for MSMEs?*         | Credit limits increased; new classification and support for exporters.           |


---

## 🧩 Folder Structure

```bash
BudgetSense-RAG/
│
├── BudgetSense_RAG.ipynb       # Main Google Colab notebook
├── budget_speech.pdf            # Example input document
├── requirements.txt             # Required dependencies
└── README.md                    # Project documentation
```

---

## 🧰 Installation & Setup

```
pip install langchain langchain-groq cassio datasets
pip install pypdf sentence-transformers
```

---

🌟 Future Enhancements

- 🗂️ Multi-document RAG system (upload multiple PDFs).
- 🌐 Streamlit web interface for interactive querying.
- 🔍 Integration with Groq LLaMA or Gemini 1.5 Flash for faster inference.


---

👨‍💻 Author

Pahuldeep Singh Dhingra\\\
🎓 M.S. in Data Science & Analytics, Florida Atlantic University 




