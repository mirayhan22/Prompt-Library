# Workflow Overview

## Business problem
Southern Cross Retail receives customer complaints and operational information as unstructured text. Employees repeatedly classify cases, request missing information, prepare case summaries, compare cases with approved policy, draft communications, document incidents, hand over store issues, and aggregate recurring themes.

The library supports these repetitive information-processing activities while retaining accountable human decisions for consequential outcomes.

## End-to-end workflow

```text
CUSTOMER ISSUE
    |
    v
P01 Complaint Intake & Risk Triage
    |
    +-- missing information --> P02 Missing-Information Request --+
    |                                                            |
    +<-----------------------------------------------------------+
    |
    v
P03 Case Preparation Summary
    |
    v
P04 Policy-Grounded Resolution Summary
    |
    +-- routine/authorised decision --> P05 Customer Response Draft
    |
    +-- exception/high risk ---------> P06 Escalation Summary --> Human decision

STORE OPERATIONS
    |
    +-- incident --> P07 Incident Report Draft --> Manager verification
    |
    +-- shift end -> P08 Shift Handover --------> Incoming manager

VALIDATED / CLOSED CASES
    |
    v
P09 Weekly Complaint Theme Analysis
    |
    v
P10 Weekly Management Action Brief
    |
    v
Management review and decisions
```

## Automation boundaries

| Prompt | Proposed automation | Required human control |
|---|---|---|
| P01 | Very High for classification | Review High/Other/ambiguous cases and audit |
| P02 | High for drafting | Agent reviews before sending |
| P03 | High for extraction/formatting | Agent verifies source fidelity |
| P04 | Medium decision support | Authorised employee makes final resolution |
| P05 | High for drafting | Employee approves and sends |
| P06 | Medium | Manager/legal/compliance review as applicable |
| P07 | Medium | Mandatory manager factual verification |
| P08 | High | Incoming manager reviews priorities/status |
| P09 | Medium–High | CX manager validates themes/limitations |
| P10 | Medium | Management interprets and decides |
