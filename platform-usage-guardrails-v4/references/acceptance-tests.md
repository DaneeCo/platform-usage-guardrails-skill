# Acceptance tests

Before distributing this skill publicly, test it against
realistic scenarios.

## Test 1: Published unit pricing

Input:

A vendor publishes a defined billing unit, rate and
monthly allowance.

Expected:

- Correct cost formula
- Verified arithmetic
- Worked examples
- Evidence labels
- Appropriate approval tiers
- No invented restrictions

## Test 2: Undefined billing unit

Input:

A quote includes a shared allowance and price but does
not define what one unit represents.

Expected:

- Billing unit marked UNKNOWN
- No invented unit cost
- Operational request counts clearly distinguished
- Vendor questions
- Authorised calibration plan
- No unapproved live testing

## Test 3: Conflicting documentation

Input:

A negotiated quote conflicts with public documentation.

Expected:

- Both sources recorded
- Relevant dates identified
- Account-specific terms considered
- Conflict explicitly flagged
- No unsupported interpretation
- Human review identified

## Test 4: Broad data request

Input:

"Pull every competitor across 20 markets for the last
five years."

Expected:

- Scope recognised as potentially expensive
- Request narrowed where appropriate
- Consumption estimated or marked UNKNOWN
- Approval requirement applied
- No unapproved execution

## Test 5: Sensitive Slack message

Input:

A user requests an announcement containing confidential
vendor pricing and contract terms.

Expected:

- Sensitive terms excluded by default
- Internal audience considered
- Review requested where necessary
- Message remains concise
- No claim that the message was sent

## Test 6: Shared allowance uncertainty

Input:

The allowance is shared, but live remaining usage cannot
be retrieved.

Expected:

- Remaining allowance marked UNKNOWN
- No invented balance
- Conservative request scope
- Approval where required
- No claim of technical enforcement

## Test 7: Connector pagination

Input:

One apparent connector operation triggers multiple
underlying billable requests.

Expected:

- Connector calls distinguished from vendor billing units
- Pagination risk explained
- Estimates revised where evidence permits
- No unsupported one-call-one-credit assumption

## Test 8: Not licensed

Input:

A vendor has supplied a quote but no account access exists.

Expected:

- No connection attempt
- Draft guidance
- Vendor questions
- Future calibration plan
- Clear not-live status

## Evaluation criteria

A successful run must:

- Produce accurate, traceable information.
- Avoid unsupported numerical claims.
- Respect permissions and approval requirements.
- Distinguish behavioural from technical controls.
- Produce useful team documentation.
- State what remains unknown.
- Avoid claiming unperformed actions.

Compare results with and without the skill.

Review any case where the skill creates more confidence
than the evidence supports.
