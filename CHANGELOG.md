# Changelog

All notable changes to this agent are tracked here.

## [1.1.0] - 2026-11-10

- Require XML documentation on every type and method the agent creates or changes, including private methods, and a WHY comment at each crucial point (transactions, concurrency, security, provider branches, business rules, and non-obvious error handling).
- Require a fixed layout for every line the agent writes or touches: 4-space indentation, Allman braces, braces on every control statement, a 120-character line limit, and methods kept short.
- These comment and formatting rules override the 1.0.0 guidance to keep documentation proportional and to skip XML docs on private methods.
- Require `dotnet format` on the changed files, then a comments-and-formatting review, before the agent reports a task done.
- Require clear, simple language in user-facing explanations, while keeping exact paths, names, evidence, and risks for developers.

## [1.0.0] - 2026-11-04

- Initial public, platform-specific Claude Code + Codex distribution.
- MIT license and step-by-step project/personal installation instructions.
- Version declarations and immutable versioned release snapshots.
- Normalized original `-v2` agent identity to the stable `csharp-expert-developer` name and removed source-project-specific reference links.
