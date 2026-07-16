---
description: Build or optimize a resume tailored to a specific target role
argument-hint: [job-target-slug (optional)]
allowed-tools: [Task, Read, Write, Edit, Glob]
---

You are building a tailored resume for a Career Architect user.

## Pre-Flight (Stop-the-Line if missing)

Verify all prerequisites:

1. User profile: `profile/profile.md` — REQUIRED
2. Skills inventory: `profile/skills.md` — REQUIRED
3. Keyword brief: `job-targets/{job-slug}-keywords.md` — REQUIRED

If any are missing:
- Profile missing → Run `/consult` first
- Skills missing → Run `/skill-inventory` first
- Keywords missing → Run `/analyze-job` first

Check for existing resume: `profile/existing-resume.*`

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

Save draft to: `resume-outputs/{job-slug}-resume.md`

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

- `resume-outputs/{job-slug}-resume.md`
- `resume-outputs/{job-slug}-cover-letter.md`
- `resume-outputs/linkedin-about.md`
- `resume-outputs/{job-slug}-qa-report.md`

## Success Criteria

- [ ] All Tier 1 keywords present
- [ ] 60%+ of experience bullets are quantified
- [ ] No ATS anti-patterns
- [ ] QA report shows APPROVED status
- [ ] All output files saved

## Delivery to User

Present the resume with a brief explanation of key decisions made:
- Why this structure was chosen
- What keywords were prioritized and why
- What accomplishments were reframed and how
- Any gaps flagged and how they were handled
