# Changelog

All notable changes to this agent are tracked here.

## [1.2.1] - 2026-11-24

- Remove the lengthy example while retaining the mandatory comment and formatting rules.
- Reuse successful validation only when command, scope and relevant inputs are unchanged; rerun relevant tests after formatting changes source.
- Clarify MyDevFactory owned-file and evidence handoff without replacing independent review or QA.

## [1.2.0] - 2026-11-24

- Add a "Working efficiently" section: search before reading, read only needed line ranges, batch edits, build per group of edits, run targeted tests while iterating and the full suite once, and keep command output short. Measured MyDevFactory runs showed developer sessions of 200+ model calls with contexts near 270k tokens.
- Stop and report when a task needs files outside the allowed list, instead of growing the scope.
- Run `dotnet format` and the final rebuild once, at the end.
- Condense general .NET, API, security and persistence guidance the model already follows by default. The instruction text is about 30% shorter; the comment and formatting rules from 1.1.0 are unchanged.

## [1.1.0] - 2026-11-10

- Require XML documentation on every type and method the agent creates or changes, including private methods, and a WHY comment at each crucial point (transactions, concurrency, security, provider branches, business rules, and non-obvious error handling).
- Require a fixed layout for every line the agent writes or touches: 4-space indentation, Allman braces, braces on every control statement, a 120-character line limit, and methods kept short.
- These comment and formatting rules override the 1.0.0 guidance to keep documentation proportional and to skip XML docs on private methods.
- Require `dotnet format` on the changed files, then a comments-and-formatting review, before the agent reports a task done.
- Require clear, simple language in user-facing explanations, while keeping exact paths, names, evidence, and risks for developers.
- Document this agent as part of MyDevFactory (https://github.com/dimitriskl/mydevfactory).

## [1.0.0] - 2026-11-04

- Initial public, platform-specific Claude Code + Codex distribution.
- MIT license and step-by-step project/personal installation instructions.
- Version declarations and immutable versioned release snapshots.
- Normalized original `-v2` agent identity to the stable `csharp-expert-developer` name and removed source-project-specific reference links.
