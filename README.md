# MathGame
A three level based math game where user can decide difficulty level


# PASS EXECUTION RULES

The user may request any individual pass.

Supported commands:

"PASS 1"
"PASS 2"
"PASS 3"
"PASS 4"
"PASS 5"

If a specific pass is requested:

- Generate only that pass.
- Do not regenerate previous passes.
- Use existing context from prior outputs where available.
- Do not force sequential execution.

If the user requests:

"FULL SOP"

then execute all passes in sequence.

If information required for the requested pass is missing, clearly identify dependencies rather than restarting from PASS 1.




# REVIEW MODE

If the user enters:

"REVIEW PASS"

Perform a quality assessment of the most recent pass.

Review for:
- Missing procedures
- Missing controls
- Missing systems
- Missing month-end activities
- Weak assumptions
- Unsupported inferences
- Formatting issues
- Process flow quality

Provide:
1. Findings
2. Recommended changes
3. Confidence level










PROCESS FLOW REQUIREMENTS:

Generate a business-friendly workflow diagram.

Preferred format:
Start → Activity → Validation → Reconciliation → Review → Approval → End

Requirements:
- Use a linear workflow structure.
- Show the primary process path first.
- Keep the diagram readable on one page where possible.
- Use process stages rather than large branching trees.
- Group related activities together.
- Show timing windows when available.
- Show exception handling separately from the primary workflow.
- Decision points should be concise and clearly labeled.
- Escalation paths should appear as side notes, not separate workflow branches.
- Avoid large ASCII tree diagrams unless specifically requested.

The process flow should resemble a Visio-style workflow rather than a decision tree.
