# Bug Report Template

A good bug report helps someone fix the problem without having to rediscover it first. This template prompts you to capture the information that matters most: what happened, what should have happened, and how to see it for yourself. Include what's useful. If the bug is obvious and reproducible in one step, you don't need a full environment section. If it only appears under specific conditions, that detail is critical.

```markdown
## Description

**Given** [context/precondition], **when** [action], **then** [unexpected behavior].

## Current Behavior
[What actually happens. Be specific.]

## Expected Behavior
[What should happen instead.]

## Steps to Reproduce
1. [First step]
2. [Second step]
3. [Third step]

## Acceptance Criteria

- [ ] [Bug no longer occurs under the described conditions]
- [ ] [Correct behavior is implemented]
- [ ] [Regression test exists]

## Developer Notes

### Environment
- **OS:** [Operating system and version]
- **Browser:** [If applicable]
- **Version:** [App version, commit hash, or branch]

### Additional Context
[Screenshots, error messages, logs, stack traces]

### Related Issues
- Similar to #[issue number]
```

## Guidance

- **Reproduction steps are essential.** A bug report without steps to reproduce is difficult to act on. Include what you did, what you expected, and what actually happened.
- **Be specific about the environment.** Bugs that only appear on certain operating systems or browser versions are common. The more detail you provide, the faster someone can investigate.
- **Include a regression test in the acceptance criteria.** When the bug is fixed, a test should exist that would catch it if it recurred.
