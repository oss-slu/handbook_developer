# Checklists

Quick-reference checklists for common developer tasks, ordered roughly by when you'll encounter them in the lifecycle of a project. Use these as pre-flight checks, not as exhaustive procedures.

## New Developer Onboarding

When you join a project, work through this list during your first week.

- [ ] Clone the repository and follow setup instructions
- [ ] Read the README, contributing guide, and any architecture docs
- [ ] Review the team's Working Agreement
- [ ] Introduce yourself in the project Slack channel
- [ ] Review recent PRs to understand current work and code style
- [ ] Pick up a small issue to get your first PR through the workflow
- [ ] Schedule time with your Tech Lead for project orientation

## Writing a New Issue

When creating or refining issues for the backlog.

- [ ] Single-sentence description using user story or given/when/then format
- [ ] Acceptance criteria written as boolean checkboxes (true when done, false when not)
- [ ] Each criterion is independently testable
- [ ] No hidden conjunctions ("and", "then") that suggest the issue should be split
- [ ] Developer notes include relevant context, technical approach, or constraints
- [ ] Related issues linked
- [ ] Appropriate labels applied (bug, enhancement, good first issue, etc.)

## Sprint Checkpoint

Use this mid-sprint to make sure you're on track.

- [ ] Issue assigned and understood
- [ ] Draft PR opened with initial work
- [ ] Blockers surfaced to Tech Lead
- [ ] Acceptance criteria reviewed and clear
- [ ] Commits pushed (not sitting only on local machine)

## Before Raising a PR

- [ ] Code builds without errors
- [ ] All existing tests pass
- [ ] New tests written for new functionality
- [ ] No new warnings introduced
- [ ] Branch is rebased on latest `main`
- [ ] Commit messages are clear and descriptive
- [ ] PR description explains what changed and why
- [ ] Related issue is linked (use `Closes #123`)
- [ ] Documentation updated if behavior changed
- [ ] Self-review completed (read your own diff before requesting review)

## Reviewing a Teammate's PR

### What to look for

- [ ] Does the code solve the problem described in the issue?
- [ ] Is the implementation approach sound?
- [ ] Is the code readable and maintainable?
- [ ] Are edge cases considered and handled?
- [ ] Is error handling appropriate?
- [ ] Are tests adequate for the changes?
- [ ] Does it follow the project's established patterns?
- [ ] Is documentation clear and accurate?
- [ ] Are there unnecessary complexity or dependencies?

### How to give feedback

- [ ] Start with what's good about the PR
- [ ] Distinguish required changes from suggestions
- [ ] Explain the reasoning behind suggestions
- [ ] Ask questions to understand intent before assuming error
- [ ] Be specific ("this function does three things" vs. "this is confusing")
- [ ] Offer to pair on complex issues

## Sprint Close

End-of-sprint wrap-up after your PR is merged.

- [ ] PR merged (or closed with documented reason)
- [ ] Issue closed and linked to merged PR
- [ ] Demo prepared (see Demo checklist below)
- [ ] Written contribution report prepared (PR links, sprint reflection)
- [ ] Sprint reflection addresses delivery, collaboration, technical growth, and professional development
- [ ] Work log included if PRs don't fully capture the scope of your contribution
- [ ] Any incomplete work documented and moved to a new issue for the next sprint

## Demo

Your demo shows working software. It is not a slide deck about what you plan to build. It is a demonstration of something real that runs.

### Content

- [ ] Demo shows the actual software running, not screenshots or mockups
- [ ] Opens with a one-sentence framing of the problem this work addresses
- [ ] Walks through the feature or fix from the user's perspective
- [ ] Explains the value delivered ("users can now..." not "I implemented...")
- [ ] Keeps technical detail minimal. Save architecture and implementation discussion for code review

### Preparation

- [ ] Rehearsed at least once. Know what you're going to show and in what order
- [ ] Test environment is set up and working before recording or presenting
- [ ] Sample data or test accounts prepared so the demo flows without fumbling
- [ ] Backup plan if the live demo fails (a pre-recorded walkthrough, for instance)

### Format

- [ ] 2-3 minutes for sprint demos (5 minutes maximum)
- [ ] Audio is clear and professional
- [ ] Screen is readable (zoom in on relevant areas, use a reasonable font size)

## Milestone and Launch

When your team is approaching a Milestone target or the final launch sprint.

- [ ] All Milestone-targeted issues merged or explicitly rescoped
- [ ] Working software is demonstrable end-to-end
- [ ] README and setup instructions verified (can a new person follow them?)
- [ ] Architecture and technical documentation current
- [ ] Known bugs and limitations documented as issues
- [ ] Client demo prepared and rehearsed
- [ ] Any gaps between plan and reality documented and communicated to stakeholders

## Handoff

Preparing the project for the next team at the end of your iteration.

- [ ] All intended work merged to `main`
- [ ] Open PRs resolved (merged, closed, or documented for the incoming team)
- [ ] Issue backlog triaged and prioritized
- [ ] Stale branches cleaned up
- [ ] README is accurate and complete (overview, setup, project structure)
- [ ] Architecture documentation reflects current state, not the state from three sprints ago
- [ ] Key decisions documented (ADRs or equivalent)
- [ ] Known issues and technical debt captured as labeled issues
- [ ] Deployment process documented and verified
- [ ] Contributing guide is current
- [ ] No secrets, credentials, or environment-specific paths committed to the repo
- [ ] Development environment setup validated by someone other than the author

## Project Maintenance

Periodic housekeeping that keeps the project healthy. Not tied to a specific lifecycle moment.

- [ ] Open issues triaged and labeled
- [ ] Stale issues closed with explanation
- [ ] Dependencies reviewed for updates and security advisories
- [ ] README and setup instructions still accurate
- [ ] CI pipeline passing on `main`
- [ ] No uncommitted work lingering in open branches
