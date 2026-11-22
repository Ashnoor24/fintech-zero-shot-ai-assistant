# Task 1: EMI Explanation and Verification

## 1. Baseline Prompt
Explain EMI to a first-year BBA FinTech student in 50 words.

## 2. Improved Prompt (Version 1)
Act as a loan officer at a fictional FinTech lender.
A customer takes a personal loan of ₹2,50,000 at 14% annual interest for 24 months.

Provide:
1. The standard EMI formula with each variable defined.
2. Monthly EMI.
3. Total repayment amount.
4. Total interest payable.

Present the numerical results in a two-column table: Metric | Amount (₹). Round currency values to the nearest rupee.

## 3. Revised Prompt (Version 2 — Precision Control)
Act as a loan officer at a fictional FinTech lender.
A customer takes a personal loan of ₹2,50,000 at 14% annual interest for 24 months.

Calculate and present:
1. The EMI formula with each variable defined.
2. Monthly EMI.
3. Total repayment amount.
4. Total interest payable.

Rules:
- Use the exact monthly interest rate r = 0.14 / 12 without intermediate rounding.
- Round only the final rupee amounts to the nearest whole number.
- Return the results in a table with columns: Metric | Amount (₹).
