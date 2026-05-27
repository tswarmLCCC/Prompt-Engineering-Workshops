Chain of Thought (CoT) Prompting

What it is and the Purpose it Solves

Chain of Thought (CoT) prompting forces the AI to explicitly state its reasoning, step-by-step, before arriving at a final answer. It is typically triggered by adding instructions like "Let's think step by step" or "Show your work."

The Problem it Solves

AI models are prone to "hallucinations" (making things up) or logic errors when faced with complex math, multi-layered constraints, or intricate logic puzzles. When asked to provide just the final answer, they try to predict the end result in one jump, which often fails.

Why this Technique Works

By forcing the model to generate the intermediate steps, you are actually feeding the model its own correct logic as context for the next step. It breaks a massive leap of logic into a series of small, highly accurate predictions, drastically increasing the reliability of the final output.

Before & After Examples: Poor vs. Highly Engineered

Example 1: Complex Math

Before: If a company makes $100k in Jan, grows revenue by 10% each month, but expenses start at $50k and grow by 15% each month, what is the profit in April?

After (Highly Engineered): "Calculate the profit for April based on the following variables: January Revenue is $100,000 (10% MoM growth). January Expenses are $50,000 (15% MoM growth).
Before giving the final answer, create a table and show your work step-by-step for each month (Jan, Feb, Mar, Apr), calculating the new revenue, new expenses, and the resulting net profit for each specific month."

Example 2: Logic and Constraints

Before: Schedule meetings for Alice, Bob, and Charlie. Alice can't do mornings, Bob is only free Tuesday, and Charlie is busy Wednesday afternoons.

After: "You need to find a 1-hour meeting time for Alice, Bob, and Charlie.
Constraints: Alice is unavailable before 12 PM. Bob is entirely unavailable except on Tuesdays. Charlie is unavailable on Wednesdays after 12 PM.
Let's think step by step. First, eliminate the days that do not work for all three. Second, evaluate the remaining days against the time-of-day constraints. Finally, propose the best available meeting window."

Example 3: Data Analysis

Before: Look at this data and tell me if the marketing campaign worked.

After: "Analyze the following marketing campaign data. Do not just give a yes or no answer. Walk me through your analytical process step-by-step:
Step 1: Calculate the total Customer Acquisition Cost (CAC).
Step 2: Calculate the Lifetime Value (LTV) of the acquired cohort.
Step 3: Compare the LTV to CAC ratio against the industry standard of 3:1.
Step 4: Provide a final conclusion on profitability. [Insert Data]"

Highly Engineered CPA-Specific Examples

1. Depreciation Calculation

"A client purchased heavy machinery for $150,000 on May 15th of the current tax year. We are using MACRS depreciation.
Please calculate the first-year depreciation deduction. Let's think step by step:
Step 1: Identify the correct MACRS asset class life for heavy construction machinery.
Step 2: Determine the applicable convention (Half-Year vs. Mid-Quarter) based on the purchase date.
Step 3: Identify the correct percentage from the MACRS table.
Step 4: Calculate the final first-year depreciation amount."

2. Tax Residency Determination (Substantial Presence Test)

"Evaluate this client's travel history to determine their US tax residency status for 2026 under the Substantial Presence Test.
History: 110 days in the US in 2026; 120 days in 2025; 150 days in 2024.
Walk me through your logic step-by-step:

State the 31-day minimum requirement for the current year.

Apply the specific multiplier formula for the current year, the first preceding year (1/3), and the second preceding year (1/6).

Sum the calculated days.

Conclude whether they meet the 183-day threshold for residency."

3. Estimated Tax Penalty Analysis

"Determine if this client is subject to an underpayment penalty for their 2026 taxes.
Client Data: 2026 Tax Liability is $45,000. 2026 Withholding is $30,000. 2025 Tax Liability was $35,000. 2026 AGI is $160,000.
Show your reasoning step by step using the IRS safe harbor rules:
First, check if they owe less than $1,000.
Second, check if they paid at least 90% of the current year's tax.
Third, check if they paid 100% (or 110% for high earners) of the prior year's tax.
Conclude with whether a penalty applies and which safe harbor protects them (if any)."
