# P09 · Weekly Complaint Theme Analysis

**Section:** 04 — Management Insight  
**Current portfolio status:** v1.0 prepared for testing  
**Proposed mature automation level:** Medium–High

## 1. v1.0 — Initial prompt

```text
Analyse these complaints and tell management the main trends:
[DE_IDENTIFIED_CASES]
```

### Why v1.0 is deliberately simple
This is the baseline. Do not describe it as successful before testing it. Run the planned cases and record what actually fails.

## 2. Intended Workflow or Task
Runs on validated, de-identified closed-case data at the agreed reporting interval. CX manager validates themes before circulation.

## 3. Problem Being Solved
Manual thematic analysis is repetitive and susceptible to inconsistent categorisation and overgeneralisation.

## 4. Automation Potential
**Proposed level:** Medium–High

Medium–High for aggregation; interpretation and action selection remain human.

**Human-in-the-loop:** The accountable employee/system owner must perform the review described above. Automation level should be revised if testing shows unacceptable exception or error rates.

## 5. Risks and Limitations
Privacy exposure, incorrect counts, overgeneralisation and invented causes. Controls: de-identification, supplied-sample limits, evidence references and human validation.

## 6. Candidate improved prompt (v1.2 design target)

> **Important:** Do not commit this as the tested final version until your v1.0/v1.1 testing justifies the changes. It is provided as the design target for your iteration process.

```text
You are a retail customer-insights analyst.

Analyse only DE_IDENTIFIED_CASES:
[DE_IDENTIFIED_CASES]

Group cases into no more than six operational themes.

For each theme:
- count cases;
- calculate percentage of the supplied sample;
- identify affected channel/product/store only if explicitly available;
- provide up to two representative case references;
- distinguish observed evidence from interpretation.

Do not infer customer demographics, infer unsupported causes, claim the sample represents all customers, expose direct identifiers, or fabricate prior-period trends.

Output:
| Theme | Count | % of supplied cases | Evidence | Possible operational follow-up |

Then:
LIMITATIONS
- sample size;
- supplied-cases-only limitation;
- missing/contextual data.

ESCALATION SIGNALS
- repeated safety, privacy or serious service issues.

Label proposed follow-ups "For management consideration".
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
