---
description: Critically review an existing resume and provide actionable improvement feedback
argument-hint: [resume-filename (optional)]
allowed-tools: [Read, Write, Edit, Glob]
---

You are reviewing an existing resume for a Career Architect user.

## Pre-Flight

1. Locate the resume:
   - Check `profile/` for `existing-resume.*`
   - Check `resume-outputs/` for any existing drafts
   - If not found, ask user to share their resume content

2. Load context if available:
   - `profile/profile.md`
   - `job-targets/` for any target job postings

## Execution

Perform a full critical analysis:

### Structure Analysis
- Is the format appropriate for their experience level and target role?
- Are sections in optimal order?
- Is length appropriate?
- ATS compliance issues?

### Content Analysis
- Professional summary: compelling or cliché?
- Accomplishments vs. responsibilities: are bullets duty-focused or impact-focused?
- Quantification: what percentage of bullets have measurable results?
- Keyword density: relevant to target roles?

### Common Resume Killers to Flag
- "Responsible for..." bullet openers
- Objective statements (outdated)
- References available upon request (outdated)
- Personal pronouns ("I managed...")
- Photos or graphics
- Functional format (usually ATS-unfriendly)
- Full home address
- Missing URLs (LinkedIn, portfolio)
- Unexplained gaps without any framing

## Output

Provide a structured critique report — be direct but constructive. For every weakness identified, provide a specific fix or example rewrite.

Format:
```markdown
# Resume Review: [Your Name]

## Overall Assessment
[1 paragraph honest summary — strengths and key issues]

## Critical Issues (Must Fix)
1. [Issue] → [How to fix]

## High-Impact Improvements
1. [Issue] → [How to fix with example]

## Quick Wins
-

## Sample Bullet Rewrites
Original: [bullet]
Rewritten: [improved bullet]

## Recommendation
[ ] Ready for targeted optimization → Run `/build-resume`
[ ] Needs significant rebuild → Run `/build-resume` with fresh approach
```

## Next Steps

> "Review complete. Recommended next:
> `/build-resume` — Build an optimized version targeting a specific role"
