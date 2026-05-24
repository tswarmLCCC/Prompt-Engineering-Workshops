# Comprehensive AI Workflow Catalog for CPAs

This catalog serves as an inspiration guide for accounting professionals looking to integrate LLMs into their daily practice. It moves beyond simple "chatting" into structured, high-value workflows.

## 1. Professional Communications & Drafting

### A. Client Advisory Summaries

**Workflow:** Take a complex technical update (like a new IRS revenue procedure) and rewrite it for a specific client's industry.

**Prompt Example:** "Rewrite the attached IRS guidance on 174 R&E capitalization specifically for a software development client. Focus on why their current year's cash flow will be impacted. Use a professional, advisory tone."

### B. "Voice-to-Memo" Capture

**Workflow:** Record a voice note after a client meeting, transcribe it, and have the AI turn the raw "brain dump" into a formal internal memo or follow-up email.

**Prompt Example:** "I am pasting a raw transcript of my post-meeting thoughts. Turn this into a formal internal file memo. Identify: 1. Key tax issues raised, 2. Agreed-upon deadlines, 3. Missing information we need to request from the client."

### C. Difficult Conversations / Conflict Resolution

**Workflow:** Draft responses to sensitive situations (e.g., billing disputes, scope creep, or firing a client) to ensure professionalism and emotional neutrality.

**Prompt Example:** "I need to respond to a client who is complaining about a bill for out-of-scope work on their audit. Draft a polite but firm response that references our engagement letter's 'Additional Services' clause. Maintain the relationship but do not waive the fee."

## 2. Flashy Excel & Formula Mastery (The "Power User")

### D. Advanced "Logic-Heavy" Formula Generation

**Workflow:** Build complex, multi-step formulas for data reconciliation that would normally require a senior-level Excel expert.

**Prompt Example:** "I have two sheets. Sheet1 has 'Vendor Name' and 'Amount'. Sheet2 has 'Vendor Alias' and 'Payment Reference'. The names don't match exactly (e.g., 'Apple Inc' vs 'Apple'). Write a flashy Excel formula using XLOOKUP and WILDCARDS, or a LAMBDA function, that reconciles these two lists and flags any variance over $0.01."

### E. Complex Formatting & Data Cleanup

**Workflow:** Using AI to generate "one-click" solutions for messy client data exports.

**Prompt Example:** "I have a messy list of 5,000 transactions where the Date, Description, and Amount are all in one cell, separated by inconsistent spaces. Write a single Excel formula using TEXTSPLIT and LET that breaks these into three clean columns and converts the date to a proper Excel date format."

### F. Dynamic Dashboard & Indirect Referencing

**Workflow:** Create formulas that automatically update report headers or data ranges based on a single cell (like "Month" or "Entity Name").

**Prompt Example:** "I am building a consolidation workbook. I need a formula that uses INDIRECT and ADDRESS to pull the 'Total Revenue' from a specific tab based on the text string in cell B1. If B1 says 'Subsidiary_A', the formula should pull from that tab's cell Z100."

## 3. Technical Tax & Accounting Research

### G. Multi-State Nexus Comparisons

**Workflow:** Compare rules across multiple jurisdictions quickly to identify filing obligations.

**Prompt Example:** "Compare the economic nexus thresholds for sales tax in California, Texas, and New York. Present the results in a table showing the dollar threshold, transaction threshold, and effective date for each."

### H. Code-to-Plain-English Translation

**Workflow:** Break down dense legislative text into understandable logic for staff training or client education.

**Prompt Example:** "Explain IRC Section 1202 (Qualified Small Business Stock) as if I am a first-year associate. Use a 'step-by-step' logic flow to determine if a taxpayer's stock qualifies for the 100% exclusion."

## 4. Audit & Assurance Efficiency

### I. Risk Assessment Brainstorming

**Workflow:** Use the AI to suggest potential fraud risks or "what could go wrong" scenarios for a specific industry.

**Prompt Example:** "I am auditing a high-volume e-commerce company that uses Shopify and multiple payment gateways. Brainstorm 5 specific fraud risks related to the revenue cycle and suggests an audit procedure to test each one."

### J. Internal Control Narrative Summarization

**Workflow:** Paste a long interview transcript about a client's internal controls and have the AI generate a clean "narrative" or "flowchart logic."

**Prompt Example:** "Based on the following interview notes with the Controller, write a formal narrative of the 'Order-to-Cash' cycle. Identify any clear gaps where duties are not properly segregated."

## 5. Data Processing & Automation (The "Staff Assistant")

### K. Regex & Data Cleaning

**Workflow:** Generate complex formulas or scripts to fix "broken" data from client software.

**Prompt Example:** "I have a column of dates formatted as '24-Jan-05' but I need them to be 'YYYY-MM-DD' for my software. Write an Excel formula and a Python snippet to perform this conversion."

### L. VBA / Macro Generation

**Workflow:** Create custom Excel macros without knowing how to code.

**Prompt Example:** "Write a VBA macro that looks at Column A for account numbers. If the account starts with '1', color the row blue (Asset). If it starts with '2', color it red (Liability). Do this for all rows with data."

## 6. Practice Management & Growth

### M. Capacity Planning & Scheduling

**Workflow:** Optimize staff assignments based on skill sets and deadlines.

**Prompt Example:** "I have 4 seniors and 10 associates. We have 50 tax returns due in 3 weeks. Suggest an optimal allocation of staff hours to ensure no one works more than 55 hours per week while prioritizing the 10 most complex files."

### N. Content Marketing for CPAs

**Workflow:** Turn a boring tax update into a LinkedIn post that actually gets engagement.

**Prompt Example:** "Take this technical summary of the New Beneficial Ownership Information (BOI) reporting requirements and turn it into a LinkedIn post. Use a 'Warning' hook to catch the attention of small business owners."

## 7. Personal Productivity

### O. Meeting Summarization

**Workflow:** Use a tool to record a Zoom meeting and have the AI summarize the decisions made.

**Prompt Example:** "Summarize this transcript. Don't tell me who said what. Just give me a list of 'Action Items,' 'Decisions Made,' and 'Parking Lot items for the next meeting'."

### P. "The Rubber Duck" (Thinking Partner)

**Workflow:** Explain a complex problem to the AI just to see if your logic holds up.

**Prompt Example:** "I'm thinking about a complex reorganization for a client. I'll explain my plan, and you tell me if I'm missing any obvious tax traps or if there's a simpler way to achieve the same result under Section 368."
