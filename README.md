1. Excel Decoder / Data Architecture Agent

Goal: take any Excel workbook and explain how it works operationally.

It should identify:

* Tabs/sheets and purpose of each
* Inputs, outputs, calculations, lookups, pivots
* Data points/attributes
* Relationships between sheets
* Manual steps vs automated steps
* Macros and what they do, if visible
* Data flow from source input to final output
* Risks/gaps, like hardcoded values, broken links, unclear owners

Ideal output:

* HTML visual map
* Data architecture summary
* Workbook operating model
* IT-friendly data model

Good test file:

* FX Options Excel workbook

Possible next step:
Create an agent called Excel Workbook Decoder and use FX Options as the pilot.

⸻

2. Decomp Commentary Agent

Goal: take actual vs estimate/decomp data and produce usable commentary.

It should output:

* Executive summary
* Business name
* Actual
* Analyst/decomp comment
* AI-generated comment

Key issue to solve:

* Consistency. Same input should produce the same style and quality.
* It needs to work quickly, ideally within 15-20 minutes, because the process has a tight turnaround.
