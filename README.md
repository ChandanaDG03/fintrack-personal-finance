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
- **Total transactions:** 65 (across 4 months, including salary + expenses)  
- **Total Income:** $16,000.00 (4 months × $4,000.00 monthly)  
- **Total Expense:** $3,818.66  
- **Net Balance:** $12,181.34  
- **Savings Rate:** 76.1%  
- **Expense by Category:** `{'rent': 1748.47, 'utilities': 516.86, 'transport': 455.44, 'shopping': 447.77, 'food': 378.89, 'entertainment': 271.23}`  
- **Budget Status (current month):**  

  | category          | limit | spent  | remaining | used_pct | over_budget |
  |-------------------|------:|-------:|----------:|---------:|------------:|
  | **Entertainment** | 150.0 |  55.16 |     94.84 |    36.8% |       False |
  | **Food**          | 400.0 |  85.39 |    314.61 |    21.3% |       False |
  | **Shopping**      | 200.0 | 153.97 |     46.03 |    77.0% |       False |


**How to Run:**  
1. Open `Personal_Finance_Tracker.ipynb` in **Google Colab** or **Jupyter Notebook**.
2. Install dependencies if running locally: `pip install pandas matplotlib`
3. Run all cells from top to bottom to initialize the SQLite database, seed sample data, view budget reports, and execute the unit test suite.
