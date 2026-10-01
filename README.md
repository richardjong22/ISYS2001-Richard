# Student Budget & Savings Goal Helper 🎓💰

A personal finance assistant designed specifically for university students. It processes transaction data from CSV files using Python and Pandas to evaluate budget gap feasibility and track savings targets.

**ISYS2001: Introduction to Business Programming**

---

## 🌟 Key Features
- **Transaction Analyzer**: Calculates total income, expenses, and net savings from student transaction history using Pandas.
- **Savings Goal Calculator**: Calculates required monthly savings based on a target amount and timeframe, detecting budget shortfalls or surpluses.
- **Interactive Interface**: Built with Gradio for an intuitive, web-based user experience.

---

## 📊 Sample Input & Output

### Input Example
- **Uploaded File**: `transactions.csv` (Contains columns: `Date`, `Description`, `Category`, `Amount`)
- **Target Savings Goal**: `$600.00`
- **Target Timeframe**: `3 months`

### Output Example
- **Financial Summary**:
  - Total Income: `$1,500.00`
  - Total Expenses: `$1,100.00`
  - Current Monthly Net Savings: `$400.00`
  - Required Monthly Savings: `$200.00`
  - Status: **On Track!** You exceed your required monthly savings by `$200.00`.

---

## 🚀 How to Run the Project

1. **Open in Google Colab or Local Environment**:
   Download this repository or open `student_budget_assistant.ipynb` directly in Google Colab.

2. **Run the Notebook**:
   - Execute all cells in `student_budget_assistant.ipynb`.
   - Launch the Gradio web interface via the generated link.

3. **Upload Test Data**:
   - Upload a sample transaction CSV file (e.g., `test_sample.csv`) to test the calculation logic.

---

## 📁 Repository Structure
- `student_budget_assistant.ipynb`: Main Google Colab notebook containing code, six-step evidence, unit tests, and Gradio UI.
- `test_sample.csv`: Sample CSV dataset for testing transaction processing.
- `README.md`: Project documentation and quick-start guide.
- `DEVELOPERS_DIARY.md`: Weekly reflection and development log.
