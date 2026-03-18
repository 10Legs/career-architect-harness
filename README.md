# Career Architect Harness

A multi-agent AI harness built for **Claude Code CLI** and **Gemini CLI** that transforms job seekers' skills and experiences into compelling career narratives. The harness orchestrates a team of specialized agents, each owning a discrete step in the resume and career strategy workflow.

---

## How It Works

The harness is a collection of AI primitives — **agents**, **commands/workflows**, and **skills** — wired together into a structured workflow. 

- **Claude Code CLI**: Uses `CLAUDE.md` and slash commands in `.claude/commands/`.
- **Gemini CLI**: Uses `GEMINI.md` and follows the operational workflows described therein.

Both tools activate the same specialist agents, which draw on domain-skill knowledge to produce specific output files. Each step gates the next.

```
/consult → /skill-inventory → /analyze-job → /build-resume → /career-strategy
```

### Agents

Specialist sub-agents live in `.claude/agents/`. Each agent has a defined role, model capability requirement, and an exit state it must reach before the next agent proceeds.

| Agent | Role | Exit State |
|-------|------|------------|
| Intake Consultant | Initial consultation, client profile creation | Client Profile Complete |
| Skills Analyst | Skill inventory, transferable skill mapping | Skill Inventory Complete |
| Keyword Researcher | Job description analysis, keyword extraction | Keywords Extracted |
| Resume Architect | Resume construction, ATS optimization | Draft Ready for Review |
| Narrative Crafter | Professional summary, cover letter, LinkedIn About | Narrative Complete |
| QA Reviewer | Final quality gate before delivery | Approved for Delivery |
| Career Strategist | Job search strategy, networking, salary guidance | Strategy Delivered |

### Commands

Slash commands in `.claude/commands/` trigger the appropriate agent and enforce pre-flight checks. If prerequisites are missing, the command halts and routes you to the correct prior step.

| Command | What It Does |
|---------|-------------|
| `/consult [client-name]` | Start a new engagement — intake interview, saves client profile |
| `/skill-inventory [client-name]` | Run a full skill inventory against the client profile |
| `/analyze-job [client-name]` | Paste or load a job description — extracts ATS keywords and requirements |
| `/build-resume [client-name] [job-slug]` | Build a tailored resume, cover letter, and LinkedIn About section |
| `/review-resume [client-name]` | Critically review an existing resume with actionable feedback |
| `/career-strategy [client-name]` | Build a job search action plan, networking strategy, and salary approach |

### Skills

Domain expertise modules in `.claude/skills/` are loaded automatically by agents as needed. They are not invoked directly by users.

| Skill | Purpose |
|-------|---------|
| `ats-optimization` | ATS formatting rules, keyword placement, anti-patterns to avoid |
| `resume-patterns` | Bullet formulas, section templates, accomplishment framing |
| `skill-translation` | Latent and transferable skill identification frameworks |
| `career-strategy-patterns` | Job search tactics, networking scripts, salary negotiation |
| `interview-prep` | STAR story coaching, behavioral question banks |
| `linkedin-optimization` | Profile keyword ranking, recruiter visibility strategies |

---

## Repository Structure

```
.claude/
├── agents/               # Specialist agent definitions
├── commands/             # Slash command workflows
├── skills/               # Domain expertise modules
├── team-config.json      # Agent roster and workflow config
client-profiles/          # Created per client — profiles, skill inventories
job-targets/              # Saved job descriptions and keyword briefs
resume-outputs/           # Final resume drafts, cover letters, QA reports
patterns_library/         # Reusable resume patterns and templates
CLAUDE.md                 # Team philosophy, workflow rules, stop-the-line conditions
```

---

## Quickstart

### New Client, Full Workflow

```
/consult Jane Smith
```
Follow the intake interview. A profile is saved to `client-profiles/jane-smith-profile.md`.

```
/skill-inventory jane-smith
```
The Skills Analyst maps Jane's full skill set, including transferable and latent skills.

```
/analyze-job jane-smith
```
Paste a job description when prompted. A keyword brief is saved to `job-targets/`.

```
/build-resume jane-smith <job-slug>
```
The Resume Architect, Narrative Crafter, and QA Reviewer run in sequence. Output files are saved to `resume-outputs/`.

```
/career-strategy jane-smith
```
The Career Strategist builds a job search action plan.

### Review an Existing Resume

```
/review-resume jane-smith
```
Upload or paste the resume. The QA Reviewer delivers structured feedback.

---

## Stop-the-Line Rules

Any agent will halt work and route back if:

- **Client goals are undefined** — return to `/consult`
- **No target job description** — required before `/analyze-job` can run
- **Skill inventory incomplete** — `/skill-inventory` must complete before `/build-resume`
- **Fabricated credentials detected** — work stops immediately, client is notified

---

## Output Files

For each client + target role, the harness produces:

| File | Contents |
|------|----------|
| `client-profiles/{name}-profile.md` | Career goals, background, target roles |
| `client-profiles/{name}-skills.md` | Full skill inventory |
| `job-targets/{slug}-keywords.md` | Extracted keywords, Tier 1/2/3 classification |
| `resume-outputs/{name}-{slug}-resume.md` | ATS-optimized tailored resume |
| `resume-outputs/{name}-{slug}-cover-letter.md` | Targeted cover letter |
| `resume-outputs/{name}-linkedin-about.md` | LinkedIn About section |
| `resume-outputs/{name}-{slug}-qa-report.md` | QA review with APPROVED/REVISION status |

---

## Ethics

- No fabricated accomplishments, credentials, employers, or dates
- All client data treated as confidential
- Embellished content is flagged, not silently accepted
- Every recommendation is grounded in the client's actual experience and the job's real requirements
