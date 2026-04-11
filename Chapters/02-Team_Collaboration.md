# 2. Team Collaboration

Software is built by teams, not individuals. Your technical skills matter, but your ability to communicate, give and receive feedback, and work effectively with others determines how much impact those skills actually have. This chapter covers the collaboration practices that make teams productive.

## Communication Norms

Use the right channel for the message. Technical discussions about code belong in GitHub issues and PR comments, where they stay connected to the work and remain discoverable. Quick questions and team coordination flow through Slack. Formal communications with clients or stakeholders go through email.

A few principles that apply everywhere:

- **Be respectful and concise.** Get to the point, but don't be curt. Assume good intent from others.
- **Acknowledge messages.** If someone asks you a question and you can't answer right away, say so. "I'll look into this after my current task" is better than silence.
- **Default to public channels.** Ask questions in your project's Slack channel rather than DMs. Others benefit from seeing the question and the answer. Your Tech Lead shouldn't have to answer the same question multiple times.
- **Document decisions where they'll be found.** If a Slack conversation leads to a decision about the codebase, capture it in a GitHub issue comment or PR thread. Slack messages scroll away. GitHub persists.

Your team's Working Agreement will define specific norms like response time expectations and meeting schedules. These vary by team.

## Asking for Help

Asking for help is expected. Struggling alone for days is not a virtue. But there's a difference between asking a thoughtful question and asking someone to do your thinking for you.

Before reaching out, do the groundwork:

1. **Read existing documentation.** Check the project README, contributing guide, and any relevant docs.
2. **Search open issues and PRs.** Someone may have encountered the same problem or discussed the same topic.
3. **Attempt a minimal solution.** Even if it doesn't work, it gives you something concrete to discuss.
4. **Formulate a clear question.** State what you're trying to do, what you've tried, and where you're stuck.

A well-formed question might look like: "I'm trying to add date filtering to the search endpoint. I looked at how the existing status filter works in `search_controller.py`, but I'm getting a type error when I pass the date parameter. Here's the traceback. What am I missing?"

Compare that to: "The search thing isn't working. Can someone help?"

The first version respects your teammate's time and gets you a faster, better answer.

## Team Meetings

Your team will have regular meetings. The specifics are defined in your Working Agreement, but the principles are the same everywhere.

**Come prepared.** Know what you've completed since the last meeting, what you're working on, and whether you're blocked on anything. If you don't have an update, that itself is worth saying.

**Respect time boundaries.** If a technical discussion goes deep during a status meeting, suggest taking it offline. "Let's pair on this after the meeting" keeps the meeting useful for everyone.

**Contribute actively.** Meetings work when everyone participates. If you have a question, insight, or concern, share it. If a quieter teammate might have relevant experience, invite their perspective.

## Working with Your Tech Lead

Your Tech Lead is responsible for your team's technical direction, code quality, and your professional growth. They're also a student, managing their own learning alongside yours. A productive working relationship benefits both of you.

**Seek feedback, not just approval.** When your Tech Lead reviews your code, they're investing time in helping you improve. Engage with their comments. Ask why a different approach is better, not just whether you need to change it.

**Surface problems early.** If you're behind, confused, or stuck, tell your Tech Lead sooner rather than later. They can't help with problems they don't know about, and late surprises limit everyone's options. Raising a concern on Tuesday gives your team a week to adapt. Raising it on sprint deadline day gives them nothing.

**Take initiative.** Don't wait to be assigned work if there's clearly work to be done. If you finish early, look at the backlog. If you notice a gap in documentation, mention it. Your Tech Lead will notice the difference between a developer who waits for instructions and one who looks for ways to contribute.

**Treat feedback as growth.** Code review comments, process suggestions, and direct feedback are all part of professional development. If feedback stings, that's natural. Take a moment, then engage with the substance. The ability to receive feedback gracefully and act on it is one of the most valuable professional skills you can build.

## Working with Your Client

Your project has a client or stakeholder. They represent the people who will use the software you're building. They bring domain knowledge you don't have and priorities shaped by real-world needs.

**Listen carefully in client meetings.** Pay attention to the problems they describe, not just the solutions they suggest. Clients know their domain. You know the technology. The best outcomes happen when both perspectives inform the work.

**Ask clarifying questions.** If a requirement is ambiguous, say so. "When you say 'export the report,' do you mean PDF, CSV, or both?" is much better than guessing and building the wrong thing.

**Demonstrate working software.** Clients gain confidence when they can see progress. Your sprint demos (see [Chapter 6](06-Project_Workflow.md)) are a chance to show them real, working functionality and get their feedback early.

## Code Reviews

Code review is one of the most important collaboration practices in software development. It catches bugs, spreads knowledge across the team, and raises everyone's standard of work.

### As a Reviewer

When reviewing a teammate's code, focus on what matters most:

- **Correctness.** Does the code solve the problem described in the issue? Does it handle edge cases?
- **Readability.** Will another developer understand this code six months from now?
- **Architecture.** Does the approach fit the project's patterns? Does it introduce unnecessary complexity?
- **Testing.** Are there tests? Do they cover the important behavior?

Be constructive and specific. "This function is hard to follow" is less helpful than "This function does three things. Could we extract the validation logic into a separate method?" Start with what's good about the PR before diving into what needs to change.

Distinguish between required changes and suggestions. "This will break if the input is null" is a required fix. "You might consider using a list comprehension here" is a suggestion. Making this distinction clear saves back-and-forth.

### As the Author Receiving a Review

Receiving code review is a professional skill. Your reviewer is spending their time to make your work better.

- Read each comment carefully. Don't get defensive.
- If you agree with the feedback, make the change and thank the reviewer.
- If you disagree, explain your reasoning in the PR thread. Focus on the technical tradeoffs, not on being right.
- Don't take it personally. The review is about the code, not about you.

Your ability to participate effectively in code review, both giving and receiving, is one of the clearest signals of professional maturity.

## Pair Programming

Pair programming is when two developers work together at one workstation. One writes code (the "driver") while the other reviews in real-time and thinks about the bigger picture (the "navigator"). Roles switch frequently.

Pairing is especially useful for:

- **Complex or unfamiliar code.** Two sets of eyes catch more issues, and you learn faster with a partner.
- **Onboarding.** Pairing with an experienced teammate is one of the fastest ways to learn a codebase.
- **Getting unstuck.** If you've been spinning on a problem for an hour, a pairing session often unblocks you in minutes.

Your team defines when and how to pair in your Working Agreement. Not every task needs pairing, but knowing when to reach for it is a valuable skill.

## Cross-Team Collaboration

Occasionally your work will intersect with another project team. When this happens, communicate assumptions explicitly. What seems obvious to your team may not be obvious to theirs.

If you're building something that another team depends on (or vice versa), align on interfaces and expectations early. Document the agreement in writing. A shared GitHub issue or a brief message in a cross-team Slack channel works well.
