---
description: Build or optimize a resume tailored to a specific target role
argument-hint: [client-name] [job-target-slug (optional)]
allowed-tools: [Task, Read, Write, Edit, Glob]
---

You are building a tailored resume for a Career Architect client.

## Pre-Flight (Stop-the-Line if missing)

Verify all prerequisites:

1. Client profile: `client-profiles/{client-name}-profile.md` — REQUIRED
2. Skills inventory: `client-profiles/{client-name}-skills.md` — REQUIRED
3. Keyword brief: `job-targets/{job-slug}-keywords.md` — REQUIRED

If any are missing:
- Profile missing → Run `/consult {client-name}` first
- Skills missing → Run `/skill-inventory {client-name}` first
- Keywords missing → Run `/analyze-job {client-name}` first

Check for existing resume: `client-profiles/{client-name}-existing-resume.*`

## Execution

### Phase 1: Resume Architect

1. Load all intelligence files
2. Select appropriate resume structure (chronological / hybrid / executive)
3. Build section by section:
   - Header
   - Professional Summary (placeholder — Narrative Crafter will polish)
   - Core Competencies
   - Work Experience (STAR-CAR accomplishments)
   - Education
   - Certifications (if applicable)
4. Apply ATS compliance checklist
5. Enforce length guidelines

Save draft to: `resume-outputs/{client-name}-{job-slug}-resume.md`

### Phase 2: Narrative Crafter

1. Polish the Professional Summary
2. Write a tailored Cover Letter
3. Write LinkedIn About section (first time only, or update if needed)

### Phase 3: QA Reviewer

1. Run full QA checklist
2. Validate keyword coverage
3. Check accomplishment quality
4. Flag any issues with routing instructions

## Output Files

- `resume-outputs/{client-name}-{job-slug}-resume.md`
- `resume-outputs/{client-name}-{job-slug}-cover-letter.md`
- `resume-outputs/{client-name}-linkedin-about.md`
- `resume-outputs/{client-name}-{job-slug}-qa-report.md`

## Success Criteria

- [ ] All Tier 1 keywords present
- [ ] 60%+ of experience bullets are quantified
- [ ] No ATS anti-patterns
- [ ] QA report shows APPROVED status
- [ ] All output files saved

## Delivery to Client

Present the resume with a brief explanation of key decisions made:
- Why this structure was chosen
- What keywords were prioritized and why
- What accomplishments were reframed and how
- Any gaps flagged and how they were handled
