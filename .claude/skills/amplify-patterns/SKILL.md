---
name: amplify-patterns
description: Frameworks for mapping a job's tasks to AI leverage opportunities — task taxonomy, automate/augment/human-core classification, impact-effort prioritization, measurement, and governance guardrails. Invoke when building an AI leverage plan for the user's current role.
allowed-tools: Read, Glob
---

# Amplify Patterns Skill

## The Amplification Principle

AI leverage is not about tools — it's about tasks. Start from what the job actually requires, classify each task by how AI can help, and measure the gain. A person who reclaims 8 hours a week and redirects them to high-visibility work outperforms a person who knows every AI tool.

> Task Inventory + Right Classification + Measured Wins = Compounding Career Capital

## Task Taxonomy — What AI Does Well

| Task Type | Examples in a Job | AI Fit |
|-----------|-------------------|--------|
| **Drafting** | Emails, reports, proposals, documentation, job posts | Excellent — human edits, never sends raw |
| **Summarizing** | Meeting notes, long threads, research papers, call transcripts | Excellent |
| **Extracting** | Pulling data from documents, structuring messy inputs | Excellent |
| **Classifying** | Triaging tickets, tagging feedback, sorting inbound | Excellent |
| **Researching** | Market scans, competitor analysis, prior-art searches | Strong — verify sources |
| **Transforming** | Reformatting, translating, converting between formats/tones | Excellent |
| **Analyzing** | Spotting patterns in data, first-pass analysis, scenario modeling | Strong — human validates |
| **Coding/Scripting** | Automation scripts, spreadsheet formulas, report pipelines | Excellent — even for non-engineers |
| **Brainstorming** | Options, edge cases, counterarguments, names | Strong — human curates |
| **Reviewing** | Proofreading, checklist compliance, consistency checks | Strong — second reader, not final gate |

## Classification Rubric: Automate / Augment / Human-Core

**Automate** (AI does most; human reviews):
- Output is verifiable at a glance
- Task is repetitive with stable structure
- Errors are cheap to catch and fix
- Examples: status report drafts, meeting summaries, data reformatting

**Augment** (AI accelerates; human drives):
- Requires context AI doesn't have
- Output quality depends on judgment
- Errors are costly but reviewable
- Examples: analysis, strategy docs, complex client communications, code

**Human-Core** (AI stays out — protect and expand these):
- Relationship-based: trust built face-to-face, managing up, mentoring
- Accountability-based: decisions someone must own, sign-offs
- Presence-based: negotiations, sensitive conversations, leadership moments
- **These are the promotion case.** The point of automating the rest is to spend MORE time here.

## Impact × Effort Prioritization

| | Low Effort | High Effort |
|---|-----------|-------------|
| **High Impact** | Quick wins — do this week | Quarter plays — schedule deliberately |
| **Low Impact** | Fill-ins — batch when convenient | Skip — revisit next quarter |

Score impact by: hours/week reclaimed × visibility of the work it frees you for.
Score effort by: learning curve + setup time + approval friction.

## Common AI Plays by Job Function

| Function | Highest-Yield Plays |
|----------|--------------------|
| Management | Meeting summaries → action items; 1:1 prep briefs; draft performance feedback (human personalizes) |
| Sales / CS | Call summaries + CRM entry; personalized outreach drafts; objection-handling prep |
| Marketing | Content first drafts; campaign variant generation; audience research synthesis |
| Finance / Ops | Spreadsheet formula + script generation; variance narrative drafts; process documentation |
| Engineering | Code generation/review; test writing; documentation; incident summaries |
| HR / Recruiting | JD drafts; screening rubrics; interview question banks; policy doc first drafts |
| Analysts | First-pass exploration; chart narration; report automation pipelines |
| Legal / Compliance | Clause comparison; policy summarization; first-pass contract review (verify everything) |

## Prompt Patterns for Work Tasks

- **Role + context + task + format + constraint**: "You are reviewing a vendor contract for a mid-size SaaS company. Summarize payment terms, auto-renewal clauses, and liability caps in a table. Flag anything unusual."
- **Few-shot from your own best work**: paste 2 examples of your best output, ask AI to match the pattern for the new case
- **Draft-then-critique**: generate a draft, then ask AI to attack it ("What would a skeptical VP push back on?")
- **Extraction schema**: define the exact fields you want before feeding messy input

## Measurement Framework

Every play needs a baseline BEFORE starting:

1. **Time**: hours/week on the task now → after (time reclaimed)
2. **Volume**: output per week now → after
3. **Quality**: error rate, review cycles, stakeholder feedback
4. **Redirection**: what the reclaimed time went to (this is the career story)

**Resume bullet formula for AI wins**:
```
[Action verb] + [AI-assisted workflow] + [task] + [measured gain] + [what the freed capacity enabled]

"Built AI-assisted reporting workflow that cut weekly status prep from 6 hours to 45 minutes,
redirecting capacity to client strategy work that grew account revenue 18%"
```

## Positioning Patterns — Becoming the AI Multiplier

- **Pilot + document + share**: run one measured win, write it up, present it — one page with numbers beats opinions
- **Lunch-and-learn**: teach one play to the team; teaching = visibility = ownership of the topic
- **Process documentation**: write the team playbook for a sanctioned tool; author = authority
- **Champion role**: volunteer for AI tool evaluations or governance committees — early access + leadership exposure
- Frame everything as capacity, not headcount: "this frees us for X," never "this replaces Y"

## Governance Guardrails (Non-Negotiable)

1. **Policy first**: know the company AI policy before any play touches company data; unknown policy = ask, don't assume
2. **Data classification**: customer PII, financials, trade secrets, regulated data NEVER enter unsanctioned tools; anonymize or use approved enterprise tools
3. **Verify before it ships**: AI output is a draft until a human validates it; the user owns every error regardless of source
4. **Disclosure where required**: regulated professions, academic work, and some client contracts require disclosing AI assistance
5. **Skill retention**: automate the task, keep the skill — periodically do it manually to stay sharp enough to catch AI mistakes
