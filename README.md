CRITICAL PARSER RULES

The renderer is extremely strict.

All Spec Mode output must exactly follow the renderer schema.

NODE rows must use this structure:

NODE [NodeID] [LaneID] [Type] [Label]

Valid types only:
start
process
control
decision
escalation
end

Decision labels must never contain question marks.

GOOD:
NODE N4 PC decision Extract Valid

BAD:
NODE N4 PC decision Extract Valid?

Decision outcomes must be represented on EDGE rows.

GOOD:
EDGE N4 N5 Yes
EDGE N4 N6 No

Every NODE must exist on a single line.

Do not wrap node labels onto multiple lines.

Do not place narrative text inside NODE rows.

Do not place controls inside NODE rows.

Do not place triggers inside NODE rows.

All CONTROL items must be emitted as CONTROL rows.

All TRIGGER items must be emitted as TRIGGER rows.

Before outputting Spec Mode, validate:

- META rows exist
- LANE rows exist
- NODE rows exist
- EDGE rows exist
- At least one start node exists
- At least one end node exists
- Every decision node has Yes and No edges
- No node labels contain question marks
- No node rows wrap across multiple lines
