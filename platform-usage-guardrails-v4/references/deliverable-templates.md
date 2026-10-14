# Deliverable templates

Full structure for the four deliverables in Step 8 of SKILL.md.

Produce four deliverables when sufficient information exists.

Scale the detail to the available evidence.

Use Markdown files unless the user requests another format.

## Deliverable A: Team guide

Suggested filename:

`PLATFORM-team-usage-guide.md`

Write for a non-technical team member.

### Required structure

#### One-minute summary

Explain:

- What the platform provides
- How the team will access it
- What drives usage or cost
- Whether the allowance is shared
- What users must do before a large pull
- Whether the integration is ready for use

Keep this section short enough to read in one minute.

#### Situation

Include:

Platform:
Evidence source:
Access method:
Account status:
Readiness status:
Policy owner:
Last verified:

Use UNKNOWN or TO BE CONFIRMED where necessary.

#### What we know

Include an evidence table:

| Item | Value | Evidence status | Source | Verified |
|------|-------|-----------------|--------|----------|
| Billing unit | | | | |
| Included allowance | | | | |
| Cost per unit | | | | |
| Reset period | | | | |
| Overage rules | | | | |
| Shared allowance | | | | |
| Usage monitoring | | | | |

Only populate values supported by evidence.

#### How cost works

Explain the billing formula in plain English.

Distinguish:

- Fixed licence costs
- Variable usage costs
- Claude's own usage
- Vendor API or connector charges

Do not combine these into a single estimate unless the
necessary information is available.

#### Example requests

Show realistic low, mindful and high-consumption examples.

Include numerical estimates only when calculable.

When the billing unit is unknown, show operational request
counts and clearly state that vendor consumption is unknown.

#### Patterns to prefer

Explain how to minimise unnecessary consumption.

#### Patterns to avoid

Explain the requests most likely to cause unexpectedly
high consumption.

#### Approval tiers

Include approved thresholds, units and approvers.

Mark unapproved thresholds as placeholders.

#### Calibration plan

Explain the smallest approved tests needed to understand
consumption.

#### Administrative controls

Identify documented settings for:

- Usage monitoring
- Alerts
- Spending limits
- Access permissions
- Rate limits
- Shared allowance management

Do not claim a control exists without evidence.

#### Data-handling rules

Summarise relevant restrictions on storage, sharing,
redistribution and external AI processing.

#### Vendor questions

List specific unanswered questions.

Prioritise questions that block safe implementation.

#### Source conflicts and gaps

Explain conflicting information without hiding it.

#### Sources

List the source title, location, relevant date and
verification date.

---

## Deliverable B: Claude-facing rules file

Suggested filename:

`PLATFORM-claude-usage-rules.md`

This file is intended for use as project knowledge or
another explicitly supported instruction location.

Mark it DRAFT unless the organisation has approved it.

### Required structure

# PLATFORM Usage Rules

## Status

Platform:
Access method:
Account status:
Readiness:
Owner:
Version:
Last verified:
Review trigger:

## Objective

Use PLATFORM efficiently while protecting shared allowances
and respecting authorised data use.

## Before every potentially billable pull

1. Identify the exact requested scope.
2. Check whether the operation is authorised.
3. Check whether the intended use is permitted.
4. Estimate expected consumption where possible.
5. Show the estimate to the user.
6. Determine the applicable approval tier.
7. Obtain approval where required.
8. Execute only the approved scope.

## Standard estimate

Show:

Platform:
Access method:
Items:
Markets:
Metrics:
Period:
Expected calls:
Estimated vendor units:
Estimated cost:
Remaining allowance:
Assumptions:
Approval requirement:
Approval status:

Use UNKNOWN when evidence is insufficient.

Never invent a remaining balance.

## Default request behaviour

- Prefer small named lists.
- Use the shortest useful period.
- Request only necessary metrics.
- Avoid broad discovery.
- Avoid unnecessary repetition.
- Limit pagination and retries.
- Do not silently expand scope.
- Reuse authorised supplied data where possible.

## Approval tiers

Insert the organisation's approved tier definitions.

If not approved, state:

"Approval thresholds have not been established.
Potentially billable operations require owner review."

## Stop conditions

Stop before execution when:

- Access is unauthorised.
- Required permission is unresolved.
- The request exceeds approved scope.
- Required approval is missing.
- The operation cannot be bounded within the approved limit.
- A known entitlement restriction would be violated.

Stop during execution when:

- The approved limit is reached.
- An entitlement or credit error occurs.
- An unexpected billing pattern appears.
- A request unexpectedly expands in scope.
- The vendor reports that access is restricted.

Do not switch routes to bypass restrictions.

## After execution

Report:

- What was requested
- What was retrieved
- Estimated consumption
- Actual consumption, if observable
- Remaining allowance, if observable
- Errors or partial results
- Any follow-up required

Never describe estimated usage as actual usage.

## Data handling

Insert the platform-specific rules on:

- Storage
- Retention
- Sharing
- Redistribution
- External processing
- Licensed outputs

If a relevant permission is unknown, request review.

## Enforcement limitations

These instructions are behavioural safeguards.

They do not create a technical spending cap.

Only describe a restriction as technically enforced when
the underlying connector, API or administrative system
provides and verifies that control.

---

## Deliverable C: Project-instruction snippet

Suggested filename:

`PLATFORM-project-instructions.md`

Write five to six short lines suitable for the relevant
Claude project instructions.

Example:

"When using PLATFORM, read the PLATFORM usage rules file
before retrieving data.

Estimate potentially billable usage before every pull.

Default to small named lists, minimal metrics and short
date ranges.

Follow the documented approval tiers and never expand
scope without permission.

Stop on unknown permissions, entitlement errors or
unapproved consumption.

Report estimated and actual usage separately."

Adapt the wording to the specific platform.

Do not claim Claude can enforce a limit unless a verified
technical mechanism exists.

---

## Deliverable D: Slack announcement

Suggested filename:

`PLATFORM-slack-announcement.md`

Maximum approximately 150 words.

Write for a busy team.

### If the platform is live

Include:

- What has been prepared
- Why it matters
- Where the rules live
- What users must do differently
- Who owns approvals or questions
- One request for feedback

Mention a cost contrast only when supported by evidence.

Exclude confidential pricing and contract details by default.

### If the platform is not live

Explain:

- The integration is not active yet
- Why usage guardrails matter
- What has been prepared
- What remains unknown
- What needs to happen before a trial or launch

Do not imply that a connector has been activated.

### Sending rules

Draft the announcement.

Do not send or post it without explicit authorisation.

Never describe an unsent draft as an announcement already
made to the team.
