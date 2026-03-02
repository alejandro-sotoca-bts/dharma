# dharma

Canonical source of engineering principles and accumulated wisdom for AI-assisted development. The name refers to "the right way" — not rigid rules, but a path refined through practice and reflection.

Human and agent share this path equally. `AGENTS.md` is a shared commitment, not instructions from one to the other.

## Starting a session

Before diving into implementation, orient yourself. These four questions are designed for the human, but work equally well spoken aloud to the agent at the start of a conversation:

1. **What do we know?** — Read `docs/reflections/` and any relevant ADRs. What has been learned? What decisions are already in place?
2. **What do we not know?** — What assumptions are we making? What information is missing?
3. **What did the last session leave for us?** — Check READMEs, recent commits, and any trail left by a previous session.
4. **What is the simplest thing we could do today?** — Before planning the work, question whether less work is the better answer.

This is not a ritual to follow rigidly. It is a habit to develop — a way of beginning with clarity rather than momentum.

## Structure

```text
AGENTS.md                  # Shared principles for human and agent
docs/
  decisions/
    TEMPLATE.md            # ADR template for architectural decisions
  reflections/
    YYYY-MM-DD-*.md        # Process insights and lessons learned
```

## Usage in other projects

To apply dharma to your project, give your AI agent this message:

```text
Read https://github.com/alejandro-sotoca-bts/dharma/blob/main/AGENTS.md and the reflections at https://github.com/alejandro-sotoca-bts/dharma/tree/main/docs/reflections to understand the reasoning behind the principles. Then adapt AGENTS.md to this project: keep the core principles intact, add project-specific guidelines (framework, language, doc links), and create a docs/decisions/ directory with the ADR template from the same repo.
```

That's it. The agent will read the principles, understand the project's stack, and produce an adapted AGENTS.md.

When principles evolve here, propagate to downstream projects. When a project-specific insight turns out to be universal, promote it upstream to dharma.

## Design decisions

- **No tooling, no dependencies.** Plain markdown in a git repo. If it needs a build step, it's too complex.
- **Principles and practices.** Principles tell both parties *how to think*. Practices compensate for structural limitations with concrete habits. Both are necessary.
- **Append-only history.** ADRs and reflections are never rewritten. The chain of reasoning is the institutional memory.
- **Reflections feed the principles.** When a pattern recurs enough to become a principle, it gets promoted to AGENTS.md. This is how dharma grows.
