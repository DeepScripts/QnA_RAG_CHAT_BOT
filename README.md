
# 📘 PDF-Based Q&A Bot using RAG (Retrieval-Augmented Generation)

This project implements a **PDF-based Question Answering (Q&A) system** using **Retrieval-Augmented Generation (RAG)**.
The system reads a PDF document, understands its content, and generates **clear, well-structured, human-like answers** instead of directly copying text from the document.

The notebook is designed to run seamlessly on **Google Colab**.

---

## 🚀 Key Features

* 📄 Load and process any PDF document
* ✂️ Intelligent text chunking for better retrieval
* 🔍 Semantic search using vector embeddings (FAISS)
* 🤖 Large Language Model (LLM) for natural language answers
* ❌ Prevents verbatim copy-paste from the PDF
* ✅ Generates rewritten, exam-ready, and interview-ready answers
* 📚 Suitable for:

  * Academic notes
  * Viva preparation
  * Interview Q&A
  * Study assistants
  * Research document analysis

---

## 🧠 Architecture Overview

```
PDF → Text Chunks → Embeddings → Vector Store (FAISS)
                                 ↓
                           Relevant Context
                                 ↓
                         LLM + Prompt Template
                                 ↓
                         Human-like Answer
```

This approach ensures:

* High factual accuracy (answers come only from the PDF)
* No hallucination
* No direct copying of sentences

---

## 🛠️ Technologies Used

* **Python**
* **Google Colab**
* **LangChain (modular version)**
* **HuggingFace Transformers**
* **Mistral-7B-Instruct**
* **FAISS (Vector Database)**
* **Sentence-Transformers**
* **PyPDF**

---

## 📦 Installation (Handled Inside Notebook)

All required dependencies are installed directly inside the Colab notebook using pinned versions to avoid import errors:

* `langchain`
* `langchain-community`
* `langchain-core`
* `langchain-text-splitters`
* `langchain-huggingface`
* `transformers`
* `sentence-transformers`
* `faiss-cpu`
* `pypdf`

> ⚠️ **Important:** After installation, the runtime must be restarted once.

---

## ▶️ How to Use (Google Colab)

1. Open the notebook `QnA_BOT.ipynb` in Google Colab
2. Upload your PDF file to Colab
3. Update the PDF path in the notebook:

   ```python
   pdf_path = "/content/your_file.pdf"
   ```
4. Run all cells step by step
5. Ask questions like:

   ```python
   "Explain money laundering in simple terms."
   ```
6. Receive rewritten, clear, and meaningful answers

---

## ✨ Prompt Design (Anti-Copy Mechanism)

The system uses a **strict prompt template** that ensures:

* Answers are rewritten in original language
* No sentences are copied from the PDF
* Responses are structured in 4–6 academic sentences
* No page numbers or document references are mentioned

This makes the output ideal for **exams, viva, and interviews**.

---

## 📊 Output Example

**Question:**

> What is money laundering?

**Answer:**

> Money laundering refers to the process of making illegally obtained money appear legitimate. It involves hiding the true source of funds through financial transactions so they can be used openly. This practice supports criminal activities and weakens the financial system. Therefore, it is treated as a serious economic offence by law.

---

## 📁 Project Structure

```
📦 QnA_BOT
 ┣ 📜 QnA_BOT.ipynb
 ┣ 📜 README.md
```

---

## 🎯 Use Cases

* 📖 Study assistant for large PDFs
* 🎓 Exam and viva preparation
* 💼 Interview preparation
* 🧾 Legal / policy document analysis
* 🔬 Research paper understanding

---

## ⚠️ Notes & Best Practices

* Use **smaller PDFs or well-structured documents** for best results
* Avoid very large chunk sizes (default is optimized)
* Restart runtime after installing dependencies
* Internet access is required to load the HuggingFace model

---

## 📌 Future Enhancements

* Multi-PDF support
* Chat-style UI
* Answer length control (2-mark / 5-mark / 10-mark)
* Deployment as a web app (Streamlit / FastAPI)
* Support for Grok / OpenAI / Local LLMs

---

## 👤 Author

**Deep Shrivastav**
M.Sc. Data Science & AI


Just tell me.
