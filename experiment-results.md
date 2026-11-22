# Lab 1: Experiment Results & Independent Verification

**Tool Used:** [Enter Tool Name, e.g., ChatGPT / Claude / Gemini]  
**Date Conducted:** [Enter Date]  

---

## Task 1: EMI Explanation & Calculation Verification

### Baseline Output (50-Word Explanation)
> EMI (Equated Monthly Instalment) is a fixed monthly payment a borrower makes to a lender until a loan is fully repaid. Each payment combines principal repayment and interest on the remaining balance. Early EMIs consist mostly of interest, while later EMIs gradually pay off more of the principal amount. *(48 words)*

### Independent Spreadsheet Verification
- **Principal (P):** ₹2,50,000
- **Annual Interest Rate:** 14% → Monthly Rate (`r`) = `0.14 / 12` = `0.01166667`
- **Tenure (`n`):** 24 months
- **Excel / Google Sheets Formula:** `=250000*(14%/12)*(1+14%/12)^24/((1+14%/12)^24-1)`

| Metric | Spreadsheet Result (Exact) | Spreadsheet (Rounded) | Revised AI Output | Variance |
|---|---|---|---|---|
| Monthly EMI | ₹12,003.22 | ₹12,003 | ₹12,003 | ₹0 |
| Total Repayment (EMI × 24) | ₹2,88,077.28 | ₹2,88,077 | ₹2,88,077 | ₹0 |
| Total Interest (Repayment − P) | ₹38,077.28 | ₹38,077 | ₹38,077 | ₹0 |

---

## Task 2: Complaint Classification Audit

| # | Complaint | My Answer Key | Revised AI Category | Match? | Notes |
|---|---|---|---|---|---|
| 1 | UPI payment failed, but the amount was debited. | Payments | Payments | Yes | Clear UPI transaction issue |
| 2 | My EMI was deducted twice this month. | Loans | Loans | Yes | Clear EMI/loan issue |
| 3 | My PAN verification is still pending. | KYC/Account | KYC/Account | Yes | Clear KYC identity check |
| 4 | I transferred ₹5,000, but the recipient hasn't received it. | Payments | Payments | Yes | Clear transfer issue |
| 5 | My loan interest rate increased unexpectedly. | Loans | Loans | Yes | Clear loan terms query |
| 6 | My account is blocked after updating my KYC. | KYC/Account | KYC/Account | Yes | Clear KYC/account access issue |
| 7 | Money has disappeared from my account. | Needs review | Needs review | Yes | Ambiguous; could be fraud, payment, or EMI |
| 8 | My application was rejected without explanation. | Needs review | Needs review | Yes | Ambiguous; product type not stated |

---

## Task 3: PaySetu Factual Summary & Manual Math

### Revised AI Output
**Factual Summary:**
- PaySetu processed 4.2 lakh transactions in September and 5.1 lakh transactions in October.
- Average transaction value decreased from ₹640 in September to ₹590 in October.
- Server downtime increased in October, and no revenue or cost data is available.

**What Cannot Be Concluded:**
- Total revenue, operating costs, or profitability for either month.
- Whether increased server downtime caused the drop in average transaction value.
- Why transaction volume grew despite higher server downtime.
- Customer retention, user growth, or transaction failure rates.

### Independent Calculation of Total Transaction Value

| Month | Transactions | Average Value | Total Transaction Value |
|---|---|---|---|
| September | 4,20,000 | ₹640 | ₹26,88,00,000 (**₹26.88 crore**) |
| October | 5,10,000 | ₹590 | ₹30,09,00,000 (**₹30.09 crore**) |
| **Change** | **+21.43%** | **−7.81%** | **+11.94% (+₹3.21 crore)** |

---

## Task 4: Hindi Translation, Back-Translation & Partner Bank Email

### Part A: Revised Hindi Translation
> **भुगतान विफल**
>
> प्रिय ग्राहक,
>
> तकनीकी समस्या के कारण आपका ₹2,500 का भुगतान पूरा नहीं हो सका।
>
> लेनदेन की स्थिति: विफल  
> राशि: ₹2,500  
> कारण: तकनीकी त्रुटि
>
> यदि आपके खाते से राशि कट गई है, तो कृपया सहायता के लिए ग्राहक सहायता से संपर्क करें।
>
> भुगतान दोबारा करने से पहले कृपया अपना लेनदेन इतिहास जांच लें।
>
> PaySetu सहायता टीम

### English Back-Translation (Verification)
> **Payment Failed**  
> Dear Customer,  
> Due to a technical issue, your payment of ₹2,500 could not be completed.  
> Transaction Status: Failed | Amount: ₹2,500 | Reason: Technical error  
> If the amount has been deducted from your account, please contact customer support for assistance.  
> Before retrying the payment, please check your transaction history.  
> PaySetu Support Team

**Verification Result:** Meaning preserved 100%; no unauthorized refund timeline or promise added.

### Part B: 100-Word Partner Bank Email (with Placeholders)
> **Subject:** Urgent: Delayed Settlement Inquiry – Batch `[Settlement_Batch_ID]`
>
> Dear `[Partner_Bank_Operations_Team]`,
>
> I am writing from PaySetu Operations regarding a delayed settlement for transaction batch `[Settlement_Batch_ID]`, originally scheduled for `[Expected_Settlement_Date]`. The total pending amount of `[Settlement_Amount]` linked to merchant account `[Merchant_Account_Number]` has not yet been credited.
>
> We have verified our internal logs under reference `[Internal_Reference_ID]` and confirmed that the payout file was transmitted on `[Submission_Date]`. Could you please investigate the delay, share the current status, and provide an updated settlement confirmation timeline?
>
> Please let us know immediately if any additional reconciliation details are required.
>
> Best regards,  
> `[Your_Name]`  
> Operations Executive, PaySetu Operations

*(Word count: 100 words; all sensitive IDs, dates, and amounts replaced with placeholders.)*
