# QueryFy: Virtual Assistant to explore the worlds largest companies

*QueryFy* is an AI-powered data assistant that transforms natural language questions into SQL queries over the *Forbes Global 2000 (2024)* dataset. Built for analysts, journalists, and anyone who wants to explore the dataset but doesn’t want to or know how to write SQL queries.

---

## Features?

- Ask questions like:  
  “Show top 5 companies by market value in Japan”  
  “Which financial firms have over 200,000 employees?”
- Let powerful LLMs generate accurate SQL queries on the fly
- See real-time results directly from a live SQLite database
- Ask factual questions (e.g. “Who is the CEO of Ericsson?”) with DuckDuckGo integration
- Choose between models like *Mistral-7B* and *Gemma-27B*
- Stay safe with built-in prompt injection detection

---

## Sample Questions to Try

- List the top 5 most profitable companies in the Oil & Gas industry.
- Which companies are based in Tokyo and have over 100,000 employees?
- Who is the CEO of Apple?
- Show average sales for companies founded before 1800.
- Search the web for what Ericsson does.

---

## Tools

| Layer | Tech |
|-------|------|
| LLM | LangChain + Together AI |
| UI | Gradio |
| DB | SQLite (with Forbes CSV loaded) |
| External Search | DuckDuckGo Search API |
| Dev Tools | Python, Pandas, re, sqlite3 |

---

## Dataset

QueryFy comes pre-loaded with the *Forbes Global 2000 – 2024* dataset:
- Fields: Name, Rank, Sales, Profit, Assets, Market Value, Industry, Headquarters, CEO, etc.
- All financials are scaled up to raw values (e.g. billions to actual amounts)

---

## How to Run

### Prerequisites:
- Google colab
- A Together AI API Key (Free: https://www.together.ai/playground)

### Steps
- Download the "queryfy.ipynb" from this repository and upload on your Google colab.
- Download "Largest-Companies.csv" from this repository and upload the data to your google drive
- Update the path to the dataset in this line "csv_file = \"/content/drive/MyDrive/Largest-Companies.csv\"\n"
- Update your Together AI API Key in this line " together_api_key = 'Enter_your_key_here'"
- Click runtime -> run all
### GUI Interaction
<img width="960" alt="image" src="https://github.com/user-attachments/assets/4556514f-9ddb-417a-81ca-e47cddbed45c" />
- Use the radio buttons to chose the LLM of choice : Mistral or Gemma 
- To display cached Queries click the "Cached Questions" drop down and select query of choice
- To run a custom query keep the "Cached Questions" drop down to "--Select--" and type your query in the "type your own question" chatbox
- Click Submit and view the output query and result in the "Assistant Response" section. 
