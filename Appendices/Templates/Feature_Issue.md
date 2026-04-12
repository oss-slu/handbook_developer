# Feature Issue Template

The goal of an issue is to give the next developer enough context to do the work well. This template helps you think through what that context looks like. Not every section will apply to every issue. A small, well-scoped task might need only a description and acceptance criteria. A complex feature might benefit from all of it. Use your judgment about what adds value.

```markdown
## Description

**As a** [type of user], **I need** [capability], **so that** [benefit/value].

## Acceptance Criteria

- [ ] [Boolean statement about the desired end-state]
- [ ] [Boolean statement about the desired end-state]
- [ ] [Boolean statement about the desired end-state]

## Developer Notes

### Context
[Why are we doing this? What problem does it solve?]

### Technical Approach
[Suggested implementation approach, relevant code areas, dependencies]

### Testing Considerations
[What should be tested? Edge cases? Integration points?]

### Related Issues
- Related to #[issue number]
- Blocked by #[issue number]
```

## Guidance

- **Acceptance criteria are key.** Each one should be unambiguously true or false when the work is done.
- **Watch for conjunctions.** "User can create and edit profiles" might be two issues, not one.
- **Developer notes add context.** Help the person who picks up this issue understand the landscape without having to reverse-engineer it from the codebase.
- **Label appropriately.** Use labels like `enhancement`, `good first issue`, etc. to help people find relevant work.
