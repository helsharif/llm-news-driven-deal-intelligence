# LLM-Powered News-Driven Deal Intelligence  
**Multi-Agent AI System for Automated Deal Signal Detection**  
*CrewAI + Large Language Models*

> Autonomous AI agents that monitor news, detect deal signals, score relevance, and produce structured, actionable intelligence.

<img width="2000" height="1037" alt="image" src="https://github.com/user-attachments/assets/137f3d1d-60cf-4597-909e-1dc80246eb8c" />


---

## 📌 Overview

This project demonstrates a **lightweight, autonomous multi-agent AI system** that monitors external news sources and identifies **high-value business and deal signals** in near real time. Using coordinated LLM-powered agents, the system transforms unstructured news data into **structured, prioritized deal intelligence**, including relevance scoring, tagging, and concise executive summaries.

The system is implemented entirely in **Python**, leveraging **CrewAI** for agent orchestration and **OpenAI-compatible LLMs** for reasoning, classification, and summarization.

---

## 🎯 Project Motivation

Deal teams, corporate strategy groups, and investors face an overwhelming volume of unstructured information from:
- News articles
- Press releases
- Regulatory announcements
- Industry updates

Manually scanning these sources to identify **early indicators of M&A activity, funding events, partnerships, regulatory risk, or corporate distress** is time-consuming and inefficient.

**Goal:**  
Build a transparent, reproducible AI agent that automatically monitors news, applies LLM-based reasoning to detect deal signals, and produces **prioritized, human-readable outputs** that are immediately actionable.

This project is intentionally scoped as a **proof of concept**, focusing on:
- Clean architecture
- Deterministic execution
- Explainable AI outputs

---

## 🧠 System Architecture

The system uses a **three-agent CrewAI pipeline**, where each agent has a clear, isolated responsibility:

### 1️⃣ Research Agent — News Monitoring
- Ingests articles from RSS feeds or APIs
- Scans headlines and summaries
- Identifies articles likely to contain deal signals
- Outputs a shortlist for deeper analysis

---

### 2️⃣ Analyst Agent — Deal Signal Detection & Scoring
- Performs structured analysis on shortlisted articles
- Extracts:
  - Deal signal type (M&A, funding, partnership, regulatory, distress)
  - Relevance score (0.0–1.0)
  - Descriptive tags
  - Short rationale explaining why the signal matters
- Produces **machine-readable JSON** outputs

---

### 3️⃣ Writer Agent — Executive Summary
- Converts structured signals into a **concise daily summary**
- Outputs a CLI-style report suitable for:
  - Rapid prioritization
  - Follow-up workflows
  - Alerting pipelines
- Ensures traceability by including **exact source URLs**

---

## 🔁 High-Level Workflow

1. **Configuration Input**  
   User defines industries, signal types, and relevance thresholds.

2. **Data Ingestion**  
   System monitors 1–2 external news sources (RSS or API-based).

3. **CrewAI Orchestration**  
   Tasks execute sequentially with shared context.

4. **LLM-Based Reasoning**  
   Agents classify, score, and explain deal signals.

5. **Structured Output Generation**  
   Results are exported as clean JSON artifacts.

6. **Human-Readable Summary**  
   A daily CLI-style summary is generated automatically.

---

## 📦 Outputs

Each run produces the following artifacts:

- **Raw monitored items**  
  `raw_items_<run_date>.json`

- **Structured deal signals**  
  `signals_<run_date>.json`  
  (includes signal type, relevance score, tags, rationale, and source URL)

- **Daily summary report**  
  `summary_<run_date>.txt`

All outputs are designed to be:
- Transparent
- Auditable
- Easy to integrate into downstream systems

---

## 🧪 Example Output

Included example runs demonstrate detection of:
- M&A activity
- Funding announcements
- Strategic partnerships
- Regulatory actions
- Corporate distress events

Each signal includes a relevance score and a concise explanation, enabling rapid prioritization and follow-up.

---

## 🛠️ Technology Stack

- **Python**
- **CrewAI** (multi-agent orchestration)
- **OpenAI-compatible LLM APIs**
- **RSS / API-based data ingestion**
- **JSON-based storage (no database dependency)**

---

## 🚀 Why This Project Matters

This project showcases hands-on experience with:
- Applied LLM systems
- Multi-agent AI architectures
- External data ingestion
- Explainable AI design
- Production-oriented GenAI workflows

It is directly applicable to:
- Deal intelligence
- Market monitoring
- Competitive intelligence
- AI-powered decision support systems

---

## 📄 Notes

- Fully autonomous execution (no human prompts)
- Deterministic, reproducible runs
- Designed for extensibility, not over-engineering
- Easily extendable to:
  - Additional data sources
  - Slack or email alerting
  - Databases or APIs
  - Feedback-driven scoring refinement




