# P10 · Weekly Management Action Brief

**Section:** 04 — Management Insight  
**Current portfolio status:** v1.0 prepared for testing  
**Proposed mature automation level:** Medium

## 1. v1.0 — Initial prompt

```text
Write a weekly management summary from these customer and operations notes:
[DATA]
```

### Why v1.0 is deliberately simple
This is the baseline. Do not describe it as successful before testing it. Run the planned cases and record what actually fails.

## 2. Intended Workflow or Task
Receives validated metrics, P09 themes and operational issues. Produces a draft briefing for management review and decision.

## 3. Problem Being Solved
Managers need a concise cross-workflow view, but manual consolidation is repetitive and may blur evidence and recommendation.

## 4. Automation Potential
**Proposed level:** Medium

Medium. AI can assemble and structure the brief; managers retain interpretation, prioritisation and decisions.

**Human-in-the-loop:** The accountable employee/system owner must perform the review described above. Automation level should be revised if testing shows unacceptable exception or error rates.

## 5. Risks and Limitations
Invented ROI/trends, false completion and overconfident recommendations. Controls: validated-input requirement, explicit prohibitions, insufficient-evidence fallback and management review.

## 6. Candidate improved prompt (v1.2 design target)

> **Important:** Do not commit this as the tested final version until your v1.0/v1.1 testing justifies the changes. It is provided as the design target for your iteration process.

```text
You are a retail operations analyst preparing a weekly briefing for senior management.

Use ONLY:
VALIDATED_METRICS: [VALIDATED_METRICS]
P09_THEME_OUTPUT: [P09_THEME_OUTPUT]
OPEN_OPERATIONAL_ISSUES: [OPEN_OPERATIONAL_ISSUES]
PREVIOUS_APPROVED_ACTIONS: [PREVIOUS_APPROVED_ACTIONS]

Do not invent financial impact, ROI, causes, targets, unsupported trends, completed actions or customer sentiment beyond supplied evidence.

Create exactly five sections:
1. EXECUTIVE SNAPSHOT — maximum 3 bullets
2. CUSTOMER ISSUES — maximum 3 evidence-based observations
3. OPERATIONAL EXCEPTIONS — safety/service/workflow exceptions
4. ACTION TRACKER
| Previous action | Current verified status | Owner if supplied | Next review |
5. MANAGEMENT DECISIONS REQUIRED — maximum 3 decisions, each with evidence, why management input is required, and missing information.

Maximum 450 words.
Where evidence is insufficient write:
"Insufficient evidence for conclusion."

Separate observed facts from recommendations.
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
