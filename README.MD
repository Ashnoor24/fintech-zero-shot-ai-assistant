**PORTFOLIO CASE STUDY · ZERO-SHOT PROMPTING**
# Can a Plain Prompt Run PaySetu's Daily Operations Tasks?
### Testing AI on loan maths, complaint sorting, reporting and customer messages
**[Your Full Name]** · Student ID: **[Your ID]** · AI Operations Analyst (student project) · BBA (FinTech), Chitkara Business School · November 2026

---

### At a glance

| Monthly EMI (checked in Sheets) | Complaints sorted correctly | Invented facts after revision |
| :---: | :---: | :---: |
| **₹12,003** *(AI first gave ₹[Your AI EMI])* | **[First Score] → [Revised Score]** out of 8 | **[First Count] → [Revised Count]** across all four tasks |

### Project snapshot

| Field | Details |
| :--- | :--- |
| **Client (fictional)** | PaySetu, a payments start-up handling about 5 lakh transactions a month |
| **My role** | AI Operations Analyst: wrote the prompts, checked every answer, revised the prompts |
| **Question** | Can zero-shot prompts (instructions only, no examples) handle four daily operations tasks safely? |
| **Method** | 4 tasks · first prompt → my own check → revised prompt → check again |
| **Tool & Date** | **[Your AI Tool & Model, e.g., ChatGPT / Claude / Gemini]**, tested on **[Date]**, plus **[Google Sheets / Excel]** |
| **Outcome** | **[1-sentence summary of what you found in your own runs]** |

*PaySetu, its customers and all data in this portfolio are fictional and were created for learning.*

---

## 01 Executive summary

- **The problem:** PaySetu's operations team spends hours on routine work: explaining loans, sorting complaints, writing reports and customer messages.
- **What I tested:** Four zero-shot prompts, one for each task. I checked every answer myself, then rewrote each prompt and ran it again.
- **What I found:** **[Summarise the exact mistakes your AI made across Tasks 1–4]**.
- **My recommendation:** **[State your 2–3 practical rules for using zero-shot prompts safely at PaySetu]**.

---

## 02 The business challenge

PaySetu is a fictional payments start-up. Its 4-person operations team handles loan questions, customer complaints, a monthly report and customer notices. Mistakes here cost money and trust: a wrong EMI, a complaint sent to the wrong team, or a promise the company can't keep.

> **THE BRIEF FROM THE HEAD OF OPERATIONS**
> "Can we use AI with simple instructions, without training it on examples, for our routine tasks? I need to know where it is safe and where it goes wrong."

| # | Task | What I checked myself |
| :---: | :--- | :--- |
| 1 | Explain and calculate an EMI | EMI, total repayment and total interest in my spreadsheet |
| 2 | Sort 8 customer complaints | My own label for each complaint, written before I ran the AI |
| 3 | Summarise a short report | Transaction totals for both months, and any claim not in the passage |
| 4 | Translate a notice and draft an email | Back-translation into English, word count, invented details |

---

## 03 Task 1: Explain and calculate an EMI

### Step 1: The basic prompt
**PROMPT · Basic**
> Explain EMI to a first-year BBA FinTech student in 50 words.

**AI OUTPUT · Basic**
> [Paste exact AI output here]

**My comment:** [Word count] words — [your assessment of clarity and usefulness].

### Step 2: The improved prompt (real loan)
**PROMPT · Improved**
> [Paste your Task 1 prompt for the ₹2,50,000 loan at 14% for 24 months]

**My spreadsheet formula:** `=250000*(14%/12)*(1+14%/12)^24/((1+14%/12)^24-1)`

**AI OUTPUT · Compared with my spreadsheet**

| Item | AI answer | My spreadsheet | Difference |
| :--- | :---: | :---: | :---: |
| Monthly EMI | ₹[Your AI EMI] | ₹12,003 | [Difference] |
| Total repaid | ₹[Your AI Total] | ₹2,88,077 | [Difference] |
| Total interest | ₹[Your AI Interest] | ₹38,077 | [Difference] |

**WHAT WENT WRONG:** [Explain whether your AI rounded `r` or matched your spreadsheet, and by how much it differed].

### Step 3: The revised prompt
**Revision added:** `[Paste the exact constraint you added]`

**RESULT AFTER REVISION:** [Report your AI's revised EMI, total repaid, and total interest].

---

## 04 Task 2: Sort customer complaints

Before running the AI, I labelled all 8 complaints myself so my answer key could not be influenced by the AI's output.

**PROMPT · Zero-shot classification**
> [Paste your exact Task 2 prompt]

**AI OUTPUT · Marked against my answer key**

| Complaint | AI category | My label | AI's reason (short) | OK? |
| :--- | :---: | :---: | :--- | :---: |
| UPI payment failed, but the amount was debited | [AI label] | Payments | [AI reason] | [✔/✘] |
| My EMI was deducted twice this month | [AI label] | Loans | [AI reason] | [✔/✘] |
| My PAN verification is still pending | [AI label] | KYC/Account | [AI reason] | [✔/✘] |
| I transferred ₹5,000, but the recipient hasn't received it | [AI label] | Payments | [AI reason] | [✔/✘] |
| My loan interest rate increased unexpectedly | [AI label] | Loans | [AI reason] | [✔/✘] |
| My account is blocked after updating my KYC | [AI label] | KYC/Account | [AI reason] | [✔/✘] |
| Money has disappeared from my account | [AI label] | Needs review | [AI reason] | [✔/✘] |
| My application was rejected without explanation | [AI label] | Needs review | [AI reason] | [✔/✘] |

**WHAT WENT WRONG:** Score: **[X] / 8**. [Explain which complaints you disagreed with and why].

**Revision added:** `[Paste the rule you added to fix ambiguous complaints]`

**RESULT AFTER REVISION:** Score: **[Y] / 8**. [Describe how the revised output changed].

---

## 05 Task 3: Summarise without inventing

**PROMPT · First version**
> [Paste your initial Task 3 prompt]

**AI OUTPUT · First version**
> [Paste the 3 bullets and "cannot be concluded" list your AI gave]

**WHAT WENT WRONG:** [Identify any unsupported claims or missing limitations in your AI's first response].

**My own calculation of total transaction value:**

| Month | Transactions | Average value | Total value |
| :--- | :---: | :---: | :---: |
| September | 4,20,000 | ₹640 | ₹26.88 crore |
| October | 5,10,000 | ₹590 | ₹30.09 crore |
| Change | +21.4% | −7.8% | +11.9% |

**Revision added:** `[Paste your revised Task 3 prompt]`

**AI OUTPUT · Revised**
> [Paste your revised Task 3 AI output]

**RESULT AFTER REVISION:** [State how many unsupported claims remained].

---

## 06 Task 4: Translate a notice and draft an email

### Part A: Hindi translation
- **First prompt & what went wrong:** [Describe what happened on your first translation run].
- **Revised prompt:**
> [Paste your revised Hindi translation + back-translation prompt]
- **AI OUTPUT · Revised Hindi translation:**
> [Paste the Hindi output]
- **Back-translation check:** [Paste the English back-translation and confirm whether any dates/promises were added].

### Part B: Email to a partner bank
- **First prompt & what went wrong:** [Note any fake IDs, amounts, or word-count issues in your first draft].
- **Revised prompt:**
> [Paste your revised email prompt]
- **AI OUTPUT · Revised email ([Word count] words):**
> [Paste your final placeholder email]

---

## 07 Results at a glance

| What I checked | First prompt | Revised prompt | Change |
| :--- | :---: | :---: | :---: |
| EMI difference from my spreadsheet | [₹X / month] | [₹Y / month] | [Result] |
| Complaints sorted correctly (of 8) | [X] | [Y] | [+Z] |
| Unsupported claims in summary | [X] | [Y] | [−Z] |
| Invented promises in translation | [X] | [Y] | [−Z] |
| Made-up IDs or amounts in email | [X] | [Y] | [−Z] |

---

## 08 Before and after

| Task | First prompt result | Revised prompt result | What I added |
| :---: | :--- | :--- | :--- |
| 1 | [First run note] | [Revised run note] | [Key constraint added] |
| 2 | [First run note] | [Revised run note] | [Key constraint added] |
| 3 | [First run note] | [Revised run note] | [Key constraint added] |
| 4 | [First run note] | [Revised run note] | [Key constraint added] |

---

## 09 Key findings & 10 My recommendation to PaySetu

**Key findings:**
1. [Finding 1 from your experiment]
2. [Finding 2 from your experiment]
3. [Finding 3 from your experiment]

**Recommendations:**
- [Actionable recommendation 1]
- [Actionable recommendation 2]
- [Actionable recommendation 3]

---

## 11 Limitations and next steps

- **Small test:** 8 complaints and one loan are an initial test, not statistical proof. Next step: test 50+ complaints and multiple loan tenures.
- **Single tool & single run:** Tested on **[Your AI Tool]** with one run per prompt. Next step: compare across multiple models and run each prompt 3 times to check consistency.

---

## 12 Reflection and skills

> **MY 100-WORD REFLECTION**
> [Write your own ~100-word reflection explaining which prompt change made the biggest difference in your experiment, what changed in the AI's output, and what you learned.]

| Skills shown | What I learned |
| :--- | :--- |
| Zero-shot prompt writing and revision | [Your takeaway] |
| Financial calculation (EMI) and checking in Sheets | [Your takeaway] |
| Complaint triage with an answer key | [Your takeaway] |
| Fact-checking AI summaries | [Your takeaway] |
| Hindi translation with back-translation | [Your takeaway] |
| Professional business email writing | [Your takeaway] |

---

### Evidence & Screenshots
All genuine AI chat screenshots and spreadsheet verification captures are uploaded in the [`screenshots/`](./screenshots) folder of this repository.
