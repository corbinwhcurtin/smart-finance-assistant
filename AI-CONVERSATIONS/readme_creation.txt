
USER:
What should go in the readme file?

CLAUDE:
Here is a clean README covering everything a marker would want to see:

---

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

- CSV Import — Upload any bank export with Date, Description, and Amount columns
- Auto-categorisation — Transactions automatically sorted into 10 spending categories
- Essential flagging — Rent, power, and phone bills tracked separately, never targeted for cuts
- Spending insights — Category breakdowns, invisible spending detection, subscription audit
- Financial health score — 0 to 100 score with honest assessment of your position
- Forward-looking budget — Set monthly limits per category based on your actual history
- Safety net tracker — Separate savings target for emergencies before holiday goals
- Savings goals — Track progress toward specific goals with projected completion dates
- Month-on-month comparison — Upload each month to see if you are improving
- AI recommendations — Personalised advice based on your real numbers
- Finn chatbot — Ask follow-up questions with full awareness of your spending data
- Persistent storage — Budget plan and monthly history saved automatically to JSON

---

## How to Run

1. Open the notebook in Google Colab
2. Go to Runtime → Run all
3. Wait for all cells to complete — the Gradio interface launches from Cell 10
4. Upload your bank CSV in Step 1 and follow the 6-step flow

---

## CSV Format

| Column      | Description                              | Example                      |
|-------------|------------------------------------------|------------------------------|
| Date        | Transaction date                         | 03/01/2025                   |
| Description | Merchant or transaction name             | Coles Supermarket Karrinyup  |
| Amount      | Positive for income, negative for expenses | -87.43                     |

---

## The 6-Step Flow

| Step       | Description                                                  |
|------------|--------------------------------------------------------------|
| 1. Import  | Upload your bank CSV                                         |
| 2. Edit    | Review categories, flag essentials, add cash transactions    |
| 3. Insights| See spending breakdown, health score, AI recommendations     |
| 4. Plan    | Set monthly budget limits, safety net target, savings goals  |
| 5. Budget  | View your plan, track goal progress, savings calculator      |
| 6. Chat    | Ask Finn anything about your finances                        |

On your second month upload, Step 4 is skipped and you go straight to a comparison of
your actual spend against your budget limits.

---

## Tech Stack

- Python — Core language
- Pandas — Data processing and analysis
- Plotly — Interactive charts and visualisations
- Gradio — Web interface
- hands-on-ai — AI chat, RAG retrieval, and agent tools
- gemma3:4b — Large language model via Ollama

---

## Project Structure

    smart-finance-assistant/
    ├── starter_notebook.ipynb       # Main notebook — all code and UI
    ├── finance_knowledge.txt        # RAG knowledge base (auto-generated on first run)
    ├── finance_data.json            # Saved budget and monthly history (auto-generated)
    ├── transactions_3months.csv     # Sample data Month 1 (Jan-Mar 2025)
    ├── transactions_months4to6.csv  # Sample data Month 2 (Apr-Jun 2025, improved)
    └── README.md                    # This file

---

## Sample Data

Two sample CSV files are included for testing:
- transactions_3months.csv — January to March 2025, tight budget (~$44/week leftover)
- transactions_months4to6.csv — April to June 2025, improved spending (~$139/week leftover)

Upload Month 1 first, complete the full 6-step flow and save a budget plan, then upload
Month 2 to see the comparison and trend features in action.

---

## Built For

ISYS2001 — Business Information Systems
Curtin University, 2025
Smart Finance Assistant Project
