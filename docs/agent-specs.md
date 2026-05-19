# Agent Specifications

## Purpose

This document defines example agent specifications for finance, accounting, legal, and corporate operations workflows.

These are not production-ready build documents. They are structured examples showing how an enterprise AI automation function should translate business workflows into agent specifications.

## Specification Template

Each agent should include:

1. Purpose statement
2. Business owner
3. Inputs
4. Processing logic
5. Outputs
6. Human handoff criteria
7. Edge cases
8. Failure definition
9. Acceptance criteria
10. Governance notes

---

## Agent 1: Finance Reporting Agent

### Purpose

Generate recurring leadership reporting drafts from approved finance data sources and route the final narrative for finance approval.

### Business Owner

Finance leadership

### Inputs

- Approved finance reports
- Budget vs. actual data
- Prior-period comparison files
- Department-level cost data
- Revenue or expense variance reports
- Manual commentary from finance owners

### Processing Logic

- Pull approved reporting inputs
- Identify material variances
- Compare current period to prior period
- Draft plain-English variance commentary
- Flag missing or inconsistent inputs
- Route summary for finance review

### Outputs

- Draft executive reporting summary
- Variance commentary
- Missing-input flag
- Material-change summary
- Finance approval request

### Human Handoff Criteria

Human review is required when:

- Variance exceeds threshold
- Input source is incomplete
- Commentary affects executive reporting
- Output may influence financial decision-making
- User challenges model interpretation

### Failure Definition

A bad output is one that:

- Misstates financial performance
- Invents a variance explanation
- Uses unapproved data
- Routes commentary without finance review
- Hides uncertainty

### Acceptance Criteria

- Uses only approved data sources
- Clearly marks draft status
- Routes final commentary to finance leadership
- Logs source files used
- Flags missing inputs instead of guessing

---

## Agent 2: Accounting Close Assistant

### Purpose

Track close-cycle tasks, identify blockers, summarize status, and escalate missing items to the correct owner.

### Business Owner

Accounting leadership

### Inputs

- Close checklist
- Task owner list
- Reconciliation status
- Email or workflow updates
- Due dates
- Exception notes
- Prior close-cycle issues

### Processing Logic

- Track open and completed close tasks
- Identify missing reconciliations
- Detect late items
- Summarize close status
- Generate owner-specific follow-ups
- Escalate blockers based on due date and severity

### Outputs

- Close status summary
- Blocker list
- Late task alerts
- Owner follow-up drafts
- Executive close progress digest

### Human Handoff Criteria

Human review is required when:

- Close certification is involved
- Reconciliation discrepancy exceeds threshold
- Task owner disputes status
- Financial statement impact is possible
- Escalation affects leadership visibility

### Failure Definition

A bad output is one that:

- Marks a task complete without evidence
- Escalates to the wrong owner
- Omits a material blocker
- Confuses status update with close approval

### Acceptance Criteria

- Task ownership is visible
- Late items are accurately flagged
- Completion status is source-backed
- Accounting leadership retains final authority

---

## Agent 3: Legal Intake Agent

### Purpose

Standardize legal request intake by summarizing requests, extracting key terms, identifying missing materials, and routing the matter to the correct legal review path.

### Business Owner

Legal operations or general counsel designee

### Inputs

- Legal request form
- Contract draft
- Vendor or customer name
- Contract type
- Requested deadline
- Supporting documents
- Business owner notes

### Processing Logic

- Summarize the legal request
- Extract key terms
- Identify missing documents
- Classify request type
- Detect urgent or high-risk terms
- Route to legal review queue

### Outputs

- Intake summary
- Missing-document checklist
- Contract type classification
- Risk flag
- Routing recommendation

### Human Handoff Criteria

Human review is required for:

- Legal interpretation
- Redlines
- Final contract positions
- Unusual indemnity, liability, exclusivity, termination, or payment terms
- Any request with regulatory or compliance exposure

### Failure Definition

A bad output is one that:

- Gives legal advice
- Approves terms
- Misses a high-risk clause
- Routes the request incorrectly
- Treats missing documents as complete

### Acceptance Criteria

- Clearly labels output as intake support
- Does not approve legal terms
- Routes all legal judgments to humans
- Flags missing information
- Maintains audit trail

---

## Agent 4: Spreadsheet Replacement Agent

### Purpose

Identify recurring manual spreadsheet workflows and convert them into structured reporting pipelines or governed dashboards.

### Business Owner

Department owner of the spreadsheet workflow

### Inputs

- Existing spreadsheet
- Source files
- Manual update process
- Output audience
- Recurrence schedule
- Data source list
- Known errors or manual workarounds

### Processing Logic

- Map spreadsheet purpose
- Identify source systems
- Separate calculation logic from manual cleanup
- Identify repeatable steps
- Flag data quality issues
- Recommend pipeline or dashboard structure

### Outputs

- Spreadsheet dependency map
- Data source map
- Manual step inventory
- Replacement workflow recommendation
- Dashboard or pipeline concept

### Human Handoff Criteria

Human review is required when:

- Business logic is ambiguous
- Spreadsheet formulas are undocumented
- Output affects finance, legal, or executive reporting
- Data source ownership is unclear

### Failure Definition

A bad output is one that:

- Automates broken spreadsheet logic
- Ignores hidden manual adjustments
- Treats unclear formulas as valid rules
- Creates reporting without a business owner

### Acceptance Criteria

- Manual steps are documented
- Source systems are named
- Business logic is validated
- Owner confirms output accuracy
- Replacement path is scoped before build

