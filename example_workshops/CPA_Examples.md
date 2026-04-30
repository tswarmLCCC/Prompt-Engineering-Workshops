# CPA Workbook: Practical Application

This workbook applies the theories from the guide to specific CPA tasks. For each technique, we compare a "Lazy Prompt" (what a beginner typically tries) with an "Engineered Prompt" to show how the results change.

## 1. Role-Based Prompting: The Tax Advisor

**Task:** Explaining the 20% Qualified Business Income (QBI) deduction to a client.

**Lazy Prompt:** "Tell my client about the QBI deduction for their S-Corp."

**The Beginner Failure:** The AI usually provides a generic Wikipedia-style summary. It often misses the "SSTB" (Specified Service Trade or Business) distinction entirely, or it uses casual language that sounds unprofessional for a CPA firm. It might also use outdated 2018 thresholds.

**Engineered Prompt:**

"Act as a Senior Tax Manager. Draft an email to an S-Corp client explaining the QBI deduction and SSTB phase-out limitations for the 2024 tax year.

Use professional but accessible language.

Define the exact income thresholds for 2024.

State the consequences of being an SSTB.

Include a standard professional disclaimer."

**The Improvement:** By setting the "Senior Tax Manager" role, the AI adopts a conservative tone and focuses on the high-risk "SSTB" nuances that a general assistant would ignore.

## 2. Delimiters: Extracting Facts from Client Emails

**The Problem:** A client sends a 5-paragraph rambling email. You just need the tax-relevant facts.

**Lazy Prompt:** "Summarize this email for my tax workpapers: [Email Text]"

**The Beginner Failure:** This leads to "Context Leakage." The AI might include the client's stories about their kids' graduation or a vacation, which clutters the workpaper. It may even get confused and try to "respond" to the client's questions instead of extracting data for you.

**Engineered Prompt:**

"I will provide a client email below. Your task is to extract only the facts relevant to their 2024 tax return into a bulleted list.

Use the following structure to prevent your instructions from getting mixed with the data:

CLIENT EMAIL START

[Paste Email Here]

CLIENT EMAIL END

Ignore any personal anecdotes or non-financial information. Focus on: New assets, changed filing status, or new income sources."

**The Improvement:** Delimiters (the ### markers) act as a "firewall." They tell the AI exactly where the client's rambling ends and your professional analysis begins.

## 3. Few-Shot & Coding: Cleaning Trial Balances

**Task:** Convert messy text from a Trial Balance into a clean CSV format.

**Lazy Prompt:** "Turn this trial balance text into a CSV table."

**The Beginner Failure:** The AI often fails at the math or the formatting. It might leave credits as positive numbers (standard accounting error) or fail to parse account numbers that have dashes in them. If you have 100 rows, the AI will likely "truncate" the list and say "and so on..." instead of doing the work.

**Engineered Prompt:**

"I need to convert messy Trial Balance text into a CSV. Here are two examples of the format I need:
Example 1: '1010-00 .. Cash ... 1,200.50 (Dr)' -> '1010-00, Cash, 1200.50'
Example 2: '2010-01 .. A/P ... 500.00 (Cr)' -> '2010-01, A/P, -500.00'

Based on these examples, write a Python script using 'pandas' to read 'raw_tb.txt'. The script must handle the regex for account numbers and ensure all (Cr) values are converted to negative floats. Export to 'cleaned_tb.csv'."

**The Improvement:** "Few-Shot" examples show the AI exactly how to handle the (Dr)/(Cr) logic. Using Python ensures the AI doesn't "get tired" and skip rows; the code will process 1,000 rows as easily as 10.

## 4. Negative Prompting: Precise Research Memos

**The Problem:** You need a technical summary without the "AI fluff."

**Lazy Prompt:** "What are the new 1099-K rules?"

**The Beginner Failure:** The AI will likely write a long, polite essay starting with "In the ever-evolving world of tax regulation..." and include several paragraphs of history about why the rule was created. This is a waste of time for a busy professional.

**Engineered Prompt:**

"Summarize the key changes in the 1099-K reporting thresholds for 2024 and 2025.

Constraints:

DO NOT include any introductory or concluding pleasantries.

DO NOT discuss the history of the 1099-K prior to 2022.

AVOID generic 'expert' filler words.

Provide the answer in a three-column table: [Old Rule, New Rule, Effective Date]."

**The Improvement:** Negative constraints act as "scope of work" boundaries. They force the AI to be a researcher, not a writer, saving you from editing out the fluff.

## 5. Chain of Thought: Audit Sampling Logic

**Task:** Determining and documenting an audit sample size.

**Lazy Prompt:** "What should my sample size be for $4.2M in accounts payable with high risk?"

**The Beginner Failure:** The AI will give you a number (e.g., "60") without showing how it got there. If a reviewer asks how you arrived at that number, "the AI said so" is not a valid answer. Furthermore, the AI's "mental math" is often wrong if it doesn't show its steps.

**Engineered Prompt:**

"Think step-by-step to determine the sample size for an Accounts Payable test of details.

Population: 1,200 invoices ($4.2M).

Tolerable Misstatement: $50,000.

Control Environment: 'Effective' (Low RMM).

Expected Misstatement: $5,000.
Show your work for each logical step of the calculation. End with a two-sentence 'Rationale for Workpapers' that I can copy-paste into our engagement software."

**The Improvement:** Chain of Thought (CoT) creates the "Audit Trail." It ensures the AI considers the "Effective" control environment before suggesting a number, and it provides the documentation required for professional standards.

## 6. Adversarial Prompting: Peer Review

**Task:** Validating an Employee Retention Credit (ERC) research memo.

**Lazy Prompt:** "Check this ERC memo for errors."

**The Beginner Failure:** The AI is naturally "agreeable" (sycophantic). It will likely say "This looks like a great memo!" and fix the grammar while leaving massive technical errors or non-existent tax codes in place.

**Engineered Prompt:**

"Act as a 'Hostile Peer Reviewer.' Audit the following ERC memo for a restaurant client.

Flag any Internal Revenue Code sections that are hallucinated.

Highlight any logic that contradicts recent IRS warnings regarding 'ERC Mills.'

If you are unsure of a fact, append [VERIFICATION REQUIRED]. Do not assume the text is correct.
[Insert Memo Here]"

**The Improvement:** Adversarial prompting breaks the "agreeability" of the AI. It forces the model to look for reasons why the memo is wrong, which is exactly what a CPA needs to do before filing.