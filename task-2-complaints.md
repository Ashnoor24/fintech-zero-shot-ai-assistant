# Task 2 Prompts: Customer Complaint Classification (Gemini AI)

## 1. Initial Zero-Shot Prompt (v1)
```text
Act as a FinTech customer complaint classification assistant.
Classify each of the following 8 fictional customer complaints into exactly one category:
- Payments: UPI, transfers, failed payments, refunds, or transaction issues.
- Loans: EMI, loan repayment, interest, or loan-related deductions.
- KYC/Account: Identity verification, account access, or account updates.
- Needs review: Insufficient information to determine the correct category.

Customer Complaints:
1. UPI payment failed, but the amount was debited.
2. My EMI was deducted twice this month.
3. My PAN verification is still pending.
4. I transferred ₹5,000, but the recipient hasn't received it.
5. My loan interest rate increased unexpectedly.
6. My account is blocked after updating my KYC.
7. Money has disappeared from my account.
8. My application was rejected without explanation.

Assign exactly one category per complaint. Do not invent missing information. Mark ambiguous complaints as Needs review. Provide a short reason and one recommended action. Return a table: Complaint | Category | Reason | Recommended Action. Do not provide classification examples.
```

## 2. Revised Zero-Shot Prompt (v2 — Fixes Ambiguous Complaints #7 & #8)
Added explicit constraint:
```text
Strict rule: If a complaint does not explicitly mention a specific product or channel (such as UPI, transfer, EMI, loan, PAN, or KYC), you MUST classify it as Needs review. Never guess or assume the product type.
```
