# dharma

Canonical source of engineering principles, behavioral guidelines, and accumulated wisdom for AI-assisted development.

## What this is

A living repository of principles that guide how AI coding agents (and the humans working with them) should approach software development. The name refers to "the right way" — not rigid rules, but a path refined through practice and reflection.

## Structure

```
AGENTS.md                  # Core principles (copy or reference from other projects)
docs/
  decisions/
    TEMPLATE.md            # ADR template for recording architectural decisions
    ADR-NNNN-*.md          # Individual decision records (append-only)
  reflections/
    YYYY-MM-DD-*.md        # Process insights and lessons learned
```

## Usage

**As a workspace-level AGENTS.md:** Copy `AGENTS.md` to the root of any project that should follow these principles. Adapt the project-specific sections (framework guidelines, doc links) but keep the core principles intact.

**As a reference:** When starting a new project or onboarding a new agent context, point to this repo for the canonical version of the principles.

**ADR template:** Copy `docs/decisions/TEMPLATE.md` into any project that should track architectural decisions. The retrospective field in the template is intentional — it operationalizes Principle 3.

## Design decisions

- **No tooling, no dependencies.** This is plain markdown in a git repo. If it needs a build step, it's too complex.
- **Principles and practices.** Principles tell agents *how to think*. Practices compensate for structural limitations (amnesia, accretion bias, false confidence) with concrete habits. Both are necessary — principles without practices are aspirational; practices without principles are mechanical.
- **Append-only history.** ADRs are never rewritten. If thinking evolves, a new record supersedes the old one. The chain of reasoning is the institutional memory.
- **Reflections feed the principles.** The `docs/reflections/` directory is where raw insights accumulate. When a pattern recurs enough to become a principle, it gets promoted to AGENTS.md. This is how dharma grows organically.
