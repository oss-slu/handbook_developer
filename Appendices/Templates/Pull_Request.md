# Pull Request Template

A PR description serves two audiences: the reviewer who needs to understand your changes right now, and the future developer who will read the git history wondering why this change was made. This template helps you think about both. The most valuable section is the rationale. Code shows *what* you did. The description captures *why*. If a section doesn't apply (e.g., no manual testing steps for a documentation-only change), drop it rather than filling it with boilerplate.

Your project may have a `.github/PULL_REQUEST_TEMPLATE.md` that pre-populates this. If not, consider adding one.

```markdown
## Related Issue

Closes #[issue number]

## Description

[Concise description of what was done and why.]

## Changes Made

- [Category of change, e.g., "Added date filtering to search endpoint"]
- [Category of change, e.g., "Updated API documentation"]

## Rationale

**Problem:**
[What problem were you solving?]

**Approach:**
[Why this approach over alternatives? What tradeoffs did you consider?]

## Acceptance Criteria

[Copy from original issue and check off]

- [ ] [AC from issue]
- [ ] [AC from issue]
- [ ] [AC from issue]

## Testing

**Tests Added:**
- [Test description]

**Manual Testing:**
1. [Step to verify]
2. [Expected result]

## Checklist

- [ ] Code follows project style guidelines
- [ ] Self-review completed
- [ ] Documentation updated if behavior changed
- [ ] Tests added/updated and passing
- [ ] No new warnings or errors

## Reviewer Notes

[Areas where you want extra feedback, known limitations, or things you're uncertain about]
```

## Guidance

- **The "why" is critical.** Code shows what you did. The PR description explains why. Why this approach over alternatives? Why these tradeoffs?
- **Link to the issue.** Use `Closes #123` to auto-close the issue when the PR merges.
- **Copy acceptance criteria from the issue.** This makes it clear when the work is complete and keeps the PR aligned with the original requirements.
- **Self-review first.** Read your own diff before requesting review. You'll catch obvious issues and save your reviewer's time.
- **Keep PRs focused.** One purpose per PR. If you find yourself writing "also" in the description, consider splitting it.
