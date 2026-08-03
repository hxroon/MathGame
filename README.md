No, the instructions did not clearly require HTML for all three options.

The earlier wording said:

Option 1: Workbook Instructions, it was described like an SOP or runbook, so the agent reasonably produced a document.

Option 2: HTML Workbook Analysis Report.

Option 3: HTML IT Handoff Report.


So the agent behaved consistently with the prompt. You now need to update the instructions so every option produces a standalone, user-friendly HTML dashboard.

Use the following changes.

1. Replace the report selection menu

Workbook successfully analyzed.

Select the HTML dashboard you would like to generate:

PASS 1 — Workbook Operating Instructions Dashboard
Generate a user-friendly HTML guide explaining how an analyst should run the workbook, based on AI interpretation of workbook structure, dependencies, formulas, macros, inputs, outputs, and validations.

PASS 2 — Full Workbook Analysis Dashboard
Generate the complete business and technical HTML dashboard, including tabs, diagrams, flowcharts, worksheet inventory, data flow, formula logic, relationships, risks, controls, and automation opportunities. Exclude the IT Handoff tab and all IT Handoff content.

PASS 3 — IT Handoff Dashboard
Generate a standalone HTML dashboard containing only the IT Handoff analysis, technical architecture, dependencies, external connections, macros, Power Query, Power Pivot, risks, modernization opportunities, and support considerations.

Reply with:
PASS 1
PASS 2
or
PASS 3

2. Add this near the top under Primary Objective

# MANDATORY OUTPUT FORMAT

All three passes must generate a complete standalone HTML dashboard.

Never generate a plain-text report, Word-style document, Markdown report, narrative document, or non-HTML output.

Every pass must return one self-contained HTML file with embedded CSS and, where needed, embedded JavaScript.

The HTML must:

- Open directly in a browser
- Require no external libraries
- Be professional and user-friendly
- Use consistent navigation, typography, spacing, colours, cards, tables, and callouts
- Support printing
- Work in Microsoft Edge and Google Chrome
- Adapt to different screen sizes
- Clearly label verified, inferred, and unverified information

If the user selects PASS 1, PASS 2, or PASS 3, output HTML only.
Do not include commentary before or after the HTML unless a critical limitation prevents generation.

3. Replace the full PASS 1 section with this

# PASS 1 — WORKBOOK OPERATING INSTRUCTIONS DASHBOARD

## PURPOSE

Generate a standalone HTML dashboard explaining how an analyst is likely expected to run and operate the workbook.

The operating instructions are inferred from workbook evidence, including:

- Worksheet structure
- Worksheet order
- Formula dependencies
- Manual input areas
- Power Query refreshes
- External links
- Macros
- Buttons
- Validation sheets
- Control totals
- Output sheets
- Reporting sheets
- File naming conventions
- Typical Product Control workflow

The dashboard must clearly distinguish between:

- Verified workbook behaviour
- AI-inferred operating steps
- Information requiring workbook-owner confirmation

Never present inferred operating steps as confirmed facts.

## REQUIRED HTML TABS

The PASS 1 dashboard must use these tabs in this exact order:

1. Overview
2. Before You Begin
3. Inputs & Prerequisites
4. How to Run the Workbook
5. Validation Checks
6. Outputs
7. Common Issues
8. Troubleshooting
9. Assumptions & Confidence

Never remove, rename, merge, or reorder these tabs.

If a tab is not applicable, retain the tab and display:

Not Applicable or Unable to Verify.

## TAB 1 — OVERVIEW

Include:

- Workbook name
- Workbook purpose
- Supported Product Control process
- Primary users
- Likely execution frequency
- Key statistics
- Main inputs
- Main outputs
- Overall confidence
- Short explanation of how the instructions were inferred

Use summary cards at the top.

## TAB 2 — BEFORE YOU BEGIN

Document:

- Required systems
- Required files
- Required permissions
- Required network or SharePoint locations
- Expected workbook version
- Required market data
- Required source reports
- Dependencies that must be available before starting

Label all uncertain prerequisites as:

Workbook Owner Confirmation Required.

## TAB 3 — INPUTS & PREREQUISITES

Use a table with:

| Input | Source | Destination | Required Action | Refresh Method | Confidence |

Include:

- Manual inputs
- Imported data
- External files
- Lookup data
- Configuration tables
- Market data
- Power Query sources
- Macro inputs

## TAB 4 — HOW TO RUN THE WORKBOOK

Generate a numbered, step-by-step operating workflow.

Each step must include:

- Step number
- Action
- Purpose
- Worksheet or system
- Expected result
- Validation
- Confidence status

Use a visual process flow at the top of this tab.

The process flow should show only the major stages, such as:

Prepare Inputs
→ Load or Refresh Data
→ Validate Data
→ Run Calculations
→ Review Reconciliations
→ Resolve Exceptions
→ Produce Outputs
→ Save and Distribute

Keep the visual concise and readable.

If more than 15 operational steps are detected, group them into phases rather than placing every step in the main diagram.

Detailed steps should remain in the table below.

For steps that are inferred rather than directly proven, display a visible badge:

AI Inferred, Confirm With Workbook Owner.

## TAB 5 — VALIDATION CHECKS

Include:

- Input completeness checks
- Refresh checks
- Formula checks
- Reconciliation checks
- Control totals
- Broken link checks
- Error value checks
- Output reasonableness checks
- Sign-off checks

Use a structured checklist or table.

## TAB 6 — OUTPUTS

Document:

- Reports produced
- Output worksheets
- Exported files
- Downstream systems
- Distribution recipients, if identifiable
- File naming conventions
- Completion criteria

## TAB 7 — COMMON ISSUES

Identify likely operational problems based on workbook evidence.

Examples:

- Missing source file
- Broken link
- Failed refresh
- Macro error
- Missing reference data
- Incorrect date
- Stale market data
- Formula error
- Reconciliation imbalance
- Output not generated

Do not invent issues unsupported by workbook structure.

## TAB 8 — TROUBLESHOOTING

For each identified issue include:

| Issue | Likely Cause | How to Diagnose | Suggested Resolution | Escalation Needed |

Clearly state when the resolution is inferred.

## TAB 9 — ASSUMPTIONS & CONFIDENCE

Include:

- Verified operating steps
- AI-inferred steps
- Unable-to-verify items
- Missing supporting documents
- Questions for the workbook owner
- Confidence by area

## PASS 1 HTML DESIGN

Use:

- Tabbed navigation
- Summary cards
- A concise high-level process flow
- Numbered instruction cards or a structured table
- Status badges
- Collapsible details where useful
- Consistent professional styling

Do not generate a document-style page.
Do not generate Markdown.
Return HTML only.

4. Strengthen PASS 2

Add this at the beginning of PASS 2:

PASS 2 must generate a standalone tabbed HTML dashboard.

It must preserve the detailed capabilities of the original Excel Decoder, including:

- Executive summary
- Workbook architecture
- Worksheet classification
- Sheet inventory
- Data flow
- Process flow
- Relationship diagrams
- Formula and logic analysis
- Data dictionary
- Macro and automation analysis
- Risks and controls
- Technical architecture
- Recommendations
- Confidence and limitations

The IT Handoff tab and all IT Handoff content must be completely excluded.

Do not create an empty IT Handoff tab.
Do not reference IT Handoff elsewhere in the dashboard.

Use these PASS 2 tabs:

1. Overview
2. Architecture
3. Worksheets
4. Data Flow
5. Logic & Formulas
6. Data Dictionary
7. Relationships
8. Automation
9. Risks & Controls
10. Technical Architecture
11. Recommendations
12. Confidence & Limitations

Add:

PASS 2 must include concise, readable diagrams and flowcharts.

Required visuals where supported by workbook evidence:

- Workbook architecture diagram
- High-level data flow diagram
- Worksheet relationship map
- High-level operational process flow
- System interaction diagram, if external systems exist

If a visual would exceed approximately 20 to 25 nodes, group repeated logic and show only the major stages. Never generate an unreadable diagram.

5. Replace PASS 3 opening and tabs

# PASS 3 — IT HANDOFF DASHBOARD

PASS 3 must generate a standalone, self-contained HTML dashboard intended for Finance IT, developers, support teams, and transformation teams.

Do not generate a narrative document.
Do not include the broader business workbook report.
Do not include operating instructions except where essential to technical support.

## REQUIRED HTML TABS

1. Technical Summary
2. Architecture
3. Dependencies
4. External Connections
5. Power Query
6. Power Pivot
7. VBA & Macros
8. Formula Complexity
9. Data Lineage
10. Performance & Stability
11. Technical Risks
12. Modernization Opportunities
13. Maintenance & Support
14. Recommended Next Steps
15. Assumptions & Confidence

Never remove, rename, merge, or reorder these tabs.

If a feature is not present, retain the tab and state:

Not Detected.

## REQUIRED VISUALS

Where supported, include:

- Technical architecture diagram
- External dependency map
- Data lineage flow
- Refresh and calculation flow
- Macro interaction map
- Target-state modernization diagram

Keep diagrams concise and readable.

6. Replace your current HTML standards with this

# SHARED HTML DASHBOARD STANDARD

These rules apply to PASS 1, PASS 2, and PASS 3.

Every output must be a complete standalone HTML document containing:

- <!DOCTYPE html>
- <html>
- <head>
- Embedded CSS
- <body>
- Tabbed navigation
- All requested content
- Closing </body> and </html> tags

No external CSS, JavaScript, icons, fonts, or libraries may be required.

Use the same design system across all passes:

- Consistent header
- Consistent tab navigation
- Consistent typography
- Consistent spacing
- Consistent cards
- Consistent tables
- Consistent status badges
- Consistent callout boxes
- Consistent diagram styling
- Consistent footer

Only the tab names and content should change by pass.

The dashboard should feel like one unified Product Control tool.

Use a clean professional layout suitable for internal RBC use.

Do not use excessive animation.
Do not use decorative graphics that do not add meaning.
Do not generate extremely long single-page HTML.
Use tabs to separate content.
Use collapsible subsections within tabs when needed.

7. Add this to final validation

# HTML OUTPUT VALIDATION

Before returning any pass, verify:

✓ Output is HTML
✓ HTML is complete and self-contained
✓ Selected pass is the only pass generated
✓ Required tabs exist in the correct order
✓ No tabs from other passes are included
✓ Navigation works
✓ Tables are readable
✓ Diagrams are readable
✓ No diagram is excessively compressed
✓ Verified and inferred information are clearly distinguished
✓ No Markdown report or plain-text document appears outside the HTML

If any check fails, correct the output before returning it.

The main problem was that PASS 1 was never explicitly defined as HTML. With these replacements, all three passes will use the same dashboard framework, while each one remains focused on a different audience and purpose.
