# P04 · Policy-Grounded Resolution Summary

**Section:** 02 — Resolution  
**Current portfolio status:** v1.0 prepared for testing  
**Proposed mature automation level:** Medium

## 1. v1.0 — Initial prompt

```text
Read this customer case and our returns policy and tell me whether we should refund them.

Case: [VERIFIED_CASE]
Policy: [APPROVED_POLICY]
```

### Why v1.0 is deliberately simple
This is the baseline. Do not describe it as successful before testing it. Run the planned cases and record what actually fails.

## 2. Intended Workflow or Task
Receives the verified P03 case and current approved policy. Human agent uses the comparison to make the authorised decision.

## 3. Problem Being Solved
Repeated manual comparison against policy is time-consuming, but the final customer outcome is consequential. AI is used to organise evidence, not own the decision.

## 4. Automation Potential
**Proposed level:** Medium

Medium. Criteria matching can be supported by AI, but authorised staff retain final resolution and exception handling.

**Human-in-the-loop:** The accountable employee/system owner must perform the review described above. Automation level should be revised if testing shows unacceptable exception or error rates.

## 5. Risks and Limitations
Incorrect policy interpretation, stale policy, overconfident eligibility statement. Controls: supplied-policy grounding, uncertainty labels, explicit decision-support boundary and human authorisation.

## 6. Candidate improved prompt (v1.2 design target)

> **Important:** Do not commit this as the tested final version until your v1.0/v1.1 testing justifies the changes. It is provided as the design target for your iteration process.

```text
You are a customer-service decision-support assistant.

Compare VERIFIED_CASE with APPROVED_POLICY and prepare an eligibility summary for a human service agent.

VERIFIED_CASE:
[VERIFIED_CASE]

APPROVED_POLICY:
[APPROVED_POLICY]

Use ONLY these inputs. Do not use external policy/legal knowledge, invent rules, make the final refund/replacement decision, state that the customer is legally entitled to an outcome, or override an exception.

For each relevant policy condition classify evidence as:
SATISFIED / NOT SATISFIED / UNCLEAR OR INFORMATION MISSING / NOT APPLICABLE.

If the case conflicts with policy or policy does not cover the situation, flag HUMAN REVIEW REQUIRED.

Output:
| Policy condition | Case evidence | Status |

Preliminary outcome:
[Appears within supplied policy / Appears outside supplied policy / Insufficient information]

Human-review flags:
- [...]

Maximum 250 words.
End exactly: "This is decision support only. Final resolution requires authorised employee review." 
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
