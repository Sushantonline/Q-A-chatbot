# 📚 Multimodal Q&A and Data Analysis App (RAG-based)

A **universal multimodal Q&A and data exploration tool** that uses **Retrieval-Augmented Generation (RAG)** with **Gemini** to answer natural-language questions from uploaded documents, spreadsheets, images, or web pages.

It also supports **conversational data analysis** — converting CSV or Excel files into **SQLite-backed data sessions** so you can run SQL-like analytics using **natural language prompts**.

---

## 🚀 Features

✅ **Multimodal Input Support**
- Handles PDF, DOCX, PPTX, TXT, CSV, XLSX, Images (JPG/PNG), and Web URLs  
- Automatically extracts and chunks document text for semantic retrieval  

✅ **Natural Language Data Analysis**
- Converts CSV/Excel files into SQLite tables  
- Gemini translates user prompts into SQL or Pandas-style queries  
- Enables quick insights like:  
  - “Show me the top 5 states by accident severity”  
  - “Plot the trend of revenue over years”  

✅ **Retrieval-Augmented Generation (RAG)**
- Contextual answering from multiple uploaded sources  
- Embedding-based similarity retrieval via **ChromaDB**

✅ **Memory + Source Attribution**
- Keeps chat history for follow-up questions  
- Displays which document, page, or chunk an answer originated from  

✅ **Streamlit UI**
- Unified interface for uploads, chat, and analysis  
- Real-time conversational insights and visualizations  

---





![image](https://github.com/user-attachments/assets/55d49e5d-fa11-49b5-a929-dbbd8cc9a39a)


## 🏗️ Project Structure

multimodal_qa_app/

├── main_app.py         # Main Streamlit application, UI, orchestration

├── config.py           # Configuration (model names, constants)

├── utils.py            # General utility functions

├── file_parsers.py     # Functions for parsing different file types

├── image_processor.py  # Image handling, OCR/VLM calls

├── web_crawler.py      # URL finding and crawling functions

├── vector_store.py     # ChromaDB interactions, embedding, context retrieval

├── qa_engine.py        # Q&A logic, data query handling, suggestions

├── requirements.txt    # Dependencies

└── .streamlit/

    └── secrets.toml    # For storing API keys locally

## ⚙️ Setup Instructions

Set up secrets: Create .streamlit/secrets.toml with your GOOGLE_API_KEY or set it as an environment variable.

**Install dependencies:**

`pip install -r requirements.txt`

**Run the main app:**

`streamlit run main_app.py`

or

`python -m streamlit run main_app.py`

## 🧩 Example Queries

| Input Type | Example Query                                                       |
| ---------- | ------------------------------------------------------------------- |
| **PDF**    | “Summarize key findings from page 3 of the report.”                 |
| **CSV**    | “Show correlation between GDP and accident rate.”                   |
| **Excel**  | “Which state has the highest YoY increase in accidents?”            |
| **Image**  | “Extract text and summarize the table shown.”                       |

## To Do
1. Adding functionality to redirect images/ tables in pdf to corresponding modules
2. Visualisation module and Suggesting plots along with prompts in chat


**Authors**

Sushant

Senthil
