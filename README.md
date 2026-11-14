# FinTrack: Personal Finance Manager

**Project Overview:**  
FinTrack is a simple personal finance management tool implemented in Python. It records income and expenses in a SQLite database, allows setting monthly budgets by category, and generates summary reports and visualizations. In the demo notebook/script, we simulate 4 months of data and show total income, expenses, net balance, savings rate, and expense breakdown by category. We also output a **Budget Status** table for the current month, highlighting spent vs. budgeted amounts.

**Tools & Technologies:**  
- **Python** (classes, `sqlite3`, `dataclasses`, custom exception handling)  
- **SQLite** (embedded SQL database for persistence)  
- **Pandas** (data aggregation and summary)  
- **Matplotlib** (pie chart and bar chart visualizations)  
- **Logging & Decorators** for debugging and input validation  
- Automated **unit tests** to validate core functionality

**Key Results (from demo output):**  
- **Total transactions:** *e.g.* 68 (for 4 months, including salary + expenses)  
- **Total Income:** \$16,000 (4 months × \$4,000 monthly)  
- **Total Expense:** (sum of all random expenses)  
- **Net Balance:** (income – expense)  
- **Savings Rate:** (net balance as % of income)  
- **Expense by Category:** breakdown like `{ 'food': 1200.00, 'rent': 4800.00, 'transport': 500.00, ... }` sorted by amount.  
- **Budget Status (current month):** a table with columns `category | limit | spent | remaining | used_pct | over_budget`. For example:

  | category      | limit | spent | remaining | used_pct | over_budget |
  |--------------|------:|------:|---------:|--------:|-----------:|
  | **Food**       | 400.0 | 150.0 | 250.0    | 37.5%   | False      |
  | **Entertainment** | 150.0 | 200.0 | -50.0    | 133.3%  | True       |
  | **Shopping**   | 200.0 |  80.0 | 120.0    | 40.0%   | False      |

  (Numbers above are illustrative; actual values come from the random demo.)

**How to Run:**  
1. Open `fintrack_analyzer.ipynb` in **Google Colab** or **Jupyter Notebook**.
2. Install dependencies if running locally: `pip install pandas matplotlib`
3. Run all cells from top to bottom to initialize the SQLite database, seed sample data, view budget reports, and execute the unit test suite.
