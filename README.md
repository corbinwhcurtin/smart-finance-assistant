# Smart Finance Assistant

A personal finance analysis and budgeting tool built for Australian university students. 
Upload your bank transaction data, understand your spending patterns, build a forward-looking 
budget, and track savings goals over time — with AI-powered advice from Finn, your no-nonsense 
financial coach.

---

## What It Does

Most budgeting tools show you what you spent but don't help you change anything. This assistant 
analyses your actual bank data, identifies where money is quietly disappearing, and helps you 
build a realistic budget based on what you actually spend — not what you wish you spent.

Built specifically for casual workers and university students who have high fixed costs like rent, 
irregular income, no sick leave, and real social lives worth budgeting for.

---

## Features

- **CSV Import** — Upload any bank export with Date, Description, and Amount columns
- **Auto-categorisation** — Transactions automatically sorted into 10 spending categories
- **Essential flagging** — Rent, power, and phone bills tracked separately and never targeted for cuts
- **Spending insights** — Category breakdowns, invisible spending detection, subscription audit, day-of-week patterns
- **Financial health score** — 0 to 100 score with honest assessment of your position
- **Forward-looking budget** — Set monthly limits per category based on your actual history
- **Safety net tracker** — Separate savings target for emergencies before holiday goals
- **Savings goals** — Track progress toward specific goals with projected completion dates
- **Month-on-month comparison** — Upload each month to see if you are improving
- **AI recommendations** — Personalised advice based on your real numbers
- **Finn chatbot** — Ask follow-up questions with full awareness of your spending data and budget
- **Persistent storage** — Budget plan and monthly history saved automatically to JSON

---

## How to Run

1. Open the notebook in Google Colab
2. Go to **Runtime → Run all**
3. Wait for all cells to complete — the Gradio interface will launch from Cell 10
4. Upload your bank CSV in Step 1 and follow the 6-step flow

---

## CSV Format

Your bank export needs at minimum these three columns:

| Column | Description | Example |
|--------|-------------|---------|
| Date | Transaction date | 03/01/2025 |
| Description | Merchant or transaction name | Coles Supermarket Karrinyup |
| Amount | Positive for income, negative for expenses | -87.43 |

A Category column will be used if present, otherwise categories are assigned automatically.

---

## Tech Stack

- **Python** — Core language
- **Pandas** — Data processing and analysis
- **Plotly** — Interactive charts and visualisations
- **Gradio** — Web interface
- **hands-on-ai** — AI chat, RAG retrieval, and agent tools
- **gemma3:4b** — Large language model via Ollama

---


## Sample Data

Two sample CSV files are included for testing:

- `transactions_3months.csv` — January to March 2025, tight budget (~$44/week leftover)
- `transactions_months4to6.csv` — April to June 2025, improved spending (~$139/week leftover)

Upload Month 1 first, complete the full 6-step flow and save a budget plan, then upload Month 2 
to see the comparison and trend features in action.

---

## Built For

ISYS2001 — Business Information Systems  
Curtin University, 2026 
Smart Finance Assistant Project
