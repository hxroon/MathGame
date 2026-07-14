The Decomp Commentary Agent now needs to combine the best parts of the earlier dashboard output with the stronger commentary from the newer version.

1. Preserve the required report structure

The final table must contain only:

Business	Actual P&L	Analyst Comment	AI Comment



Remove:

Estimate

Variance


The analyst comment and AI comment must remain in separate columns so Evan can compare them quickly.

2. Keep the modern dashboard formatting

Do not let the agent redesign the report into a long document.

Keep:

Executive dashboard header

Report date and currency

Top contributor cards

Dominant and secondary driver sections

Named client activity

Largest loss cards

Grouped business hierarchy

Review and data-quality section

Consistent colours, spacing and typography


The HTML layout should remain identical from one file to another.

3. Improve the Executive Summary

Use a fixed structure:

1. Top Contributors, top three positive business lines, with values and brief drivers.


2. Dominant Driver, the largest decomposition theme across the business.


3. Secondary Driver, the second-largest theme.


4. Notable Named Flow, clients, positions or deals explicitly identified in the source.


5. Largest Losses, top three negative businesses and their known drivers.


6. Executive Takeaway, a short overall conclusion, ideally three to five sentences.



It should not describe every business line.

4. Make the AI comments richer

Each AI comment should answer:

What happened?

What drove it?

What offset or supported it?

How did it affect the parent business?


The AI should synthesize the financial decomposition and analyst comment rather than repeat them.

For example:

> IG USA delivered a strong positive result, led by new trading activity in Commercial Paper, with additional support from Hedging Pod and Utilities. These gains helped offset weaker portfolio revaluation elsewhere in Investment Grade and were a major contributor to the segment’s overall result.



5. Keep the commentary concise

The newer version became too long.

Set limits such as:

Leaf business comment, two to four sentences

Parent roll-up comment, two to three sentences

Top contributor or loss description, three to five lines

Executive Takeaway, no more than five sentences


Mention only the two to four most material drivers.

6. Avoid repetitive and artificial wording

Do not start every row with:

“Performance was...”

“The business generated...”

“Results were...”


Vary openings naturally, but do not become overly creative.

Avoid phrases such as:

“demonstrated operational execution capability”

“continued relationship momentum”

“capitalized on opportunities”

“profound dispersion”


The tone should sound like Product Control, not marketing or consulting.

7. Do not over-interpret

The agent should explain the information, not invent conclusions.

It must not recommend actions such as:

> Management should urgently review position sizing.



unless that concern is explicitly supported by the analyst comment or a clearly defined review rule.

Safer wording would be:

> The size and concentration of the loss should be highlighted for analyst review.



8. Preserve source information correctly

Copy the Analyst Comment exactly as written.

Do not correct or summarize it in its column.

Use the analyst comment and decomposition as evidence for the AI comment.

Do not invent clients, trades, market causes or risk explanations.


When evidence is limited, state:

> No analyst commentary was provided. Commentary is based on the financial decomposition and business hierarchy only.



9. Handle hierarchy properly

The agent must first identify:

Overall business

Parent groups

Sub-businesses

Leaf desks

Total rows


Parent AI comments should summarize the child businesses instead of treating the parent as an independent line.

The hierarchy section should also reconcile to the workbook totals where possible.

10. Apply the correct unit consistently

The final report should display all monetary values in C$000s.

The agent should first confirm whether the workbook is already stored in thousands. It must not divide by 1,000 again if the source is already in C$000s.

The recent output incorrectly displayed values such as C$979.6 million when the actual table value was 979,635 in C$000s, so currency scaling must be explicitly validated before writing any commentary.

11. Strengthen review and data-quality checks

Flag:

Material P&L with missing or thin analyst commentary

Missing business names or actuals

Unclear hierarchy

Parent and child totals that do not reconcile

Named flows with unclear context

Low-confidence AI commentary

Potential unit or scaling issues


Do not claim “High confidence” or “roll-ups verified” unless the agent actually completed those checks.

12. Focus consistency testing on first-run quality

Run the same frozen instructions against the four historical files separately.

Compare:

Same HTML structure

Same section ordering

Correct hierarchy

Correct units

Commentary depth

No invented facts

Similar writing quality


Once those four perform reliably, ask Evan for a new week of files and test them without changing the prompt. That unseen sample is the proper validation of whether the agent is ready.
