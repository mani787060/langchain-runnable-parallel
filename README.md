# LangChain RunnableParallel Mastery
[![LangChain](https://img.shields.io/badge/Framework-LangChain-green)](https://www.langchain.com/)
[![Python](https://img.shields.io/badge/Python-3.9%2B-blue)](https://www.python.org/)
[![Concurrency](https://img.shields.io/badge/Concept-Concurrency-red)](https://python.langchain.com/docs/concepts/#runnableparallel)

## 🏗️ Project Overview
This repository deep-dives into **`RunnableParallel`**, the primary primitive for creating non-linear pipelines in LangChain. In high-performance AI applications, efficiency is key. This project showcases how to branch an input into multiple "expert" chains that run at the same time, significantly reducing the total execution time and allowing for multi-perspective analysis of a single query.

---

## 🛠️ Key Technical Implementations

### 1. The Branch-and-Merge Pattern
* **Concurrent Execution:** Using `RunnableParallel` to trigger multiple LLM calls or tool lookups simultaneously.
* **Input Distribution:** Mapping a single dictionary input to multiple sub-chains without manual data duplication.

### 2. State Aggregation
* **Unified Output:** Collecting results from different branches into a single dictionary, making it easy for a final "Reviewer" model to synthesize the findings.
* **Type Management:** Ensuring that parallel branches return compatible data structures for downstream consumption.

### 3. Performance Optimization
* **Latency Reduction:** Proving how parallel chains scale better than sequential chains by cutting total processing time down to the duration of the slowest branch.
* **Batch Processing:** Combining `RunnableParallel` with `.batch()` for massive throughput.

---

## 💻 Tech Stack
* **Language:** Python 3.9+
* **Orchestration:** LangChain (`langchain-core`, `langchain-google-genai`)
* **Model:** Google Gemini Pro
* **Environment:** `python-dotenv`

---

## 🚀 Getting Started

1. **Clone the repository:**
   ```bash
   git clone [https://github.com/your-username/langchain-runnable-parallel-concurrency.git](https://github.com/your-username/langchain-runnable-parallel-concurrency.git)

2. **Install Dependencies:**
   ```bash
   pip install -U langchain-core langchain-google-genai python-dotenv

3. **Setup API Key:**
   Create a .env file in the root directory:
   ```bash
   GOOGLE_API_KEY=your_gemini_key_here

4.Run the Implementation:
  ```bash
  python runnable_parallel.py
