# Platform Usage Guardrails

**Brought to you by [Danee Co](https://www.linkedin.com/in/daneechavez), creative operations and AI enablement consultant.**

A Claude skill for the moment you connect a paid data platform to Claude and nobody knows what it will cost, who is allowed to pull what, or what the licence actually permits.

It started with a custom connector (MCP) that let Claude read a client team's sales data. Connecting was the easy part. Knowing what each request consumes, and who should approve it, was not written down anywhere.

## What it does

It researches how the platform bills, what its limits are, and what the licence says about storing and processing data. It labels every fact by how much you can trust it, builds the usage model, sets the approval rules, and drafts everything your team needs to follow them.

It researches and drafts policy. It does not certify contractual compliance, and it does not technically enforce spending limits.

## When it runs

Platform onboarding, API or MCP connections, credit or cost estimates, usage policies, and team guidance for any paid data platform you are connecting to Claude (think Similarweb, FactSet, Placer.ai or another licensed data provider).

## What you get

- **Team guide:** a one-minute summary, readiness status, what the platform charges for, safe defaults, approval process, data restrictions, open vendor questions.
- **Claude-facing rules:** approved access paths, a pre-pull estimate template, request limits, approval tiers, stop conditions, retry and pagination rules.
- **Project instructions:** a short snippet that points to the rules.
- **Slack announcement:** a draft only. Nothing is sent without your say-so.

## Principles

- **Evidence labels:** every fact is QUOTED, PUBLISHED, DERIVED or UNKNOWN. An unknown never gets turned into a guess.
- **Readiness statuses:** each access path is CLEARED FOR CONTROLLED USE, DRAFT ONLY or NOT CLEARED FOR LIVE USE.
- **Estimate before you pull:** Claude shows the expected requests, units, cost and remaining allowance, and asks for approval where your policy says to.
- **Behavioural vs enforced:** the skill says which controls are just instructions and which are technically enforced.
- **Protect the data:** confidential pricing, contract terms and licensed data stay out of public outputs.
- **Lighter mode:** when most facts are unknown, it produces a guide with clear gaps and a vendor question list instead of a complete-looking guess.

## Before you roll it out

The skill includes eight test scenarios in `references/acceptance-tests.md`. Run them on your own platforms before trusting it with a team.

## Install

Drop the `platform-usage-guardrails-v4/` folder (containing `SKILL.md` and `references/`) into your Claude skills directory. In Claude Cowork or Claude.ai with skills enabled, it loads automatically and fires on the situations above.

## License

MIT

---

Built by Danee Co. If this saved you time, tell me what landed: https://www.linkedin.com/in/daneechavez
