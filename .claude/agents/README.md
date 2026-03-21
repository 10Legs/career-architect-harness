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
| Interview Strategist | `interview-strategist.md` | `/interview-prep` — interview preparation, mock interviews, delivery coaching |

## Model Capability Requirements

Agents specify model requirements as capability descriptions rather than specific model IDs. This allows any capable AI to be matched appropriately:

- **Conversational/Fast** (Intake, Skills Analyst, Keyword Researcher): Optimized for interactive dialogue and structured output
- **High-Capability** (Resume Architect, Narrative Crafter): Deep reasoning, strong writing, nuanced judgment
- **Analytical/Precise** (QA Reviewer): Strong attention to detail, pattern recognition, high accuracy
- **Broad Knowledge** (Career Strategist, Interview Strategist): Wide industry expertise, strategic reasoning, human psychology, communication coaching

## Workflow Gates

Work MUST stop if:
1. Client profile missing → run `/consult` first
2. Skills inventory missing → run `/skill-inventory` first
3. No keyword brief for target role → run `/analyze-job` first
4. Fabricated content detected → halt and flag to client
