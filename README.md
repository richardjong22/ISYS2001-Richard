# Student Budget & Savings Goal Helper 🎓💰

A personal finance assistant designed specifically for university students. It processes transaction data from CSV files using Python and Pandas to evaluate budget feasibility and leverages Google's Gemini API to deliver personalized financial coaching.

**ISYS2001: Introduction to Business Programming**

---

## 🌟 Key Features
- **Transaction Analyzer**: Calculates total income, expenses, and net savings from student transaction history using Pandas.
- **Savings Goal Calculator**: Calculates required monthly savings based on a target amount and timeframe, detecting budget shortfalls or surpluses.
- **AI Financial Coach**: Powered by Google's Gemini API (`gemini-flash-latest`) to provide personalized, educational budget recommendations grounded in the student's actual spending data.
- **Interactive Interface**: Built with Gradio for an intuitive, web-based user experience.

---

## 📊 Sample Input & Output

### Input Example
- **Uploaded File**: `transactions.csv` (Contains columns: `Date`, `Description`, `Category`, `Amount`)
- **Target Savings Goal**: `$600.00`
- **Target Timeframe**: `3 months`
- **Optional Question**: *"Where can I cut down my expenses to meet my goal?"*

### Output Example
- **Financial Analysis Summary (Pandas)**:
  - Total Income: `$1,500.00`
  - Total Expenses: `$1,100.00`
  - Current Monthly Net Savings: `$400.00`
  - Target Goal: `$600.00` in `3 month(s)`
  - Required Monthly Savings: `$200.00/month`
  - Goal Status: **✅ ON TRACK!** You exceed your required monthly target by `$200.00`.
- **AI Financial Coach Advice (Gemini API)**:
  > *"Great job! Your current savings rate easily covers your $600 goal in 3 months. To stay safe, maintain your current spending on Dining out ($120/month) and keep building your emergency fund."*

---

## 🚀 How to Run the Project

1. **Open in Google Colab or Local Environment**:
   Download this repository or open `student_budget_assistant.ipynb` directly in Google Colab.

2. **Set Up API Key**:
   - Obtain a free API key from [Google AI Studio](https://aistudio.google.com/).
   - In Google Colab, open the **Secrets** panel (key icon in the left sidebar).
   - Add a new secret named `GOOGLE_API_KEY` and paste your key as the value.
   - Toggle **Notebook access** ON.

3. **Run the Notebook**:
   - Execute all cells in `student_budget_assistant.ipynb`.
   - Launch the Gradio web interface via the generated link.

4. **Upload Test Data**:
   - Upload a sample transaction CSV file (e.g., `test_sample.csv`) and set a target goal to test both the Pandas calculation logic and the Gemini AI coaching output.

---

## 📁 Repository Structure
- `student_budget_assistant.ipynb`: Main Google Colab notebook containing code, six-step evidence, unit tests, and Gradio UI.
- `test_sample.csv`: Sample CSV dataset for testing transaction processing.
- `README.md`: Project documentation and quick-start guide.
- `DEVELOPERS_DIARY.md`: Weekly reflection and development log.
