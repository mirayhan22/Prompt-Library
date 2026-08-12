# P02 · Missing-Information Request

**Section:** 01 — Customer Intake  
**Current portfolio status:** v1.0 prepared for testing  
**Proposed mature automation level:** High

## 1. v1.0 — Initial prompt

```text
Write an email asking this customer for the information we still need.

Missing information: [MISSING_FIELDS]
```

### Why v1.0 is deliberately simple
This is the baseline. Do not describe it as successful before testing it. Run the planned cases and record what actually fails.

## 2. Intended Workflow or Task
Conditionally triggered by P01 when required information is missing. Agent reviews the draft; customer reply returns to the case workflow.

## 3. Problem Being Solved
Generic requests create back-and-forth and can collect unnecessary data. This prompt restricts the request to information needed to continue.

## 4. Automation Potential
**Proposed level:** High

High drafting potential because inputs and output are constrained. Human review remains appropriate before external communication.

**Human-in-the-loop:** The accountable employee/system owner must perform the review described above. Automation level should be revised if testing shows unacceptable exception or error rates.

## 5. Risks and Limitations
Excessive personal-data requests, implied approval, wrong customer details and empty-list errors. Controls: field whitelist, credential prohibitions, no-outcome language, safe fallback and agent review.

## 6. Candidate improved prompt (v1.2 design target)

> **Important:** Do not commit this as the tested final version until your v1.0/v1.1 testing justifies the changes. It is provided as the design target for your iteration process.

```text
You are a customer-service coordinator for an Australian retailer.

Draft a concise message requesting ONLY the information listed in MISSING_FIELDS so the case can continue.

Customer first name: [FIRST_NAME]
Product: [PRODUCT_NAME]
Missing fields: [MISSING_FIELDS]
Ticket reference: [TICKET_REFERENCE]
Approved reply channel: [CONTACT_CHANNEL]

Rules:
- Request only information appearing in MISSING_FIELDS.
- Do not request passwords, PINs, full payment-card details, or unrelated identity documents.
- Explain briefly why the information is needed without blaming the customer.
- Do not imply that a refund, replacement or compensation is approved.
- Do not invent information.

If MISSING_FIELDS is empty, return exactly:
NO INFORMATION REQUEST REQUIRED

Output:
Subject: [maximum 10 words]
Message: [maximum 120 words]

Tone: courteous, neutral and helpful. End with the ticket reference and approved reply channel.
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
