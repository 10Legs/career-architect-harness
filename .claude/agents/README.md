# Career Architect Agents

## Agent Roster

| Agent | File | Trigger |
|-------|------|---------|
| Intake Consultant | `intake-consultant.md` | `/consult` — start every new client here |
| Skills Analyst | `skills-analyst.md` | `/skill-inventory` — after intake |
| Keyword Researcher | `keyword-researcher.md` | `/analyze-job` — with a job description |
| Resume Architect | `resume-architect.md` | `/build-resume` — after skills + keywords |
| Narrative Crafter | `narrative-crafter.md` | Invoked by Resume Architect automatically |
| QA Reviewer | `qa-reviewer.md` | Final gate before client delivery |
| Career Strategist | `career-strategist.md` | `/career-strategy` — job search planning |
| Interview Strategist | `interview-strategist.md` | `/interview-prep [client-name] [job-slug]` — interview preparation, mock interviews, delivery coaching |

## Model Assignments

Agent frontmatter uses valid Claude Code `model` values (`sonnet`, `opus`, `haiku`, `inherit`). Capability rationale lives as a comment at the top of each agent file.

| Tier | Agents | `model:` | Why |
|------|--------|----------|-----|
| Conversational/Fast | Intake Consultant, Skills Analyst, Keyword Researcher | `sonnet` | Interactive dialogue, structured extraction — speed matters |
| High-Capability | Resume Architect, Narrative Crafter | `inherit` | Deep reasoning, strong writing — runs on the session's best model |
| Analytical/Precise | QA Reviewer | `inherit` | Final gate must never run on a weaker model than the builder |
| Broad Knowledge | Career Strategist, Interview Strategist | `inherit` | Industry expertise, coaching judgment; has WebSearch/WebFetch for live research |

## Workflow Gates

Work MUST stop if:
1. Client profile missing → run `/consult` first
2. Skills inventory missing → run `/skill-inventory` first
3. No keyword brief for target role → run `/analyze-job` first
4. Fabricated content detected → halt and flag to client
