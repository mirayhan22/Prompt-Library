# P07 · Incident Report First Draft

**Section:** 03 — Store Operations  
**Current portfolio status:** v1.0 prepared for testing  
**Proposed mature automation level:** Medium

## 1. v1.0 — Initial prompt

```text
Write an incident report based on these staff notes:
[STAFF_NOTES]
```

### Why v1.0 is deliberately simple
This is the baseline. Do not describe it as successful before testing it. Run the planned cases and record what actually fails.

## 2. Intended Workflow or Task
Triggered after a store incident is reported. Duty manager verifies the draft before it becomes an organisational record.

## 3. Problem Being Solved
Manual incident documentation is repetitive and inconsistent, but inaccurate records can create serious legal/compliance consequences.

## 4. Automation Potential
**Proposed level:** Medium

Medium. Drafting/structure can be automated; factual verification and submission cannot.

**Human-in-the-loop:** The accountable employee/system owner must perform the review described above. Automation level should be revised if testing shows unacceptable exception or error rates.

## 5. Risks and Limitations
Invented causation, incomplete notes, false legal record. Controls: use-only grounding, no-inference rules, insufficient-data fallback and mandatory manager verification.

## 6. Candidate improved prompt (v1.2 design target)

> **Important:** Do not commit this as the tested final version until your v1.0/v1.1 testing justifies the changes. It is provided as the design target for your iteration process.

```text
You are a store-operations documentation assistant.

Using ONLY STAFF_NOTES and VERIFIED_RECORDS, prepare a DRAFT incident report.

STAFF_NOTES:
[STAFF_NOTES]

VERIFIED_RECORDS:
[VERIFIED_RECORDS]

Do not infer cause, fault, negligence, liability, injury severity, motives, or undocumented events.

Required sections:
1. INCIDENT SUMMARY
2. TIMELINE — if time unavailable write "Time not stated"
3. PEOPLE/ROLES INVOLVED — approved identifiers only
4. IMMEDIATE ACTIONS — explicitly recorded actions only
5. INFORMATION REQUIRING VERIFICATION
6. NEXT ADMINISTRATIVE STEP — only if supplied; otherwise "Manager to determine next step."

If any required section lacks evidence write:
"Insufficient data — follow-up required."

Tone: factual, neutral, third-person.
Maximum 350 words.
Header: DRAFT INCIDENT REPORT — MANAGER VERIFICATION REQUIRED
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
