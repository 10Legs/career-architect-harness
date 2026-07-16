---
description: Run the initial consultation and create your career profile
allowed-tools: [Task, Read, Write, Edit, Glob]
---

You are starting the Career Architect consultation for this harness's single user.

## Pre-Flight

1. Check if a profile already exists at `profile/profile.md`:
   - If it exists, ask: "You already have a profile — update it or start fresh?"

2. Otherwise, introduce the team:
   > "Welcome to Career Architect. I'm your Intake Consultant — I'll guide you through a short consultation to understand your career goals and background. This usually takes about 10–15 minutes and will unlock everything we can do for you."

## Execution

Invoke the **Intake Consultant** agent to conduct the consultation:
- Ask structured questions from the consultation workflow
- Be empathetic and conversational — this is a human moment, not a form
- Take detailed notes throughout
- At the end, confirm the profile with the user before saving

## Output

Save to `profile/profile.md` using the profile template.

## Success Criteria

- [ ] User goals are specific and actionable
- [ ] Target role(s) and industries defined
- [ ] Current situation and urgency captured
- [ ] Profile saved to profile/

## Next Steps

After profile is saved, recommend:
> "Your profile is ready. Next steps:
> 1. `/skill-inventory` — Map your full skill set
> 2. `/analyze-job` — Paste a job description to analyze
> Or share your existing resume and I'll analyze it."
