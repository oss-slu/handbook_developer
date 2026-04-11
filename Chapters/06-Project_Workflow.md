# 6. Project Workflow

This chapter covers how you'll work day-to-day: the sprint rhythm, how to use GitHub effectively, and what a good pull request looks like. These practices apply across all projects in the program, though your team's Working Agreement may define additional norms.

## The Two-Week Sprint Cycle

Work is organized into two-week sprints. Each sprint is a bounded commitment: you take on a piece of work, you deliver it, and then you reflect on what happened. This rhythm creates accountability, shortens feedback loops, and builds the professional habit of shipping on a schedule.

### Week 1: Build

At the start of the sprint, your Tech Lead will have issues ready for the team. Pick up an issue, ask questions early if anything is unclear, and start working.

During the first week:

- Push commits regularly. Don't wait until the last day to show progress.
- Open a **draft PR** as soon as you have something reviewable. This gives your Tech Lead early visibility into your approach and lets them catch issues before they compound.
- Ask for help when you're stuck. Your project Slack channel, teammates, and office hours are all there for this.

By the end of Week 1, you should have a **functional pull request** raised. "Functional" means the code runs without breaking existing functionality and addresses the issue you were assigned, even if it's not yet polished. This mid-sprint deadline exists because code review takes time. Your Tech Lead needs to see your work while there's still a week to iterate.

### Week 2: Refine and Merge

Your Tech Lead will review your PR and likely request changes. This is normal. Professional code rarely merges on the first try.

During the second week:

- Respond to review feedback promptly. Aim for within 24 hours.
- Ask clarifying questions if you don't understand the feedback.
- Push fixes and request re-review.
- Communicate in the PR thread, not just Slack. The PR is the record of the work.

By the end of Week 2, your PR should be fully merged. Your Tech Lead will either merge your work or close the PR. They won't merge broken code just because the sprint is ending. The work has to be worth merging.

### When Things Don't Go as Planned

**Your issue is bigger than you thought.** Talk to your Tech Lead early. Try to surface this by Wednesday of Week 2. They can rescope the work: reduce the current issue to something achievable and move the remaining work to a new issue for a future sprint. Identifying scope creep early is a professional skill, not a failure.

**You're stuck and can't make progress.** Raise this immediately, not at the sprint deadline. Your Tech Lead, your teammates, and your project's Slack channel are all resources. Suffering in silence for two weeks helps no one.

**Your PR got closed without merging.** This happens when the work doesn't meet the bar for merging. Perhaps it breaks existing functionality or doesn't actually solve the issue. It's not punishment. It's how professional development works. Understand what went wrong, learn from it, and do better next sprint.

## Iteration Milestones

Sprints keep you moving; Milestones give that movement direction. Each iteration has two Milestones. These are larger goals that your team is working toward across multiple sprints.

- **Milestone 1** targets completion around midterms.
- **Milestone 2** targets completion before the end of the semester.

Milestones represent tangible value: a working feature set, a deployed integration, a usable tool. They're ambitious but achievable, and reaching them builds a real sense of accomplishment for you and your team. They also give your client something concrete to see and react to at natural checkpoints in the semester.

### How Milestones Shape Your Sprint Work

A single merged PR per sprint is the baseline expectation (see [Chapter 7](07-Program_Requirements.md)), but Milestones often require sustained momentum beyond that baseline. Some sprints may call for multiple PRs, or for coordinating your work closely with teammates so that related pieces land together.

When planning your sprint work, think about where your issue fits in the Milestone. Ask yourself: "Does this move us closer to something we can demonstrate?" Work that advances a Milestone, not just closes a ticket, creates outsized value for the project.

### When a Milestone Is at Risk

Sometimes a Milestone won't be reached despite the team's best effort. External dependencies shift, technical assumptions prove wrong, or a key piece turns out to be harder than anyone anticipated. These are real-world circumstances, not failures.

When it becomes clear that a Milestone is at risk, handle it professionally:

- **Surface it early.** Don't wait until the target date to raise the concern. As soon as you see the gap, talk to your Tech Lead.
- **Document the challenges.** Capture what happened. Record what was attempted, what blocked progress, and what was learned. This goes in your sprint reflections and in communication with your client.
- **Communicate with stakeholders.** Your Tech Lead will coordinate with the client and program staff, but you should be prepared to speak to your own contributions and what you observed.
- **Adjust the plan.** Work with your team to rescope: what can still be delivered? What moves to the next Milestone? A partial delivery with clear communication is always preferable to silence followed by a missed target.

The goal isn't perfection. It's professional accountability. Milestones that aren't fully reached still produce working software, learning, and a clearer picture of what comes next.

## Working with GitHub

GitHub is where the work lives. Your project uses Issues for tracking work, Projects for prioritization, and Pull Requests for code review and collaboration.

### Issues

Issues are the units of work. A well-written issue includes a clear description (what needs to happen and why), acceptance criteria (boolean conditions that are true when the work is done), and any relevant technical context.

When you pick up an issue:

- Make sure you understand the acceptance criteria before you start coding. If something is ambiguous, ask your Tech Lead.
- Assign yourself to the issue so your team knows it's being worked on.
- Reference the issue number in your commits and PR description.

### Feature Branches

Create a branch from `main` for each issue you work on. Keep the branch focused on that one issue. Name it descriptively. `feature/add-user-search` is better than `my-branch`.

Keep your branch short-lived. If it runs longer than one sprint, it's probably doing too much. Rebase on `main` before requesting review to ensure you're working with the latest code and to catch any conflicts early.

### Pull Requests

Every PR should:

- **Solve one issue.** Don't bundle unrelated changes. A PR that fixes a bug and also refactors a different module is harder to review and harder to revert if something goes wrong.
- **Include a clear description.** Explain what you changed and, more importantly, *why*. The code shows the "what"; the description explains the reasoning. Reference the issue it closes (use `Closes #123` to auto-close the issue on merge).
- **Pass CI checks.** If your project has automated tests and linting, your PR should pass them before you request review.
- **Be a reasonable size.** Aim for under 400 lines of changed code. Smaller PRs get faster, higher-quality reviews.

#### The Draft PR Pattern

Open a draft PR early, even if your implementation is incomplete. A draft PR:

- Gives your Tech Lead visibility into your approach before you've invested days in a direction that might need adjustment.
- Creates a place for early feedback and discussion.
- Shows your progress to the team.

Convert the draft to "Ready for Review" when you've met the acceptance criteria and are confident in your implementation.

#### Responding to Review Feedback

When your Tech Lead or a teammate requests changes:

- Read the feedback carefully. Make sure you understand what's being asked and why.
- If you disagree with a suggestion, explain your reasoning in the PR thread. Professional disagreement is healthy. Focus on the technical merits, not personalities.
- Push your fixes as new commits (don't force-push during review, so reviewers can see what changed).
- Re-request review when you've addressed all feedback.

## Sprint Demos

At the end of each sprint, you'll demonstrate your work. Think of this as presenting to a client or stakeholder: show the working functionality, explain what it does and why it matters, and keep it concise (2-3 minutes).

Good demos focus on value delivered, not implementation details. "Users can now filter search results by date" is more compelling than "I added a date parameter to the API endpoint." Save the technical discussion for code review.

## Working Agreements

Your team defines its own norms through a Working Agreement. This document covers communication expectations, code standards, meeting schedules, and how you'll work together. The Working Agreement is created collaboratively at the start of each iteration and updated as the team learns what works.

When a practice isn't covered by this handbook, check your Working Agreement. When neither covers it, bring it up with your team.
