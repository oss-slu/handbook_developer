# 10. Open Source Logistics and Operations for Student Teams

**Scope:** Operational standards for planning, coordination, measurement, and continuity on student open-source teams. Academic calendars, rotating membership, and external stakeholders make implicit process brittle; this chapter defines explicit practices that keep repositories and knowledge usable across cohorts. It applies to all Open Source with SLU projects and supplements workflow detail in other chapters.

## 1. Purpose

Operational planning ties delivery to observable outcomes and to a codebase the next team can run and extend.

- **Calendar pressure:** Exams, breaks, and course deadlines shrink and shift engineering time. Work planned without capacity data stalls or ships under pressure.
- **Temporary ownership:** Contributors and stakeholder availability change. Reliance on unwritten knowledge fails at handoff.
- **Long-lived artifacts:** Issues and documentation outlast any sprint. Operations make prior work legible instead of re-derived each term.
- **Stakeholder predictability:** Clear plans and accurate status reduce churn and preserve trust with clients, faculty, Tech Leads, and upstreams.

Logistics do not replace engineering judgment; they reduce avoidable disruption.

## 2. Core Principles

| Principle | In practice |
| --- | --- |
| **Consistency** | Planning, status (sync or async), and reviews use stable formats and timeboxes so risks surface on a fixed rhythm. |
| **Transparency** | Status, decisions, and blockers live in the issue tracker, PRs, and agreed channels—not only in meetings. |
| **Sustainability** | Commitments match capacity; scope moves before quality or people burn out. |
| **Accountability** | Every issue has an owner; the team owns dates collectively, with named contacts for outward-facing topics. |
| **Documentation-first collaboration** | Behavior, architecture, and onboarding decisions are written where the next contributor looks (README, contributing guide, ADRs, or linked issue threads). |

Revisit these defaults in retrospectives; treat them as operating constraints, not slogans.

## 3. Sprint and Capacity Planning

### Estimating realistic capacity

Base plans on time available after classes, labs, jobs, and other obligations.

- **Sizing:** Align with existing issue practice (points or t-shirt sizes), or estimate in half-day or day blocks if points are unused.
- **Focus factor:** Assume a fraction of nominal hours (e.g. 60–70%) becomes deep work; the rest goes to review, meetings, context switching, and academic surprises.
- **Visible calendar:** Record exams, travel, and known absences on the team calendar or board so planners see the same constraints.

### Planning sprint goals

Goals are **outcome-based** and **limited**—typically one primary outcome and at most one secondary. Map each goal to a small set of issues with acceptance criteria and explicit order where dependencies exist.

- **Committed work:** Finish and merge within the sprint window.
- **Stretch work:** Non-blocking; pull only when committed work is on track.

### Avoiding overcommitment

Overcommitment raises defects and erodes stakeholder trust.

- Cap WIP per person and per workstream.
- Run **dependency checks** before sprint commit (APIs, credentials, design sign-off, upstream releases).
- Reserve **buffer** for review, integration, and rework when multiple people touch one subsystem.

### Academic schedules

- **Front-load discovery** when exam load may be lighter relative to onboarding cost.
- **Reserve end-of-semester capacity** for stabilization, documentation, and handoff—not sustained feature velocity through finals.
- **Align sprints** to blackout periods (midterms, heavy weeks in other courses) via reduced scope or maintenance-only iterations when agreed.

## 4. Risk Management

**Definition:** Identify threats to schedule, quality, or continuity early; record owners and mitigations while options remain.

### Common risks

| Risk | Indicators | Mitigations |
| --- | --- | --- |
| **Unclear ownership** | Unassigned issues; assumed handoffs on dependencies | One **driver** per issue or stream; sub-issues/checklists for shared work; escalate in weekly ops |
| **Blocked work** | Waits on credentials, legal sign-off, or third parties | Time-box waiting; escalate to Tech Lead; document in the issue; parallel work where possible |
| **Technical debt** | Regressions; slow reviews; hesitation to change hot modules | Recurring refactor capacity; labeled debt issues; pair on high-risk edits |
| **Missing documentation** | Repeated onboarding questions; knowledge only in chat | Section 7; include doc updates in definition of done when behavior changes |
| **Stakeholder delays** | Feedback longer than a sprint; shifting requirements off-thread | Feedback SLAs where feasible; written decision summaries; smaller batches awaiting approval |
| **Handoff gaps** | No runbooks; env-only secrets; roadmap only in notes | Section 8; handoff readiness template (Section 10) |

### Operating rhythm for risks

Maintain a **living risk register** (Section 10), reviewed at least **biweekly**; surface critical items in stakeholder updates. Each risk is **specific**, **owned**, and **time-bound** where mitigation is expected.

## 5. Stakeholder Communication

Separate signal from noise; leave a written trail aligned to work items.

### Clients and domain stakeholders

- **Channels:** Email for formal decisions; demos for feedback; issue comments for scoped, work-linked questions.
- **Post-demo notes:** Shipped, in-flight, decisions needed, and dates by which responses unblock work.
- **Recommendations vs. commitments:** State what the team advises separately from what it will deliver this iteration.

### Faculty advisors and course context

- **Milestone-aligned updates** that connect output to course expectations without excess detail.
- **Early flags** on grading timelines, presentations, or other constraints so sprints absorb them.

### Tech Leads and program technical leadership

- Escalate architecture and quality with **options and tradeoffs**, not open-ended questions.
- Report **capacity and skill gaps** that affect delivery so pairing or staffing can adjust.

### Maintainers and upstream projects

- Follow each repo’s contribution rules; validate approach with drafts or early issues before large PRs.
- Cross-link upstream issues; avoid large surprise changes outside maintainer norms.

### Future contributors

- Treat **oral handoff as insufficient:** build, test, deploy, and extend paths must live in-repo or linked docs.
- Keep a short **start-here** path in the README: setup, architecture pointer, good-first issues.

## 6. Metrics and KPI Tracking

Metrics are **lightweight**, **hard to game**, and **actionable**—for reflection and transparency, not scorekeeping.

### Recommended lightweight metrics

| Metric | Rationale | Source |
| --- | --- | --- |
| **Completed issues** (label / milestone) | Throughput vs. plan | Closed issues in period |
| **PR cycle time** (open → merge) | Review and scope friction | PR timestamps |
| **Review responsiveness** (first review, re-review) | Feedback loop health | PR events; team SLA |
| **Documentation coverage** (doc changes vs. features, or checklist) | Bus factor | Commits under `docs/`; audits |
| **Onboarding readiness** (optional: time to first merge) | Doc and issue quality | Informal timing or survey |
| **Stakeholder feedback** (demo/issue themes) | Product alignment | Sprint notes summary |
| **Unresolved blockers** (count, age) | Systemic impediments | Labels; board columns |

### Using metrics responsibly

- Discuss in **retrospectives** and planning; avoid public leaderboards unless the team opts in.
- Always add **qualitative context** (quality, learning goals, debt accepted).
- **Change the set** tracked when numbers no longer drive decisions.

## 7. Documentation Governance

Documentation is a deliverable. Governance keeps it correct and findable.

### Quality expectations

- **Single source of truth:** One canonical doc per procedure; link from Slack or email instead of duplicating.
- **Version-sensitive detail** (deps, env vars, CLI): colocate with code or under `docs/`; behavior-changing PRs update those docs in the same merge.
- **Architecture notes:** Capture invariants and integration boundaries, not full implementation detail.

### Updating docs alongside code

Include documentation in **definition of done** when:

- User-visible behavior changes.
- Setup, build, or deploy steps change.
- Public APIs or configuration contracts change.

Prefer small, frequent updates over end-of-semester doc sprints.

### Reusability beyond the current team

- Maintain a **docs index** (`docs/README.md` or equivalent): purpose and audience per page.
- Log non-obvious choices with **ADRs** or a short decision log.
- **Retire** obsolete pages with a pointer to replacements; do not leave conflicting instructions live.

## 8. Handoff and Continuity Planning

Handoff makes the repository operable for the next cohort without reconstructing private context.

### Repository health

- Default branch **CI green**; failures understood and owned.
- **Branches** pruned; stale PRs closed or refreshed with current context.
- **Dependencies** pinned or ranged consistently; known vulnerabilities have owner and timeline.
- **No secrets in git**; rotation and access roles documented per project security practice.

### Architecture and operations notes

- **Architecture overview** (diagram or bullets): components, data flows, external systems.
- **Runbooks:** local dev, staging (if any), production-like environments.
- **Operational limits:** rate limits, quotas, cost; who approves changes that affect them.

### Setup and contribution path

- **README:** prerequisites, install, test, lint, common failures.
- **CONTRIBUTING:** branches, PR expectations, review norms, issue workflow.

### Known issues and roadmap

- **Known issues:** labeled, prioritized, workarounds written.
- **Roadmap:** near-term goals, deferred work, dependencies on stakeholders or upstreams.

### Stakeholder context

Document **who** the domain owner is, **what success means**, and **how to demo**—enough for a new Tech Lead to represent the project without informal backstory.

## 9. Operational Checklists

### Sprint planning

- [ ] Capacity updated for the sprint (academic conflicts noted).
- [ ] Sprint goal set and tied to milestone or release theme.
- [ ] Committed issues: owners, acceptance criteria, dependencies recorded.
- [ ] Stretch backlog ordered; WIP limits acknowledged.
- [ ] Risk register reviewed; new risks logged.
- [ ] Stakeholder touchpoints (demo, email) scheduled or assigned.

### Weekly team operations

- [ ] Status (async or sync): on-track / at-risk / blocked, with issue and PR links.
- [ ] Blockers escalated or given owner and next-action date.
- [ ] Stale PRs assigned or pinged per team norms.
- [ ] Documentation gaps from the week filed as issues.
- [ ] Upcoming academic or stakeholder events on the board.

### Risk review

- [ ] Register open; every risk has owner and status.
- [ ] New risks logged with impact/likelihood (or H/M/L).
- [ ] Mitigations advanced or replanned; closed risks noted.
- [ ] Top risks summarized for Tech Lead or stakeholders when needed.

### Stakeholder updates

- [ ] Delivered vs. last update (bullets, links to evidence).
- [ ] Current focus and expected completion window.
- [ ] Decisions or feedback requested, with due dates.
- [ ] Scope/timeline risks stated plainly.
- [ ] Demo, build, or release links attached.

### End-of-semester handoff

- [ ] Handoff readiness template (Section 10) completed.
- [ ] README and CONTRIBUTING verified outside the core feature pair (clean env or fresh machine where possible).
- [ ] Open issues triaged: labels, priority, comments for next owners.
- [ ] Roadmap and known issues current.
- [ ] Access and credentials documented per security norms.
- [ ] Final stakeholder summary sent; sprint notes archived in-repo or agreed store.

## 10. Templates

Copy into wikis, issues, or shared docs; replace bracketed fields.

### Sprint operating plan

```markdown
## Sprint [ID] — [Date range]

### Sprint goal
- Primary:
- Secondary (stretch):

### Capacity snapshot
| Role / stream | Available capacity | Notes (exams, travel) |
| --- | --- | --- |

### Committed deliverables
| Issue | Owner | Dependencies | Definition of done |
| --- | --- | --- | --- |

### Risks to watch
| Risk | Mitigation | Owner |

### Stakeholder touchpoints
| Audience | Format | Date | Owner |

### Links
- Project board:
- Milestone:
```

### Risk register (excerpt layout)

```markdown
## Risk register — [Team / Project] — [Last updated]

| ID | Description | Category | Impact | Likelihood | Owner | Mitigation | Status | Next review |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| R-001 | | ownership / technical / external / continuity | H/M/L | H/M/L | | | open / mitigated / closed | |
```

### Stakeholder update

```markdown
## [Project name] — Stakeholder update — [Date]

### Summary
[2–4 sentences: health, trajectory]

### Shipped since last update
- 

### In progress
- 

### Upcoming (next 2 weeks)
- 

### Decisions / feedback needed
| Topic | Question | Needed by | Link |
| --- | --- | --- | --- |

### Risks
- 

### Appendix
- Demo / build link:
- Milestone link:
```

### Handoff readiness checklist

```markdown
## Handoff readiness — [Project] — [Semester / cohort]

### Repository
- [ ] Default branch green (CI)
- [ ] Dependencies documented and current
- [ ] No committed secrets; access list verified

### Documentation
- [ ] README: setup verified end-to-end
- [ ] CONTRIBUTING: workflow current
- [ ] Architecture overview updated
- [ ] ADRs or decision log current for major choices

### Work management
- [ ] Open issues labeled and prioritized
- [ ] Roadmap reflects realistic next steps
- [ ] Known issues and workarounds documented

### Product / stakeholder context
- [ ] Stakeholder contact and expectations summarized
- [ ] Demo script or recording linked

### Operational
- [ ] Runbooks for deploy / ops (if applicable)
- [ ] Backup / recovery notes (if applicable)

### Sign-off
| Area | Verified by | Date |
| --- | --- | --- |
```
