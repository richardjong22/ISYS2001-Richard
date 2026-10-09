# Developer's Diary

---

## Week 1: Project Scope, Six-Step Method, and Repository Setup
**Date**: September 23, 2026

### 1. Goal
Define the project problem statement, establish the target audience (university students), write the Six-Step Method documentation, and set up the GitHub repository structure.

### 2. AI Collaboration & Prompts
- **Prompt Used**: 
  > *"I need to design a student budget and savings goal assistant using Python, Pandas, Gemini API, and Gradio for ISYS2001 Assessment 2. Help me draft the Six-Step Method including problem definition, inputs/outputs, hand example, and pseudocode."*
- **AI Response Summary**: 
  The AI suggested a problem statement focused on students trying to reach a savings target (e.g., $600 in 3 months) by analyzing transaction CSV files and calculating monthly budget gaps.

### 3. What I did with it
- **What I Kept**: 
  I adopted the "Student Budget & Savings Goal Helper" idea as it addresses a realistic financial problem for university students. I kept the hand-calculated example and logic for calculating required monthly savings versus current net savings.
- **What I Changed**: 
  I refined the required inputs to explicitly require columns `Date`, `Description`, `Category`, and `Amount` in the CSV to match standard transaction dataset formats.

### 4. Rejections & Reasoning
- **Rejected Suggestion**: 
  The AI initially suggested using an external database (SQLite) to store student profiles over time.
- **Reason for Rejection**: 
  I rejected this because unit requirements specify using Pandas for CSV loading and processing. Introducing SQL would add unnecessary complexity and deviate from the unit's core stack.

---

## Week 2: Core Algorithm, CSV Processing, and Financial Logic
**Date**: October 1, 2026

### 1. Goal
Implement the core financial logic for the Student Budget Assistant in Python, including CSV data loading with Pandas, transaction filtering (income vs. expense), monthly savings calculations, target goal verification, and input error handling.

### 2. AI Collaboration & Prompts
- **Prompt Used**: 
  > *"Help me write a Python function that reads a transaction CSV with columns 'Date', 'Description', 'Category', and 'Amount', calculates total income and expenses, and determines if a student is on track to reach a target savings goal over a set number of months."*
- **AI Response Summary**: 
  The AI provided a Pandas-based function structure that validates input parameters, checks for required CSV headers, uses conditional filtering (`Amount > 0` for income, `Amount < 0` for expenses), counts required monthly savings (`target_amount / target_months`), and outputs a structured financial status string ("ON TRACK" vs "SHORTFALL DETECTED").

### 3. What I did with it
- **What I Kept**: 
  I implemented the `monthly_gap` calculation logic (`current_monthly_savings - required_monthly_savings`) to clearly evaluate whether a student meets their goal or falls short. I also kept the explicit validation check for non-zero and non-negative target amounts/months.
- **What I Changed**: 
  I changed the expense calculation to explicitly use absolute values (`ABSOLUTE SUM of Amount WHERE Amount < 0`) so that net savings (`total_income - total_expenses`) evaluates correctly regardless of whether expense numbers in the CSV are logged as negative integers.

### 4. Rejections & Reasoning
- **Rejected Suggestion**: 
  The AI suggested using complex regex pattern matching to auto-categorize missing transaction categories.
- **Reason for Rejection**: 
  I rejected this approach to keep the function predictable. Ensuring strict verification of required CSV headers before processing is cleaner and prevents unexpected runtime errors for invalid files.

---

## Week 3: Gemini API Integration, Unit Testing, and UI Finalization
**Date**: October 9, 2026

### 1. Goal
Finalize the Student Budget Assistant application by integrating Google's Gemini API (`gemini-flash-latest`) for personalized financial coaching, securing API credentials via Google Colab Secrets, updating unit tests for dual-output data structures, and completing final project documentation.

### 2. AI Collaboration & Prompts
- **Prompt Used**: 
  > *"Help me connect my Pandas financial summary function directly to the Gemini API while keeping the API key secure in Colab Secrets, updating my unit tests, and displaying both outputs cleanly in Gradio."*
- **AI Response Summary**: 
  The AI provided an updated modular structure where `calculate_savings_plan` returns both formatted text and a `financial_context` dictionary. It also provided a helper function `get_ai_financial_advice` using `google.colab.userdata` to securely retrieve `GOOGLE_API_KEY` and updated the Gradio interface to display dual text outputs.

### 3. What I did with it
- **What I Kept**: 
  I kept standard 2-decimal place currency formatting (`:,.2f`) across financial summaries to maintain consistency with financial accounting standards. I also kept the modular dual-output approach to cleanly separate data analysis from AI coaching.
- **What I Changed**: 
  I adapted the unit test function `test_calculate_savings_plan()` to unpack the returned tuple `(summary, context)` and added explicit assertions to verify both string outputs and dictionary values (`context['total_income']`). Additionally, I added dependency installation (`!pip install -q google-generativeai`) at the top of the notebook.

### 4. Rejections & Reasoning
- **Rejected Suggestion**: 
  The AI suggested hardcoding the Gemini API key directly into the Python code string for quick testing.
- **Reason for Rejection**: 
  I rejected hardcoding API keys because it creates severe security risks and violates Requirement 1 guidelines. Using Colab Secrets (`userdata.get('GOOGLE_API_KEY')`) ensures credentials remain hidden before pushing code to GitHub.

---
