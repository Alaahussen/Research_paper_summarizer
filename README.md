Here is the **full `README.md` file** with markdown formatting, ready to be used in your project directory:

---

### 📘 `README.md`

```markdown
# 🧠 AI-Powered Research Paper Summarization Pipeline

This project leverages AI agents to **automatically discover, scrape, and summarize academic research papers**. The goal is to assist researchers, students, and professionals in quickly understanding key insights from scholarly documents without manually reading entire papers.

---

## 🚀 Overview

The system is built using a **multi-agent architecture** orchestrated by [CrewAI](https://github.com/joaomdmoura/crewAI). Each agent has a defined responsibility in the pipeline, and together they form a complete workflow from keyword input to research summary generation.

### 🧠 Agents

#### 1. **Keyword Agent**
- **Role**: Accepts user-provided research topics or keywords.
- **Goal**: Enhances and contextualizes the keyword to form useful search queries.
- **Output**: Query strings for academic search.

#### 2. **Search Agent (SerpAPI)**
- **Role**: Searches academic papers on **Google Scholar**.
- **Goal**: Fetches a list of papers related to the given query using **SerpAPI**.
- **Output**: Titles, URLs (PDF or accessible web), and snippets for each paper.

#### 3. **Scraping Agent**
- **Role**: Extracts paper content.
- **Goal**: Uses **BeautifulSoup** for HTML pages and **pdfplumber** for PDF documents to extract key paper sections.
- **Output Sections**: Abstract, Introduction, Methodology, Results, Dataset, Related Work.

#### 4. **Summarization Agent**
- **Role**: Summarizes the structured data.
- **Goal**: Uses an LLM to generate a human-readable, concise summary from all sections of the paper.
- **Output**: Paragraph-style summaries.

---

## 🧱 Project Structure

```

ai-research-summarizer/
│
├── agents/
│   ├── keyword\_agent.py           # Query generation logic
│   ├── search\_agent.py            # Searches via SerpAPI
│   ├── scraping\_agent.py          # Extracts sections using BeautifulSoup or PDFPlumber
│   └── summarization\_agent.py     # Summarizes the extracted paper content
│
├── data/
│   ├── step\_1\_keywords.json
│   ├── step\_2\_search\_results.json
│   ├── scraped\_papers.json
│   └── final\_summaries.json
│
├── output/
│   └── logs/                      # Optional logs and diagnostics
│
├── utils/
│   ├── section\_parser.py          # Text matching and section identification
│   └── pdf\_extractor.py           # PDF-to-text conversion
│
├── run\_pipeline.py                # Runs all agents in sequence
├── requirements.txt               # Dependencies list
└── README.md                      # You’re here!

````

---

## 🛠 Technologies Used

- [`CrewAI`](https://github.com/joaomdmoura/crewAI) – Agent orchestration framework
- `SerpAPI` – Google Scholar integration
- `BeautifulSoup` – Web page scraping
- `pdfplumber` – PDF text extraction
- `Pydantic` – Typed data models
- `OpenAI GPT / LLM` – Summarization

---

## ⚙️ Installation

1. Clone the repository:
```bash
git clone https://github.com/your-username/ai-research-summarizer.git
cd ai-research-summarizer
````

2. Install dependencies:

```bash
pip install -r requirements.txt
```

3. Set your API keys in a `.env` file or directly in your environment:

```env
SERPAPI_API_KEY=your-serpapi-key
OPENAI_API_KEY=your-openai-key
```

---

## 🧪 How to Use

### 1. Run the full pipeline

```bash
python run_pipeline.py --topic "Graph Neural Networks in Drug Discovery"
```

This executes all 4 agents in sequence: keyword → search → scrape → summarize.

### 2. Run individual steps (for debugging or customization)

```bash
python agents/keyword_agent.py
python agents/search_agent.py
python agents/scraping_agent.py
python agents/summarization_agent.py
```

---

## 📤 Output Files

* `step_2_search_results.json` – Paper titles, URLs, and snippets
* `scraped_papers.json` – Extracted sections from HTML/PDF
* `final_summaries.json` – Final one-paragraph summaries per paper

### ✨ Example Summary Output

```json
{
  "title": "Graph Neural Networks for Predicting Drug-Target Interactions",
  "url": "https://...",
  "summary": "This paper proposes a novel graph neural network architecture to model molecular structures and predict drug-target interactions. It introduces a dataset of protein-ligand pairs and reports improved accuracy over traditional methods. The work demonstrates strong potential for drug discovery pipelines."
}
```

---

## 🧠 Motivation

Reading and understanding academic papers is time-consuming. This AI agent system automates much of the research workflow—empowering you to focus on **insights** rather than search and structure.

---

## 📌 Future Improvements

* Support for other academic search engines (Semantic Scholar, ArXiv)
* Citations and reference extraction
* Topic clustering for multi-paper analysis
* UI to browse summaries

---

## 🤝 Contributions

We welcome contributions! Fork the repo and open a pull request with improvements.

---

## 📄 License

This project is licensed under the **MIT License**.

```

---

Let me know if you want this file saved and structured inside your repo as well, or if you'd like a pre-configured `run_pipeline.py`.
```
