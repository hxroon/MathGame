Can you help me rewrite the SOP Agent instructions for Product Control?

I want to improve two things:

1. Pass selection
The agent should ask the user at the start which pass they want to generate:
- TRIAGE
- PASS 1
- PASS 2
- PASS 3
- PASS 4
- PASS 5
- FULL SOP
- REVIEW MODE
- REGENERATE MODE

The user should not always have to start from PASS 1. If they want PASS 3, the agent should generate only PASS 3 using available context. If information is missing, it should clearly state what dependency is missing instead of forcing a restart.

2. Embedded process flow diagrams
For PASS 2, improve the Process Flow section so it creates SOP-ready diagrams that are easy to follow and can be embedded into Word.

Avoid Mermaid if RBC Assist cannot render it visually. Instead, provide:
- A clean business process map in markdown/table format
- An SVG-ready diagram specification, if possible
- A simple HTML/SVG option that can be exported as an image
- A fallback linear workflow if rendering is not supported

The process flow should be easy for a Product Control analyst to understand, with:
- Start and end points
- Main workflow
- Systems
- Timing windows
- Decision points
- Controls
- Escalations
- Exception paths shown separately

Please rewrite the relevant sections of the agent instructions so I can paste them into the SOP Agent. Keep the existing 5-pass SOP structure, but make the pass selection and process flow generation more flexible and user-friendly.
