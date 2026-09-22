# Student Budget & Savings Goal Helper 🎓💰

An AI-powered personal finance assistant designed specifically for university students. It analyzes transaction data from CSV files, calculates savings goal feasibility, and uses Google's Gemini API to deliver financial advice in a friendly tone.

**ISYS2001: Introduction to Business Programming**

---

## 🌟 Key Features
- **Transaction Analyzer**: Calculates total income, expenses, and net savings from student transaction history.
- **Savings Goal Calculator**: Calculates required monthly savings based on a target amount and timeframe, detecting budget shortfalls.
- **AI Financial Coach**: Powered by Google Gemini API (`gemini-flash-latest`) to provide personalized, educational budget recommendations based on actual spending habits.
- **Interactive Interface**: Built with Gradio for an intuitive, web-based user experience.

---

## 📊 Sample Input & Output

### Input Example
- **Uploaded File**: `transactions.csv` (Contains columns: `Date`, `Description`, `Category`, `Amount`)
- **Target Savings Goal**: `$600.00`
- **Target Timeframe**: `3 months`
- **User Question**: *"Where can I cut down my expenses to meet my goal?"*

### Output Example
- **Financial Summary**:
  - Total Income: `$1,500.00`
  - Total Expenses: `$1,100.00`
  - Current Monthly Net Savings: `$400.00`
  - Required Monthly Savings: `$200.00`
  - Status: **On Track!** You exceed your required monthly savings by `$200.00`.
- **AI Response**:
  > *"Great job! Your current savings rate easily covers your $600 goal in 3 months. To stay safe, try maintaining your current spending on Dining out ($120/month) and keep building your emergency fund."*

---

## 🚀 How to Run the Project

1. **Download Repository**:
   Download this repository or open the notebook in Google Colab.

2. **Set Up API Key**:
   - Obtain a free API key from [Google AI Studio](https://aistudio.google.com/).
   - In Google Colab, open the **Secrets** panel (key icon in the left sidebar).
   - Add a new secret named `GOOGLE_API_KEY` and paste your key as the value.
   - Toggle **Notebook access** ON.

3. **Run the Notebook**:
   - Execute all cells in `student_budget_assistant.ipynb`.
   - Launch the Gradio web interface via the generated link.

---

## 📁 Repository Structure
- `student_budget_assistant.ipynb`: Main Google Colab notebook containing code, six-step evidence, and assert tests.
- `README.md`: Project documentation and quick-start guide.
- `Developer_Diary.md`: Weekly reflection and AI collaboration log.

---
