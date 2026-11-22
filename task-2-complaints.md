# Task 2: Customer Complaint Classification — Prompts

## 1. Initial Prompt (Single Complaint)
Act as a FinTech complaint classification assistant.
Classify the following customer complaint into exactly one category: Payments, Loans, or KYC/Account. If the category is unclear, label it Needs review.

Customer complaint: "EMI deducted twice."

Return a table with Complaint, Category, Reason, and Recommended Action. Do not provide any classification examples.

## 2. Full Batch Zero-Shot Prompt (8 Complaints)
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

Instructions:
1. Assign exactly one category per complaint.
2. Do not invent missing information.
3. Mark ambiguous complaints as Needs review.
4. Provide a short reason for each classification.
5. Suggest one recommended action.

Return a table with four columns: Complaint, Category, Reason, and Recommended Action.
Do not provide classification examples before processing the complaints.

## 3. Revised Prompt (Anti-Guessing Constraint Added)
[Same as Batch Prompt above, with Instruction #3 strengthened to:]
3. If a complaint does not explicitly mention a specific product or process (such as UPI, transfer, EMI, loan, PAN, or KYC), you MUST label it Needs review. Never assume or guess the product type.
