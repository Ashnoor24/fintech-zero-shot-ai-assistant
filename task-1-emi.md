# Task 1: EMI Explanation and Verification — Prompts

## 1. Baseline Prompt
Explain EMI to a first-year BBA FinTech student in 50 words.

## 2. Initial Improved Prompt
Act as a loan officer at a fictional FinTech lender.
A customer takes a personal loan of ₹2,50,000 at 14% annual interest for 24 months.
Provide:
1. The EMI formula with each variable explained.
2. Monthly EMI.
3. Total repayment amount.
4. Total interest paid.
Present the numerical results in a table.

## 3. Final Revised Prompt (Precision Fix)
Act as a loan officer at a fictional FinTech lender.
A customer takes a personal loan of ₹2,50,000 at 14% annual interest for 24 months.
Provide:
1. The EMI formula: EMI = P × r × (1 + r)^n / [(1 + r)^n − 1], with each variable defined.
2. Monthly EMI.
3. Total repayment amount.
4. Total interest paid.

Rules:
- Use the exact monthly interest rate r = 0.14 / 12 without intermediate rounding.
- Round only the final rupee amounts to the nearest rupee.
- Return the numbers in a Markdown table with two columns: Metric and Amount (₹).
