# AI and Machine Learning Research Intelligence Pipeline (2026)

This repository contains an **end-to-end intelligence pipeline** designed to automate the discovery, analysis, and scoring of academic literature. The system processes **7,000+ research papers** (scaled from the initial 1,500 record baseline) fetched from the ArXiv repository to identify emerging trends and high-signal research in Artificial Intelligence and Machine Learning.

## 🚀 Features

*   **Automated Data Acquisition:** Batch-fetches large-scale datasets from the ArXiv API using custom query parameters and rate-limit handling.
*   **NLP Cleaning & Enrichment:** Orchestrates a cleaning pipeline using **spaCy** for lemmatization and **YAKE** for automated keyword extraction.
*   **Topic Modeling (NMF):** Deconstructs the research landscape into 10 distinct thematic clusters, such as "Agents & Tool Use," "Reinforcement Learning," and "Memory Systems".
*   **Semantic Intelligence:** Utilizes **Sentence Transformers** (`all-MiniLM-L6-v2`) to generate dense vector embeddings, enabling "true meaning" retrieval and semantic search.
*   **Automated Research Agent:** 
    *   **Novelty Scoring:** Measures semantic distance from the corpus centroid to find "outlier" ideas.
    *   **Impact Detection:** Scans for high-value signals like "state of the art," "benchmark," and "open source".
    *   **LLM Synthesis:** Employs a local **Flan-T5** model to automatically extract core contributions and problem statements from top-ranked papers.

## 🛠️ Tech Stack

*   **Data Science:** Pandas, NumPy, Scikit-learn
*   **NLP:** spaCy, NLTK, YAKE, Sentence-Transformers
*   **AI/LLM:** Hugging Face Transformers (Flan-T5)
*   **Visualization:** Matplotlib, Seaborn, t-SNE

## 📊 Pipeline Workflow

1.  **Ingestion:** Fetch 7,000+ papers via ArXiv API.
2.  **Preprocessing:** Clean text and extract tokens/keywords.
3.  **Thematic Analysis:** Run NMF topic modeling to categorize research.
4.  **Embedding:** Transform text into 384-dimensional semantic vectors.
5.  **Scoring:** Compute **Research Scores** by combining novelty and impact metrics.
6.  **Insight Generation:** Use LLM agents to summarize "Frontier Papers".

---
*This pipeline transforms unstructured XML feeds into an enriched, actionable dataset (`arxiv_research_agent.csv`) for rapid literature review and trend forecasting.*
