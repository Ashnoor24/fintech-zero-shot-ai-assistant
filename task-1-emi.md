## 1. Baseline Prompt
```text
Explain EMI to a first-year BBA FinTech student in 50 words.
```

## 2. Improved Prompt (v1)
```text
Act as a loan officer at a fictional FinTech lender.
A customer takes a personal loan of ₹2,50,000 at 14% annual interest for 24 months.
Show the EMI formula, monthly EMI, total repayment, and total interest in a table.
```

## 3. Revised Prompt (v2 — Fixes Rounding Error)
```text
Act as a loan officer at a fictional FinTech lender.
A customer takes a personal loan of ₹2,50,000 at 14% annual interest for 24 months.
Use exact monthly interest rate r = 0.14 / 12 without intermediate rounding, and round only the final rupee figures to the nearest whole rupee.
Show:
1. The EMI formula with each variable explained.
2. A table with columns: Item | Amount (₹) covering Monthly EMI, Total Repayment, and Total Interest.
```
