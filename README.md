# Lexum

**Deterministic control for distributed systems.**

Lexum is a control-plane programming language where system behavior is defined as executable law.

Instead of scripting operations or declaring configurations, Lexum defines what must be true — and the runtime deterministically enforces it.

---

# Core Idea

```
Code  → tells the system what to do
.lex  → defines what must be true
```

A ".lex" file is not configuration.

It is a law governing a domain of your system.

---

# Example

```
auth.lex
network.lex
storage.lex
```

Each file defines:

- state
- invariants (must never break)
- goals (must converge)
- transitions (deterministic correction)

---

# Execution Model

Lexum systems are:

- Deterministic — same input → same execution → same result
- Convergent — systems reconcile toward defined goals
- Traceable — execution can be replayed exactly
- Isolated — domains communicate via explicit boundaries

---

# CLI

```
lex apply auth.lex     # enforce system law
lex plan auth.lex      # preview required changes
lex validate auth.lex  # verify invariants
lex trace auth.lex    # replay execution
```

## Development tooling:

```
lex build
lex test
lex lint
lex fmt
```

---

# Philosophy

Lexum treats infrastructure as law, not configuration.

- No implicit behavior
- No hidden side effects
- No nondeterminism

A system defined in ".lex" behaves exactly as written.

---

# Getting Started

Visit the official site:

[LEXUM](https://lexumhq.netlify.app)

---

# Status

Early prototype.

Core runtime, compiler, and deterministic execution model are under active development.

---

# License

Core repositories are released under the Apache License 2.0.
