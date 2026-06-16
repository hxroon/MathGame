PROCESS FLOW AND VISUAL DIAGRAM GENERATION STANDARDS

PURPOSE

PASS 2 must generate visual documentation in TWO formats:

1. PROSE MODE
2. SPEC MODE

Both formats are mandatory.

The purpose of Prose Mode is to provide a detailed analyst-readable narrative.

The purpose of Spec Mode is to provide structured input for the PC SOP Process Flow Renderer.

The agent must never generate only one format.

For every visual generated, the agent must generate BOTH formats.

---

SUPPORTED VISUAL TYPES

The following visual types must be supported:

- Process Flow Diagram
- Data Flow Diagram
- Reconciliation Logic Diagram
- Exception Escalation Diagram
- Control Framework Diagram
- System Architecture Diagram
- Swimlane Diagram
- Data Lineage Diagram
- Validation Framework Diagram
- Month-End Workflow Diagram
- Daily Operational Workflow Diagram

If a visual is required in the SOP, both Prose Mode and Spec Mode must be generated.

---

OUTPUT ORDER

For every diagram:

Generate output in this order:

Diagram Title

Prose Mode

[narrative process]

Spec Mode

[renderer specification]

Never reverse the order.

Never output only one mode.

---

PROSE MODE REQUIREMENTS

Prose Mode must describe:

Step Number

Owner

System Used

Input

Process

Control

Output

Escalation Path

Example:

Step 1: Market Open Validation
Owner: Trader / Product Control

System:
Bloomberg
Trader Sheet

Input:
Spot rates

Process:
Validate spot rates have refreshed.

Control:
Cross-check Bloomberg feed.

Output:
Validated market data.

Escalation:
Notify Technology Support if Bloomberg feed unavailable.

---

SPEC MODE REQUIREMENTS

Immediately after Prose Mode generate:

##DIAGRAM_SPEC_START##

and end with

##DIAGRAM_SPEC_END##

The renderer specification must contain:

META

LANE

NODE

EDGE

sections.

---

META SECTION

Always include:

META agent SOP Agent

META product [Product Name]

META version [SOP Version]

META diagram [Diagram Type]

---

LANE SECTION

Every role becomes a lane.

Example:

LANE FO Front Office

LANE PC Product Control

LANE OPS Operations

LANE TECH Technology

LANE FIN Finance

---

NODE SECTION

Node format:

NODE [ID] [LANE] [TYPE] [DESCRIPTION]

Allowed Types:

start

process

control

decision

escalation

end

Examples:

NODE N1 FO start Market Open

NODE N2 TECH process Load Murex Extract

NODE N3 PC control Book Mapping Validation

NODE N4 PC decision Variance Above Threshold

NODE N5 PC escalation Escalate To Senior PC

NODE N6 PC end Daily Sign Off

---

EDGE SECTION

Node relationships.

Examples:

EDGE N1 N2

EDGE N2 N3

EDGE N3 N4

EDGE N4 N5 YES

EDGE N4 N6 NO

---

PROCESS FLOW RULES

Flow direction must always be logical and sequential.

Start

Load

Validate

Reconcile

Investigate

Escalate

Approve

Sign Off

End

Decision points must always be represented using decision nodes.

All YES/NO paths must be explicit.

No orphan nodes.

No disconnected paths.

---

SWIMLANE RULES

If multiple teams participate:

Trader

Front Office

Operations

Technology

Product Control

Finance

must be separated into individual lanes.

Ownership must always be visible.

---

RECONCILIATION LOGIC RULES

For reconciliations include:

Source System

Target System

Tolerance

Break Identification

Investigation Path

Resolution Path

Escalation Path

Sign-Off

Each becomes a node sequence.

---

DATA FLOW RULES

Data Flow Diagrams must show:

Source

Transformation

Validation

Aggregation

Reporting

Output

Every data movement must become a process node.

Every validation becomes a control node.

---

CONTROL FRAMEWORK RULES

Controls must be represented as control nodes.

Include:

Preventive Controls

Detective Controls

Manual Controls

Automated Controls

Escalation Controls

Sign-Off Controls

---

MANDATORY VALIDATION

Before completing PASS 2 verify:

✓ Prose Mode exists

✓ Spec Mode exists

✓ META exists

✓ LANE exists

✓ NODE exists

✓ EDGE exists

✓ Start node exists

✓ End node exists

✓ Decision branches labelled

✓ Escalations represented

✓ Ownership assigned

If any validation fails regenerate output before presenting to user.

The agent must never output a diagram without both Prose Mode and Spec Mode.
