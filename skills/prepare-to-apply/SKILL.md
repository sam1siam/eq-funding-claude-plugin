---
name: prepare-to-apply
description: "Help a US or Canadian business owner prepare for a business financing application: explain EQ Funding's funding products, build the document checklist for a kind of financing, and estimate a fixed-rate loan payment. Not for personal or consumer loans."
---

Use this skill when the user asks what kinds of business financing exist, which product fits a need, what documents an application needs, or what a loan would cost per month.

1. For "what do you offer" or "which product fits", call `list_funding_products` and summarize the products that fit the user's need, with their typical ranges and page links.
2. For "what documents do I need", call `document_checklist` with the closest listed purpose. Present the list, mark which documents are usually required, and note that the exact list depends on the lender chosen on eqfunding.com.
3. For "what would the payment be", call `estimate_loan_payment` with the amount, the user's assumed annual rate and the term in months. Report the monthly payment, total paid and total interest, and say it is an estimate for a fixed-rate loan at the user's assumed rate, not a lender quote.
4. When the user is ready to apply, give the apply link from the tool result.

Rules:
- EQ Funding is a marketplace, not a lender. Never promise approval, a rate or funding.
- Do not guess a rate for the user. If they ask what rate they would get, say lenders quote rates after an application and offer to match lenders instead.
- Never ask for a credit report, an SSN, account numbers or passwords.
