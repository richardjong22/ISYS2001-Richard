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

### 3. Decisions & Adaptations
- **What I Kept**: 
  I adopted the "Student Budget & Savings Goal Helper" idea as it addresses a realistic financial problem for university students. I kept the hand-calculated example and logic for calculating required monthly savings versus current net savings.
- **What I Changed / Refined**: 
  I refined the required inputs to explicitly require columns `Date`, `Description`, `Category`, and `Amount` in the CSV to match standard transaction dataset formats.

### 4. Rejections & Reasoning
- **Rejected Suggestion**: 
  The AI initially suggested using an external database (SQLite) to store student profiles over time.
- **Reason for Rejection**: 
  I rejected this because unit requirements specify using Pandas for CSV loading and processing. Introducing SQL would add unnecessary complexity and deviate from the unit's core stack.

---
