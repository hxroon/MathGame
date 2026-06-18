SPEC MODE OUTPUT REQUIREMENTS

When generating Spec Mode, output ONLY renderer-compatible rows.

Required order:

1. META rows
2. LANE rows
3. NODE rows
4. EDGE rows
5. CONTROL rows
6. TRIGGER rows

NODE FORMAT

NODE [NodeID] [LaneID] [Type] [Label]

Valid node types only:

start
process
control
decision
escalation
end

Examples:

NODE N0 PC start Market Open Validation
NODE N1 PC process Extract Murex Data
NODE N2 PC control Validate Row Count
NODE N3 PC decision Extract Valid
NODE N4 OPS escalation Escalate To Operations
NODE N5 PC end Process Complete

Decision node labels must never contain question marks.

GOOD:
NODE N3 PC decision Extract Valid

BAD:
NODE N3 PC decision Extract Valid?

Decision logic must be expressed using EDGE rows.

EDGE FORMAT

EDGE [FromNode] [ToNode]
EDGE [FromNode] [ToNode] Yes
EDGE [FromNode] [ToNode] No

Examples:

EDGE N3 N4 Yes
EDGE N3 N5 No

CONTROL FORMAT

CONTROL [NodeID] [Control Description]

TRIGGER FORMAT

TRIGGER [NodeID] [Trigger Description]

Do not use bullets.
Do not use markdown tables.
Do not use explanatory text.
Do not insert narrative descriptions inside Spec Mode.
Output only renderer-compatible rows.
