# EQ Funding

EQ Funding is a business-financing marketplace for the United States and Canada. This plugin lets Claude match a business with the kinds of lenders in EQ Funding's network that fit it, list EQ Funding's eight funding products, build a document checklist for an application and estimate a fixed-rate loan payment. One link then opens the application on eqfunding.com with the answers already filled in.

EQ Funding is not a lender. Each lender decides on approval, amounts, rates and terms after it reviews an application, and nothing in the chat is an offer or a guarantee.

## Use it

Ask Claude about funding for a business, for example:

- Could my 2-year-old trucking company in Texas get a $150K equipment loan?
- I run a dental practice in Ontario doing $60K a month. Who could give me a $200K line of credit?
- What documents do I need to apply for an SBA loan?

Claude asks for what the money is for, the country and state or province, the amount, how long the business has operated, its monthly revenue and a rough credit score. It answers how many lenders fit, the type of each, the typical time to an offer and the documents each asks for, and gives the apply link.

## What it contains

- Two skills: `find-business-lenders` (matching) and `prepare-to-apply` (products, documents and payment estimates).
- One connector, EQ Funding's MCP server at `https://www.eqfunding.com/api/mcp/claude` (Streamable HTTP, no authentication), with four read-only tools: `match_lenders`, `list_funding_products`, `document_checklist` and `estimate_loan_payment`.

The plugin runs no code on your computer and needs no account or key.

## Data

The plugin sends only the business answers needed to run a tool to EQ Funding's server at www.eqfunding.com: the funding purpose, country, state or province, amount, months in business, monthly revenue, an approximate credit score if given, industry, customer type and property type, or a loan amount, rate and term for a payment estimate. It never asks for a name, contact details, a Social Security number, bank details, login details or documents. EQ Funding does not store these answers and does not send them to lenders or anyone else; lenders receive information only if the owner submits an application on eqfunding.com. The apply link carries the answers in its address so the application opens filled in.

Privacy policy: https://www.eqfunding.com/privacy (section "EQ Funding in ChatGPT and Claude"). Documentation: https://www.eqfunding.com/ai-assistants. Support: hello@eqfunding.com.
