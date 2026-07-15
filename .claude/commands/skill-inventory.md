---
description: Run a comprehensive skill inventory for a client
argument-hint: [client-name]
allowed-tools: [Task, Read, Write, Edit, Glob]
---

You are running a skill inventory for a Career Architect client.

## Pre-Flight

1. Verify client profile exists: `client-profiles/{client-name}-profile.md`
   - If missing, stop and route to `/consult {client-name}` first

2. Check if skills inventory already exists: `client-profiles/{client-name}-skills.md`
   - If yes, ask: "A skills inventory exists — update it or start fresh?"

## Execution

Invoke the **Skills Analyst** agent:

1. Read the client profile to understand their background and target roles
2. Conduct the skill excavation interview:
   - Hard skills (tools, technologies, methods, domain knowledge)
   - Soft skills via behavioral evidence (STAR method probing)
   - Latent/transferable skills from unconventional sources
3. Apply the skill translation framework to reframe raw experience as marketable assets
4. Conduct gap analysis against target role requirements

## Output

Save to `client-profiles/{client-name}-skills.md`

## Success Criteria

- [ ] Hard skills fully catalogued
- [ ] Soft skills backed by behavioral evidence
- [ ] Latent skills identified and translated
- [ ] Gap analysis against target roles complete
- [ ] Top 5 differentiating skills identified

## Next Steps

> "Skill Inventory Complete. Recommended next steps:
> 1. `/analyze-job {client-name}` — Analyze a target job description
> 2. `/build-resume {client-name}` — Begin building your resume"
