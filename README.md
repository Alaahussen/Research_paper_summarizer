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

---

## 🧱 Repository Structure

