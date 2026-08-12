# P08 · Shift Handover Action List

**Section:** 03 — Store Operations  
**Current portfolio status:** v1.0 prepared for testing  
**Proposed mature automation level:** High

## 1. v1.0 — Initial prompt

```text
Turn these notes into a clear shift handover:
[SHIFT_NOTES]
```

### Why v1.0 is deliberately simple
This is the baseline. Do not describe it as successful before testing it. Run the planned cases and record what actually fails.

## 2. Intended Workflow or Task
Runs at shift end from supervisor notes. Incoming manager reviews the structured handover and acts on verified items.

## 3. Problem Being Solved
Free-text handovers can obscure outstanding actions, timing and status. Structured handover improves operational continuity.

## 4. Automation Potential
**Proposed level:** High

High for transformation/formatting, with incoming manager responsible for action and priority review.

**Human-in-the-loop:** The accountable employee/system owner must perform the review described above. Automation level should be revised if testing shows unacceptable exception or error rates.

## 5. Risks and Limitations
False completion, invented urgency or altered times. Controls: explicit classification rules, unclear-priority fallback and exact preservation of references.

## 6. Candidate improved prompt (v1.2 design target)

> **Important:** Do not commit this as the tested final version until your v1.0/v1.1 testing justifies the changes. It is provided as the design target for your iteration process.

```text
You are a retail shift-handover assistant.

Transform SHIFT_NOTES into an operational handover for the incoming manager.

SHIFT_NOTES:
[SHIFT_NOTES]

Use only SHIFT_NOTES. Do not invent priorities, deadlines, completion status or staff instructions.

Classify each supported item:
- URGENT — explicit safety issue or explicitly due before/at next shift
- OPEN — action remains outstanding
- INFORMATION — no action explicitly required
- COMPLETED — only if notes explicitly state completion

If priority is unclear, classify as OPEN and write:
"Priority requires manager review."

Output:
SHIFT HANDOVER — [STORE] — [DATE]

URGENT
☐ ...

OPEN
☐ ...

INFORMATION
• ...

COMPLETED
✓ ...

MISSING / UNCLEAR INFORMATION
• ...

Maximum 250 words.
Preserve supplied times, locations and reference numbers exactly.
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
