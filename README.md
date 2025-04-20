# 🚀 QueryFy: Chat with Your Data

> “Your voice. Your data. One question away.”  

*QueryFy* is an AI-powered data assistant that transforms natural language questions into SQL queries over the *Forbes Global 2000 (2024)* dataset. Built for analysts, students, founders, and anyone who doesn’t want to write SQL but still wants SQL-level answers.

---

## 🧠 What Can It Do?

With QueryFy, you can:

- 🔎 Ask questions like:  
  “Show top 5 companies by market cap in Japan”  
  “Which financial firms have over 200,000 employees?”
  
- 🤖 Let powerful LLMs generate accurate SQL queries on the fly
- 💻 See real-time results directly from a live SQLite database
- 🌐 Ask factual questions (e.g. “Who is the CEO of Ericsson?”) with DuckDuckGo integration
- 🔄 Choose between models like *Mistral-7B* and *Gemma-27B*
- 🔒 Stay safe with built-in prompt injection detection

---

## 📦 Tech Stack

| Layer | Tech |
|-------|------|
| LLM Engine | LangChain + Together AI |
| UI | Gradio |
| DB | SQLite (with Forbes CSV loaded) |
| External Search | DuckDuckGo Search API |
| Dev Tools | Python, Pandas, re, sqlite3 |

---

## 📊 Dataset

QueryFy comes pre-loaded with the *Forbes Global 2000 – 2024* dataset:
- Fields: Name, Rank, Sales, Profit, Assets, Market Value, Industry, Headquarters, CEO, etc.
- All financials are scaled up to raw values (e.g. billions to actual amounts)

---

## 🛠 How to Run

### 🔗 Prerequisites:
- Python 3.8+
- A Together AI API Key (Free: https://www.together.ai/playground)

### ⚙ Installation

```bash
git clone https://github.com/your-username/queryfy.git
cd queryfy

pip install -r requirements.txt
# or install manually:
pip install langchain langchain-together gradio duckduckgo-search pandas sqlite3
