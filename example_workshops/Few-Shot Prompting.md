Few-Shot Prompting

What it is and the Purpose it Solves

Few-shot prompting involves "teaching" the AI by providing it with a few high-quality examples of the input and the exact desired output before asking it to process your actual data.

The Problem it Solves

Zero-shot prompting fails when you need a highly specific, proprietary, or non-standard format that the AI won't naturally default to. If you need output to match your firm's specific internal coding, tone guidelines, or data structuring, you have to show the AI what "correct" looks like.

Why this Technique Works

Language models are exceptional pattern recognizers. By showing the AI a pattern (Input A -> Output A, Input B -> Output B), it temporarily adapts its behavior to match your exact constraints, ignoring its default tendencies.

Before & After Examples: Poor vs. Highly Engineered

Example 1: Formatting Messy Data

Before: Clean up this list of names and numbers.

After (Highly Engineered): "Process the following raw data strings into a standardized JSON format. Follow the exact capitalization and formatting shown in the examples.
Example 1:
Input: 'john doe - paid 500 dollars on 12/04'
Output: {Name: Doe, J., Status: Paid, Amount: $500.00, Date: 2026-04-12}
Example 2:
Input: 'SMITH, JANE. owes 45.50 due 10/11'
Output: {Name: Smith, J., Status: Pending, Amount: $45.50, Date: 2026-11-10}
Now process the following input: [Insert Raw Data]"

Example 2: Tone Translation

Before: Make these emails sound more professional.

After: "Translate internal, blunt employee notes into polished, client-facing responses. Maintain the core boundary but soften the delivery.
Example 1:
Input: 'Tell them no, they missed the deadline by a week.'
Output: 'Thank you for your submission. Unfortunately, because the deadline passed on [Date], we are unable to process this request at this time.'
Example 2:
Input: 'I can't do this until next Tuesday, I'm swamped.'
Output: 'I have received your request and have added it to my queue. I will be able to provide a comprehensive update by next Tuesday.'
Now translate this: 'They forgot to attach the W-2 again, tell them to send it or we can't file.'"

Example 3: Sentiment Classification

Before: Categorize these reviews.

After: "Classify the following customer feedback into one of three categories: [Urgent Issue], [Feature Request], or [General Praise].
Input: 'The app crashes every time I export.' -> Output: [Urgent Issue]
Input: 'I wish there was a dark mode.' -> Output: [Feature Request]
Input: 'Great tool, saves me hours.' -> Output: [General Praise]
Now classify this: 'The latest update deleted all my saved templates.'"

Data Analysis and Advanced Classification

Few-shot prompting is highly effective for converting unstructured text into structured data. By providing clear examples, you can force the AI to apply specific grading scales, route information, or extract exact data points without adding unwanted conversational filler.

Example 4: Likert Scale Scoring

Use Case: Converting qualitative feedback into quantitative data.

Prompt: "Score the following employee feedback on a 1-5 Likert scale for 'Process Efficiency' (1 = Highly Inefficient, 5 = Highly Efficient). Only output the number.
Input: 'The new reimbursement process requires four different approvals and takes weeks.' -> Output: 1
Input: 'I just snap a picture of the receipt and it auto-syncs. Done in seconds.' -> Output: 5
Input: 'It is okay, but I sometimes have to manually enter the tax amount.' -> Output: 3
Now score this: 'Logging hours is straightforward, though the system lags a bit on Fridays.'"

Example 5: Support Ticket Routing

Use Case: Automatically categorizing and assigning incoming requests.

Prompt: "Route the incoming client emails to the correct department: [Tax Prep, Audit, Payroll, General Admin].
Input: 'My employees did not get their direct deposits this morning.' -> Output: Payroll
Input: 'We received a notice saying our books are under review by the state.' -> Output: Audit
Input: 'Can we schedule our annual planning meeting?' -> Output: General Admin
Now route this: 'I need to send you the K-1s from my real estate investments.'"

Example 6: Multi-Factor Extraction

Use Case: Pulling out multiple specific data points from a single text block.

Prompt: "Analyze the financial commentary. Output the overall sentiment (Bullish, Bearish, Neutral) and the primary driver in a JSON format.
Input: 'We expect margins to expand next quarter due to lower material costs.' -> Output: {Sentiment: Bullish, Driver: Lower material costs}
Input: 'Regulatory headwinds continue to pressure our revenue growth across Europe.' -> Output: {Sentiment: Bearish, Driver: Regulatory headwinds}
Now analyze this: 'While Q3 sales were flat, our new software product pipeline looks strong for next year.'"

Highly Engineered CPA-Specific Examples

1. Chart of Accounts Categorization

"You are an automated bookkeeping assistant. Categorize the following bank feed descriptions into the exact General Ledger account names provided in the examples. Do not deviate from these category names.
Input: 'AMZN Mktp US' -> Output: 'Office Supplies & Software'
Input: 'DELTA AIR LINES' -> Output: 'Travel & Meals'
Input: 'GUSTO INTUIT' -> Output: 'Professional Services'
Input: 'STARBUCKS STORE' -> Output: 'Travel & Meals'
Now categorize the following transactions: [Insert Bank Feed]"

2. Client 'Shoebox' Translation

"Convert messy, informal client notes regarding their deductions into formal, tax-ready descriptions suitable for workpapers.
Note: 'Bought a bunch of lumber and nails at Home Depot for the new deck' -> Output: 'Job Materials - Home Depot (Lumber/Hardware)'
Note: 'Took the team out to Applebees to celebrate the big win' -> Output: 'Meals & Entertainment - Applebees (Staff Event)'
Note: 'Paid my brother to fix the office plumbing' -> Output: 'Repairs & Maintenance - Subcontractor'
Now convert this note: 'Bought a new Macbook Pro at Best Buy for editing videos'"

3. IRS Notice Response Drafting

"Generate a standard response framework for an IRS notice based on the notice type. Follow the provided format strictly.
Input: CP2000 (Underreported Income)
Output: 'Dear [Client Name], We received a CP2000 notice indicating a discrepancy between your return and documents reported to the IRS. Please upload any missing 1099s/W-2s to the portal so we can draft a response agreeing to or disputing the changes.'
Input: CP14 (Balance Due)
Output: 'Dear [Client Name], We received a CP14 notice indicating a balance due of [Amount] for tax year [Year]. We will review our records to ensure your payments were credited properly. If correct, payment is required by [Date].'
Now generate a response for: LTR 2205A (Audit Examination)"
