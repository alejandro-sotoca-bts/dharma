# AGENTS.md

## Core Principles

### 1. Maximum Simplicity (KISS — hard mode)

- Default to the least complex solution that satisfies *current* requirements, not anticipated ones.
- Prefer standard library > well-known framework > custom code — in that order.
- If a feature requires significant scaffolding to support, question whether the feature is necessary at all.
- Complexity is a cost. Every abstraction, config option, and dependency must earn its place.
- Distinguish between *what is needed now* and *what might be needed later*. Build only the former.
- Features that are not actively used or tested are liabilities. Remove them or don't build them.

### 2. Solutions Close to the Root

- When debugging or designing, resist fixing symptoms. Trace the problem to its origin before writing any code.
- Ask: *Is this problem a consequence of a prior design decision that should be revisited instead?*
- Prefer removing code over adding code when both achieve the goal.
- A 10-line solution that eliminates a problem is better than a 100-line solution that manages it.

### 3. Mandatory Retrospective Lens

Before committing to any non-trivial implementation, pause and ask:

> **"What would I do differently if I already knew what I'm about to learn by building this?"**

> **"What is the simplest way to meet today's actual needs — even if it means abandoning prior work or dropping non-essential features?"**

This is not optional. Apply it when:
- Starting a new feature or capability.
- A task turns out significantly harder than expected.
- The codebase has grown noticeably without a clear payoff.
- A workaround is being stacked on top of a previous workaround.

### 4. Quality Guardian

- If a requested change would introduce duplication, tight coupling, unclear naming, or untested behavior, flag it and propose an alternative before implementing.
- Do not silently comply with a request that contradicts the principles in this file. Explain the conflict, suggest a better path, and defer to the human's final decision.
- "Make it work" is not an excuse to bypass these principles. A quick fix that degrades the codebase is only acceptable if the human explicitly acknowledges the trade-off.

---

## Behavior

- Check README.md files when needed for context; update them when the documented behavior no longer reflects reality.
- When the correctness of a framework or library API call is uncertain, verify against the official docs before implementing — training data may reflect an outdated API shape.
- Surface trade-offs explicitly rather than making silent architectural choices.
- Prefer self-contained, easy-to-delete code over deeply integrated code.

---

## Decision Records (ADR)

Non-obvious architectural decisions must be recorded as **Architecture Decision Records** in `docs/decisions/`.

Use the template at `docs/decisions/TEMPLATE.md`. Keep entries short — 10 to 20 lines is enough.

**Create an ADR when:**
- Choosing between two or more viable technical approaches.
- Deciding to drop a feature, reverse a previous decision, or accept a known trade-off.
- The retrospective lens (Principle 3) reveals that the current path should change.
- A task took significantly longer than expected and the reason was a prior design choice.

ADRs are append-only: never delete or rewrite an accepted record. If a decision is reversed, create a new ADR that supersedes the old one. This preserves the chain of reasoning across sessions.
