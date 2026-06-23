Token Optimization Testing Plan

I was thinking of testing the token optimization prompts across three scenarios:

1. Baseline Test (No Optimization)

* Run the SOP Agent using the current prompt and workflow.
* Capture output quality, response length, and token behaviour.
* Use this as the control group.

2. Prompt-Level Optimization

* Use the Token Efficiency Prompt Prefix provided by Brent/Kalpana at the beginning of the request.
* Keep the SOP Agent unchanged.
* Compare results against the baseline.

3. Agent-Level Optimization

* Embed the Token Efficiency rules directly into the agent’s system instructions rather than adding them to every prompt.
* Test whether the behaviour remains consistent while reducing prompt overhead.
* This may be more scalable for broader PC adoption if users do not need to manually add the optimization prompt each time.

Metrics to Compare

Output Quality

* Accuracy of process understanding
* Number of meaningful gaps identified
* Quality of clarification questions generated
* Ability to correctly identify systems, controls, reconciliations, and escalation paths

Efficiency

* Total response length (word count)
* Number of clarification questions generated
* Amount of repetitive content
* Number of follow-up prompts required

Multi-Pass SOP Performance

* Ability to complete Passes 1-5 without context degradation
* Ability to retain information from previous passes
* Number of times a new chat/session is required

Token Management

* Estimated response size
* Whether token warnings occur
* Whether context is lost later in the SOP generation process
* Overall conversation longevity before reaching limits

Expected Outcome

The goal is to determine whether the optimization prompt reduces token consumption while maintaining SOP quality and process understanding. If the agent-level implementation performs similarly to the prompt-level implementation, it may be a better long-term solution for wider Product Control adoption.
