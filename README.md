# 🧠 AI-Powered Research Paper Summarization Pipeline

This project leverages AI agents to **automatically discover, extract, and summarize academic research papers** using a multi-agent system. It is designed for researchers, students, and professionals who want quick access to key insights from scholarly documents.

---

## 🚀 Project Overview

The pipeline uses **four AI agents** to handle the research process from keyword entry to summarization:

1. **Keyword Agent**  
   - Accepts user-defined research topics or keywords (e.g., "Graph Neural Networks in drug discovery").
   - Generates meaningful and contextual search queries.

2. **Search Agent (SerpAPI)**  
   - Uses SerpAPI to search **Google Scholar** for research papers relevant to the keyword.
   - Extracts titles, URLs, and snippets of top academic results.
   - Filters for **accessible PDFs** and **HTML pages**.

3. **Scraping Agent (BeautifulSoup & PDFPlumber)**  
   - Scrapes content from web pages using **BeautifulSoup**.
   - Extracts structured sections: `abstract`, `introduction`, `methodology`, `results`, `dataset`, and `related work`.
   - Handles PDFs using **pdfplumber** if a direct PDF URL is found.

4. **Summarization Agent (LLM)**  
   - Reads the structured data from each paper.
   - Produces a concise and well-organized summary combining key insights from all sections.


## 🧠 Technologies Used

- `CrewAI` – Multi-agent orchestration
- `SerpAPI` – Academic paper search via Google Scholar
- `BeautifulSoup` – HTML content scraping
- `pdfplumber` – PDF section extraction
- `OpenAI GPT / LLM` – Language model for summarization

---

## 📦 Installation

git clone https://github.com/Alaahussen/Research_paper_summarizer.git

cd ai-research-summarizer

pip install -r requirements.txt

## 📱 Streamlit Web App

A user-friendly Streamlit interface is included to let users:
- Input a research topic or keyword
- Launch the pipeline with a click
- View summaries of papers directly in the browser
