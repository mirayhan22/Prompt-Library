# P03 · Case Preparation Summary

**Section:** 01 — Customer Intake  
**Current portfolio status:** v1.0 prepared for testing  
**Proposed mature automation level:** High

## 1. v1.0 — Initial prompt

```text
Summarise this customer case for the service agent:
[CASE_DATA]
```

### Why v1.0 is deliberately simple
This is the baseline. Do not describe it as successful before testing it. Run the planned cases and record what actually fails.

## 2. Intended Workflow or Task
Runs after intake information is sufficiently complete. Output becomes the evidence-organising input for P04.

## 3. Problem Being Solved
Agents otherwise reread multiple messages and order notes before assessing a case. Structured preparation reduces repetitive synthesis while preserving source boundaries.

## 4. Automation Potential
**Proposed level:** High

High for extraction and formatting; low for resolution judgement. Agent must verify the summary against source records.

**Human-in-the-loop:** The accountable employee/system owner must perform the review described above. Automation level should be revised if testing shows unacceptable exception or error rates.

## 5. Risks and Limitations
Loss of nuance, omitted contradictions and invented chronology. Controls: use-only grounding, Not stated fallback, review flags and source verification.

## 6. Candidate improved prompt (v1.2 design target)

> **Important:** Do not commit this as the tested final version until your v1.0/v1.1 testing justifies the changes. It is provided as the design target for your iteration process.

```text
You are a customer-service case-preparation assistant.

Using only CASE_DATA, convert the customer's case into a factual handover for the employee who will assess the resolution.

CASE_DATA:
[CASE_DATA]

Extract:
1. Ticket reference
2. Customer's stated issue
3. Product/order information explicitly supplied
4. Requested resolution
5. Actions already taken
6. Outstanding information
7. P01 category and urgency
8. Explicit safety/legal indicators

For every unsupported field write "Not stated".

Do not decide eligibility, infer customer intent, assign blame, infer legal liability, recommend compensation, or invent chronology.

Output a two-column table:
Field | Verified case information

Then:
REVIEW FLAGS:
- [maximum 3 factual issues requiring employee attention]

Maximum 220 words.
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
