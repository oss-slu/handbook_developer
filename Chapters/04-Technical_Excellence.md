# 4. Technical Excellence

Writing code that works is the starting point, not the finish line. Technical excellence means writing code that is correct, readable, tested, and maintainable. The software you build will outlive your time on the team. Future developers, possibly including your future self, will need to understand it, extend it, and fix it.

## Core Principles

A few engineering principles apply regardless of language, framework, or project type.

**Separation of concerns.** Each module, class, or function should have one clear responsibility. When a component does too many things, it becomes hard to understand, hard to test, and hard to change without breaking something else.

**Clear interfaces.** The boundary between components should be explicit and well-defined. Other developers should be able to use your code without reading its internals. Good function signatures, type annotations, and API contracts make this possible.

**Minimal coupling.** Components should depend on each other as little as possible. When module A changes, module B shouldn't need to change too. Loose coupling makes the codebase more resilient and easier to work on in parallel.

**Simplicity over cleverness.** Readable code is more valuable than clever code. If a solution requires a comment explaining the trick, consider whether a more straightforward approach would serve better. You write code once; others read it many times.

## Code Quality

Good code quality is not about following rules for their own sake. It's about making the codebase easier for everyone to work with.

**Follow your project's conventions.** Every project has established patterns for naming, file organization, error handling, and style. Learn them early and follow them consistently. If your project uses a linter or formatter, run it before committing. If it doesn't, suggest adding one.

**Keep functions small and focused.** A function that fits on one screen is easier to understand than one that scrolls for pages. If a function is doing multiple things, break it into smaller functions with clear names.

**Name things well.** Variable names, function names, and class names should describe what they represent or do. `calculate_total_price` communicates more than `calc` or `process`. Avoid abbreviations that only make sense to the person who wrote them.

**Avoid unnecessary dependencies.** Every dependency is code you didn't write but are responsible for. Before adding a library, consider whether the functionality is simple enough to implement directly. When you do add a dependency, pin a specific version so builds are reproducible.

## Testing

Tests are how you prove your code works and how you protect it from breaking when the codebase changes. Writing tests is not optional.

**Unit tests** verify that individual functions and methods produce the correct output for a given input. They should be fast, isolated, and focused. Aim for approximately 80% code coverage. Where you fall short, document why.

**Integration tests** verify that components work together correctly. If your project has an API, integration tests confirm that endpoints return the right responses. If it has a database, they confirm that queries and writes behave as expected.

**End-to-end tests** verify complete workflows from the user's perspective. These are the most expensive to write and maintain, so use them selectively for critical paths.

**Write tests as you go.** Don't leave testing for "later." Code that ships without tests tends to stay untested, and untested code is a liability. If your project has CI/CD configured, your tests should run automatically on every pull request.

When you fix a bug, write a test that would have caught it. This prevents the same bug from recurring and gradually makes the test suite more robust.

## Documentation

Good documentation serves different audiences. Code comments help future developers. README files help new contributors. API docs help users. Each serves a purpose, and none replaces the others.

**Code comments** explain *why*, not *what*. The code already shows what it does. Comments should capture reasoning that isn't obvious from the code itself: why a particular approach was chosen, what constraint led to this design, or what edge case this block handles. Don't comment the obvious. `# increment counter` above `counter += 1` adds noise, not clarity.

**README and setup guides** help someone new to the project get oriented and running. If a new developer can't set up the project by following the README, the README needs updating.

**Architecture documentation** explains how the system fits together. It captures the high-level design, the major components, and how they interact. Architecture Decision Records (ADRs) capture *why* important technical choices were made. These are especially valuable when the original developers are no longer on the team.

**Inline documentation** (docstrings, type annotations) describes public interfaces. Functions that other developers call should document their parameters, return values, and any exceptions they raise.

Treat documentation as a first-class part of the work. When you change code, update the documentation that describes it. Stale documentation is worse than no documentation because it actively misleads.

## CI/CD

Continuous Integration and Continuous Deployment (CI/CD) automate the process of building, testing, and deploying your code. Most projects in the program use GitHub Actions for this.

At minimum, your project's CI pipeline should:

- Build the code on every pull request.
- Run the test suite on every pull request.
- Enforce linting and formatting standards.

A pull request that fails CI checks should not be merged. Fix the failures first. If a CI check is flaky (fails intermittently for reasons unrelated to your code), raise it as an issue. Don't train yourself to ignore red checks.

## Managing Technical Debt

Technical debt is the cost of choosing a quick or expedient solution now instead of a better one that would take longer. Some debt is intentional and strategic. Most debt accumulates gradually through small shortcuts.

You don't need to fix every piece of technical debt you encounter. But you should notice it and communicate about it. If you find a pattern that makes the codebase harder to work with, mention it to your Tech Lead. File an issue so it's tracked. Small improvements made consistently compound over time.

When you do touch existing code, follow the scout rule: leave it a little cleaner than you found it. Rename a confusing variable. Extract a duplicated block. Add a missing test. These small acts of care add up.

For a deeper treatment of how to identify, assess, and prioritize technical debt, see the [Codebase Technical Assessment Guidebook](https://github.com/oss-slu/guidebook_tech_debt).
