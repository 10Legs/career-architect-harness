---
description: Kick off interview preparation for a client — builds a custom prep plan, STAR story bank, mock interviews, and delivery coaching
argument-hint: [client-name] [job-slug (optional)]
allowed-tools: [Task, Read, Write, Edit, Glob]
---

You are kicking off interview preparation for a Career Architect client.

## Pre-Flight

1. Verify client profile: `client-profiles/{client-name}-profile.md`
   - If missing, halt: "Please run `/consult {client-name}` first to create a client profile."

2. Load the job analysis brief from `job-targets/`:
   - If a job-slug was provided, read: `job-targets/{job-slug}-keywords.md`
   - If no job-slug was provided, scan `job-targets/` for any keyword briefs associated with this client and use the most recent one
   - If no brief exists at all, prompt: "No job analysis found — run `/analyze-job {client-name}` first, then rerun this command."
   - **Pass the full contents of the keyword brief to the Interview Strategist.** The agent must not ask questions that this file already answers (company, role title, level, requirements, keyword tiers, gap analysis).

3. Check for an existing interview prep file: `client-profiles/{client-name}-interview-prep.md`
   - If it exists, ask: "An interview prep session already exists for this client — continue where we left off or start fresh?"

## Execution

Invoke the **Interview Strategist** agent to run the full session:

1. **Intake** — The client profile and job analysis brief are pre-loaded. Do not re-ask anything already answered by those files. Only confirm details that are genuinely unknown:
   - Interview stage (phone screen / behavioral panel / technical / case / final round) — if not in the profile
   - Interview date and timeline urgency — if not in the profile
   - Format specifics if known (number of rounds, interviewer roles, known question types)

2. **Risk Assessment** — Immediately identify the client's top 3 preparation risks based on their profile:
   - Resume gaps or weak spots likely to be probed
   - Technical skill areas that need shoring up
   - Behavioral themes that may be challenging given their background

3. **Custom Prep Plan** — Generate a tailored daily plan based on timeline:
   - **≤ 3 days**: Emergency triage — prioritize highest-probability question types only
   - **1 week**: Focused plan covering behavioral, role-specific, and one full mock
   - **2+ weeks**: Full plan across all modules with progressive mock difficulty

4. **STAR Story Bank** — Build or populate `client-profiles/{client-name}-interview-prep.md` with:
   - 8–10 reusable stories anchored in the client's actual experience
   - Each story tagged to the behavioral themes it covers
   - Quantified results wherever possible

5. **Mock Interview** — Run at least one timed mock during this session:
   - Select question type based on the client's highest-risk area
   - Score response across: Content, Structure, Specificity, Quantification, Delivery
   - Provide actionable feedback and an improved model answer

6. **Company Research Brief** — If target company is known, generate:
   - Key things to know (recent news, culture, leadership principles)
   - Recommended questions the client should ask the interviewer

## Output

Save all prep materials to: `client-profiles/{client-name}-interview-prep.md`

Include:
- Interview details (company, role, date, stage)
- Risk assessment
- Prep plan with daily tasks
- STAR story bank
- Mock interview scores and feedback
- Action items before the interview

## Success Criteria

- [ ] Interview details confirmed (company, role, date, stage)
- [ ] Top risks identified and addressed in the prep plan
- [ ] STAR story bank started with at least 5 stories
- [ ] At least one mock interview completed with scored feedback
- [ ] Action items defined with clear ownership

## Next Steps

After the session, recommend:
> "Your interview prep foundation is set. Next:
> 1. Practice your STAR stories out loud — 3x each today
> 2. Run `/interview-prep {client-name}` again for another mock round
> 3. Research your interviewer on LinkedIn the night before
> 4. Prepare 3–5 smart questions to ask at the close"
