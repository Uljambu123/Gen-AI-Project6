# Summarize Text From YT or Website Using LLM

## 1. Project Overview

This project is a **Streamlit web application** that summarizes text from **YouTube videos or web pages** using **Large Language Models (LLMs)**. It leverages **LangChain**, **Groq API**, and other NLP tools to fetch and process content from online sources and provide concise summaries.

## 2. Objective

The goal of this project is to automate the process of summarizing textual content from **YouTube video transcripts** and **web pages**, making it easier for users to quickly grasp key information.

## 3. Key Steps in the Project

- **User Input:** Users provide a **URL** (YouTube or website) and their **Groq API key**.
- **URL Validation:** The system verifies if the given input is a valid URL.
- **Data Extraction:**
  - **YouTube videos:** Extracts transcripts using `YoutubeLoader`.
  - **Web pages:** Fetches and processes text using `UnstructuredURLLoader`.
- **Summarization Process:**
  - Uses **ChatGroq (Gemma-7B-It)** to generate a **300-word summary** of the extracted text.
  - Utilizes a **LangChain summarization chain** for text processing.
- **Result Display:** The summary is presented in a **Streamlit app** with error handling for invalid inputs.

## 4. Conclusions

- The application provides an **efficient way to summarize long-form content** from online sources.
- It is useful for quickly obtaining key insights without manually reading or watching the full content.
- The integration of **LLMs via LangChain and Groq API** enhances **text processing capabilities**.

## 5. Technologies Used

- **Programming Language:** Python
- **Frameworks & Libraries:**
  - `streamlit` (for UI)
  - `langchain`, `langchain_groq` (for LLM interaction)
  - `YoutubeLoader`, `UnstructuredURLLoader` (for data extraction)
  - `validators` (for URL validation)
  - `pandas`, `duckdb`, `openai`, `sentence_transformers` (for NLP processing)
- **LLM Model:** Gemma-7B-It via **Groq API**
- **Data Handling:** FAISS, ChromaDB, MySQL, SQLAlchemy

## 6. Future Work

- **Support for more LLMs:** Expand support to other models like GPT-4, Claude, or local models.
- **Multilingual Summarization:** Enable summaries in different languages.
- **Enhanced Summarization Options:** Provide **bullet points, detailed analysis, or key takeaways**.
- **Mobile Compatibility:** Improve UI for better mobile accessibility.

## 7. How to Run

### Step 1: Clone the Repository
```bash
git clone https://github.com/your-repo/summarize-text-yt-website.git
cd summarize-text-yt-website

Step 2: Create a Virtual Environment (Optional)
```bash
- python -m venv venv
- source venv/bin/activate   # On macOS/Linux
- venv\Scripts\activate      # On Windows

Step 3: Install Dependencies
```bash
- pip install -r requirements.txt

Step 4: Run the Streamlit App
```bash
- streamlit run "Summarize Text From YT or Website Using LLM.py"

Step 5: Provide API Key & URL
```bash
- Enter your Groq API key.
- Paste a YouTube video URL or a website URL.
- Click "Summarize" to get the text summary.
