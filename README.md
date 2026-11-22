# FinTech Zero-Shot AI Assistant

### Applied Generative AI | Prompt Engineering | FinTech

**Institution:** Chitkara University  
**Program:** BBA FinTech  
**Lab:** 1 — Zero-Shot Prompting  
**Student:** Ashnoor Kaur  
**Student ID:** 2620992549  
**Academic Session:** 2026–2027  
**AI Tool/Model:** Gemini AI  
**Status:** Educational Prototype  

---

## 1. Executive Summary

This project demonstrates the application of zero-shot prompt engineering to four realistic FinTech business workflows using **Gemini AI**:

1. EMI explanation and financial calculation verification.
2. Customer complaint classification and triage.
3. Evidence-based financial data summarization.
4. Multilingual customer communication and professional email drafting.

The project uses no-code Generative AI tools, manual spreadsheet verification, and documented evaluation procedures.

**Project Goal:** Explore how structured zero-shot prompts improve clarity, reliability, and responsible AI compliance in financial services without providing worked examples.

## 2. Business Problem

FinTech organizations handle high volumes of customer queries, payment complaints, operational summaries, and bank communications. Generative AI can accelerate these tasks, but rounding errors, guessed complaint categories, unsupported revenue claims, and invented refund timelines create financial and compliance risks.

## 3. Project Objectives

- Develop precise zero-shot prompts for four FinTech operations workflows.
- Verify AI-generated financial calculations independently in Google Sheets.
- Classify fictional customer complaints without inventing missing context.
- Identify hallucinations and unsupported conclusions in financial summaries.
- Evaluate Hindi translation accuracy via back-translation into English.
- Document reproducible experiments and follow responsible AI principles.

## 4. Methodology

For each experiment:
1. Identify the business problem.
2. Create an initial zero-shot prompt.
3. Execute the prompt in Gemini AI.
4. Record the original AI response.
5. Independently verify the response (spreadsheet / answer key / back-translation).
6. Improve the prompt with explicit constraints.
7. Execute the revised prompt and compare results.
8. Document observations, errors caught, and limitations.

## 5. Lab Experiments

### Task 1: EMI Explanation and Verification

**Business Application:** Customer financial education and loan information.

**Baseline Prompt:**
> Explain EMI to a first-year BBA FinTech student in 50 words.

**Improved Prompt (Revised):**
> Act as a loan officer at a fictional FinTech lender. A customer takes a personal loan of ₹2,50,000 at 14% annual interest for 24 months. Use exact monthly rate `r = 0.14 / 12` without intermediate rounding, and round only the final rupee amounts. Show the EMI formula, monthly EMI, total repayment, and total interest in a table with columns: Item | Amount (₹).

**Independent Verification:**
- Formula: `EMI = P × r × (1 + r)^n / [(1 + r)^n − 1]`
- Where `P = ₹2,50,000`, `r = 0.14 / 12 = 0.01166667`, `n = 24 months`
- Spreadsheet formula: `=250000*(14%/12)*(1+14%/12)^24/((1+14%/12)^24-1)`

**Record Results:**

| Metric | Gemini AI Initial Run | Gemini AI Revised Run | Spreadsheet Result | Difference (After Revision) |
|---|---|---|---|---|
| Monthly EMI | ₹12,008 | ₹12,003 | ₹12,003 | ₹0 |
| Total Repayment | ₹2,88,192 | ₹2,88,077 | ₹2,88,077 | ₹0 |
| Total Interest | ₹38,192 | ₹38,077 | ₹38,077 | ₹0 |

**Conclusion:** In the initial run, Gemini AI rounded `r` to `1.17%`, causing a ₹5/month (₹115 total) overestimate. Adding the no-intermediate-rounding rule in the revised prompt produced an exact match with Google Sheets.

### Task 2: Customer Complaint Classification

**Business Application:** Customer support ticket categorization.

**Objective:** Classify eight fictional customer complaints into `Payments`, `Loans`, `KYC/Account`, or `Needs review`.

**Revised Zero-Shot Prompt:**
> Act as a FinTech customer complaint classification assistant. Classify each of the 8 fictional customer complaints into exactly one category: Payments (UPI, transfers, failed payments, refunds), Loans (EMI, loan repayment, interest), KYC/Account (identity verification, account access/updates), or Needs review (insufficient information). Rule: If a complaint does not name a specific product or cause (such as UPI, EMI, loan, or KYC), you MUST choose Needs review—never guess. Return a table with columns: Complaint | Category | Reason | Recommended Action. Do not provide classification examples.

**Final Output Table (Revised Run — 8/8 Correct):**

| Complaint | Category | Reason | Recommended Action |
|---|---|---|---|
| UPI payment failed, but the amount was debited. | Payments | Failed UPI transaction with account debit. | Verify UPI settlement status and initiate auto-reversal check. |
| My EMI was deducted twice this month. | Loans | Duplicate loan EMI deduction. | Audit loan repayment ledger and refund duplicate debit. |
| My PAN verification is still pending. | KYC/Account | Identity verification (PAN) delayed. | Check KYC verification queue and update customer. |
| I transferred ₹5,000, but the recipient hasn't received it. | Payments | Outgoing fund transfer not credited. | Trace UTR reference number with partner bank. |
| My loan interest rate increased unexpectedly. | Loans | Query regarding change in loan interest rate. | Review loan sanction terms and share rate-reset notice. |
| My account is blocked after updating my KYC. | KYC/Account | Account access restricted post-KYC update. | Escalate to KYC compliance team for account unblock review. |
| Money has disappeared from my account. | Needs review | Missing transaction details; could be fraud, UPI, or EMI. | Request transaction date, amount, and mode from customer. |
| My application was rejected without explanation. | Needs review | Unclear whether application is for a loan, card, or account. | Ask customer for application ID and product type. |

**Manual Review:** In the initial run, Gemini AI scored 6/8 by guessing "Payments" for Complaint 7 and "Loans" for Complaint 8. Adding the explicit rule forbidding guesses when no product is named raised accuracy to 8/8.

### Task 3: Evidence-Based Summarization

**Business Application:** Financial operations reporting (Fictional Company: PaySetu).

**Independent Calculations:**
- September total transaction value: `4,20,000 × ₹640 = ₹26.88 crore`
- October total transaction value: `5,10,000 × ₹590 = ₹30.09 crore`

**Evaluation:**

| Check | Observation |
|---|---|
| Accurate transaction figures | Pass — 4.2 lakh (Sep) and 5.1 lakh (Oct) reported accurately. |
| Accurate calculations | Pass — Total values match ₹26.88 crore and ₹30.09 crore. |
| Unsupported revenue claims | Caught in v1 (implied revenue grew); fixed to 0 in v2. |
| Unsupported profitability claims | Caught in v1; explicitly excluded in v2. |
| Correct identification of missing data | Pass — v2 listed revenue, costs, and root causes as unknown. |

**Conclusion:** Explicit negative constraints ("Do not infer causes, revenue, or profit; list what cannot be concluded") eliminated unsupported assumptions completely.

### Task 4: Translation and Business Communication

**Part A: Hindi Translation & Back-Translation**
- Initial run invented a "5–7 working days" refund promise not present in the original PaySetu notice.
- Revised run preserved exact meaning, kept `PaySetu` and `₹2,500` unchanged, and added zero timelines. Back-translation into English matched the source sentence-for-sentence.

**Part B: Professional Email (Partner Bank Delayed Settlement)**
- Drafted a 98-word formal operations email using placeholders `[Transaction_ID]`, `[Amount]`, `[Settlement_Date]`, and `[Account_Reference]`.

**Evaluation:**

| Criterion | Observation |
|---|---|
| Translation accuracy | High — exact match confirmed via English back-translation. |
| Meaning preserved | Pass — all technical error details preserved cleanly. |
| Professional tone | Pass — formal, concise B2B banking tone. |
| Word-count compliance | Pass — 98 words (within 100-word limit). |
| No invented commitments | Pass after revision — 0 invented refund dates or IDs. |

## 6. Evaluation Framework

| Criterion | Description | Result |
|---|---|---|
| Accuracy | Correct facts and calculations | Pass (100% verified after v2 revisions) |
| Clarity | Understandable language | Pass — clear for students, customers, and bank ops |
| Instruction Following | Compliance with requirements | Pass — all constraints met after explicit negative rules |
| Output Structure | Correct format | Pass — exact requested Markdown tables and word limits |
| Responsible AI | Avoids unsupported claims | Pass — synthetic data only; 0 fabricated promises in v2 |

## 7. Repository Structure

```text
fintech-zero-shot-ai-assistant/
├── README.md
├── prompts/
│   ├── task-1-emi.md
│   ├── task-2-complaints.md
│   ├── task-3-summary.md
│   └── task-4-communication.md
├── results/
│   └── experiment-results.md
├── evaluation/
│   └── evaluation-log.md
├── screenshots/
│   └── README.md
└── reflection.md
```

## 8. Tools and Technologies

- Generative AI / Large Language Models (Gemini AI)
- Zero-Shot Prompt Engineering
- Google Sheets (Independent EMI and transaction value verification)
- GitHub & Markdown documentation

## 9. Responsible AI and Risk Management

1. Fictional customer and company data only (PaySetu).
2. Zero real PAN, Aadhaar, bank account, or UPI credentials used.
3. Independent spreadsheet verification of all financial figures.
4. Explicit identification and removal of unsupported AI claims.
5. Mandatory human review escalation (`Needs review`) for ambiguous complaints.
6. Zero fabricated refund timelines or banking commitments.
7. Original and revised outputs both documented honestly.
8. Gemini AI assistance acknowledged transparently.

## 10. Limitations

- Academic prototype using synthetic data only.
- No live banking API or production deployment.
- Outputs from LLMs can vary slightly across runs; human oversight remains mandatory.

## 11. Future Scope

- Few-shot prompting experiments (Lab 2).
- Chain-of-thought financial modeling (Lab 3).
- System prompt guardrails for banking assistants (Lab 4).

## 12. Reflection

**100-word reflection:**  
The prompt change that made the biggest difference across all four tasks was replacing vague instructions like "be accurate" or "do not invent" with explicit, itemized prohibitions. In my initial Gemini AI runs, the model rounded the monthly interest rate (shifting EMI by ₹5), guessed categories for ambiguous complaints, implied revenue growth without data, and added a 5–7 day refund timeline to the Hindi notice. Once I specified exact rules—no intermediate rounding, mandatory "Needs review" when no product is named, and no invented dates—errors dropped to zero. I learned that AI outputs are drafts requiring independent spreadsheet and logic checks.

## 13. Author

**Student Name:** Ashnoor Kaur  
**Student ID:** 2620992549  
**Program:** BBA FinTech  
**University:** Chitkara University  

## 14. Academic Integrity

This repository documents educational AI experiments completed by Ashnoor Kaur (2620992549) using Gemini AI. All calculations and evaluations were independently verified in accordance with Chitkara University guidelines.
