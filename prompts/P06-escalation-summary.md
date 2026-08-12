# P06 · High-Risk Escalation Summary

**Section:** 02 — Resolution  
**Current portfolio status:** v1.0 prepared for testing  
**Proposed mature automation level:** Medium

## 1. v1.0 — Initial prompt

```text
Summarise this serious customer complaint for management:
[ESCALATION_CASE]
```

### Why v1.0 is deliberately simple
This is the baseline. Do not describe it as successful before testing it. Run the planned cases and record what actually fails.

## 2. Intended Workflow or Task
Triggered for high-risk or exceptional cases from the resolution workflow. Output goes to an accountable manager and, where required, specialist review.

## 3. Problem Being Solved
High-risk cases need concise, traceable escalation without collapsing allegations, facts and unknowns.

## 4. Automation Potential
**Proposed level:** Medium

Medium: AI can structure information, but consequential interpretation and decisions remain human.

**Human-in-the-loop:** The accountable employee/system owner must perform the review described above. Automation level should be revised if testing shows unacceptable exception or error rates.

## 5. Risks and Limitations
Liability inference, omitted contradictions, reputational/legal harm. Controls: strict grounding, fact/allegation separation, missing-information section and mandatory review.

## 6. Candidate improved prompt (v1.2 design target)

> **Important:** Do not commit this as the tested final version until your v1.0/v1.1 testing justifies the changes. It is provided as the design target for your iteration process.

```text
You are an escalation-documentation assistant supporting a retail customer-service manager.

Using ONLY ESCALATION_CASE, prepare a factual escalation summary.

ESCALATION_CASE:
[ESCALATION_CASE]

Do not determine legal liability, decide whether an allegation is true, infer motive/intent, diagnose injury, recommend disciplinary action, or recommend settlement/compensation.

Output:
ESCALATION TYPE:
[Safety / Legal threat / Discrimination or harassment / High-value / Repeated unresolved issue / Other]

KNOWN FACTS:
- ...

CUSTOMER'S STATED POSITION:
- ...

ACTIONS ALREADY TAKEN:
- ...

UNVERIFIED OR DISPUTED INFORMATION:
- ...

MISSING INFORMATION:
- ...

DECISION REQUIRED FROM MANAGER:
- ...

SOURCE REFERENCES:
- ...

If unavailable write "Not stated".
Maximum 300 words.
Label: DRAFT — HUMAN REVIEW REQUIRED
```

## 7. Iteration log

| Version | Change made | Observed effect | Lesson learned |
|---|---|---|---|
| v1.0 | Initial broad prompt | **[COMPLETE AFTER TESTING]** | **[COMPLETE AFTER TESTING]** |
| v1.1 | **[ADD ONLY CHANGES JUSTIFIED BY v1.0 TEST]** | **[COMPLETE AFTER TESTING]** | **[COMPLETE AFTER TESTING]** |
| v1.2 | **[ADD ONLY IF A SECOND ITERATION IS JUSTIFIED]** | **[COMPLETE AFTER TESTING]** | **[COMPLETE AFTER TESTING]** |

## 8. Evidence to retain
- Test input used (fictional/anonymised)
- AI output
- Your evaluation scores
- Specific failure/strength observed
- Exact prompt change
- Reason for change
- Git commit showing the revision

## 9. Related workflow
See `../workflow/workflow-overview.md`.
