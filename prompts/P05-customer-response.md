# P05 · Customer Resolution Response Draft

**Section:** 02 — Resolution  
**Current portfolio status:** v1.0 prepared for testing  
**Proposed mature automation level:** High

## 1. v1.0 — Initial prompt

```text
Write a response to this customer explaining our decision:
[CASE]
[DECISION]
```

### Why v1.0 is deliberately simple
This is the baseline. Do not describe it as successful before testing it. Run the planned cases and record what actually fails.

## 2. Intended Workflow or Task
Runs only after an authorised employee decision. Agent reviews and sends the draft.

## 3. Problem Being Solved
Separates consequential decision-making from repetitive communication drafting, improving consistency without delegating authority.

## 4. Automation Potential
**Proposed level:** High

High for drafting; sending remains human-controlled, particularly during pilot.

**Human-in-the-loop:** The accountable employee/system owner must perform the review described above. Automation level should be revised if testing shows unacceptable exception or error rates.

## 5. Risks and Limitations
Unauthorised promises, invented dates and wrong decision. Controls: authorised-decision dependency, incomplete-input fallback, no-extension rule and human approval.

## 6. Candidate improved prompt (v1.2 design target)

> **Important:** Do not commit this as the tested final version until your v1.0/v1.1 testing justifies the changes. It is provided as the design target for your iteration process.

```text
You are a customer-care communications specialist.

Draft a response using ONLY:
VERIFIED_CASE: [VERIFIED_CASE]
AUTHORISED_DECISION: [AUTHORISED_DECISION]
APPROVED_NEXT_STEPS: [APPROVED_NEXT_STEPS]

Do not change or extend the authorised decision. Do not invent compensation, dates, delivery promises, policy rules or legal statements.

The response must:
1. acknowledge the customer's specific issue;
2. state the authorised decision clearly;
3. explain the approved next step;
4. identify anything the customer must do;
5. provide the ticket reference;
6. provide an approved contact route.

If AUTHORISED_DECISION is blank, return:
INCOMPLETE INPUT — AUTHORISED DECISION REQUIRED

Tone: calm, accountable and helpful.
Maximum 180 words.

Output:
Subject:
Message:
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
