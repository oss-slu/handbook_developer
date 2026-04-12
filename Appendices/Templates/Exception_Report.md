# Exception Report Template

An exception report is not a punishment or a form to fill out. It's a professional communication tool for making your reasoning visible when something deviates from plan. The structure below helps you think clearly about what happened and why. The sections that matter most depend on the situation. A brief process adaptation might need only a summary, context, and reasoning. A significant deadline miss benefits from the full structure. Focus on honesty and clarity over length.

See [Chapter 7](../../Chapters/07-Program_Requirements.md) for context on when and why exception reports are filed.

```markdown
## Summary
[One sentence: what varied and when.]

## Context
[What was the expectation? What actually happened? Be specific.]

## Evidence
[Concrete artifacts that corroborate your account. Link to commit history,
PR timelines, Slack threads, work logs. "I was working on it" is a claim.
Your commit history is evidence.]

## Reasoning
[Walk through the sequence of events and decisions that led to the variation.]

## Alternatives Considered
[What other options were available? Why were they not selected?]

## Impact
[What was affected? Your team's sprint, someone else's code review schedule,
the deliverable? What was done to mitigate?]

## Going Forward
[For deadline misses: what concrete changes will prevent recurrence?
For process adaptations: what did you learn? Would you make the same choice again?]
```

## Guidance

- **Submit proactively when possible.** A report filed before the deadline passes carries more weight than one filed after the fact.
- **Be concrete about changes.** "I'll start earlier" is not a plan. "I'll raise a draft PR by Thursday even if the implementation is incomplete, so my Tech Lead has visibility" is a plan.
- **Evidence matters.** Link to commit history, Slack messages, and PR timelines. Claims without artifacts are hard to evaluate.
- **Reasoning, not rationalization.** Reasoning works forward from evidence to conclusion. Rationalization works backward from a desired conclusion to cherry-picked justification. A useful test: could a skeptical peer follow your evidence to the same conclusion?
