# BUS4005 Assessment 1 — AI Prompt Library Portfolio

## Project
**Business field:** Australian omnichannel retail  
**Organisation:** Southern Cross Retail (fictional mid-sized retailer)  
**Purpose:** Evidence portfolio for the iterative development of a 10-prompt workflow-automation library.

> This repository is the development portfolio, not a replacement for the LMS submission. The final assessment submission should include the required report, video pitch, and an accessible link to this repository.

## Workflow sections
1. **Customer Intake:** P01–P03
2. **Resolution:** P04–P06
3. **Store Operations:** P07–P08
4. **Management Insight:** P09–P10

See [`workflow/workflow-overview.md`](workflow/workflow-overview.md).

## How to use this repository
For each prompt:
1. Start with the deliberately simple **v1.0** shown in the prompt file.
2. Run the six test cases in `testing/test-cases.md`.
3. Save/copy the relevant output or record a concise factual observation in `testing/evaluation-log.md`.
4. Make only changes that address an observed failure.
5. Update the prompt file to v1.1 and commit it.
6. Test again, record the result, then create v1.2 only where further improvement is justified.
7. Never invent test scores, time savings, evaluator feedback, dates, or observed effects.

## Suggested commit sequence
Use separate commits so GitHub history demonstrates development. Example:

- `Create P01 complaint triage v1.0`
- `Test P01 v1.0 and record failures`
- `Improve P01 with fixed taxonomy and JSON v1.1`
- `Test P01 v1.1`
- `Add grounding and escalation controls to P01 v1.2`

Repeat this pattern for P02–P10.

## Evidence standard
A strong iteration record answers four questions:
- **What changed?**
- **Why did it change?**
- **What did testing show?**
- **What lesson informed the next version?**

## Academic integrity / evidence note
Fields marked **[COMPLETE AFTER TESTING]** must be completed from your genuine test runs. Do not replace them with invented results.
