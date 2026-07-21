# Prompt Patterns for Spec-Driven Agentic Engineering

This document explains how I communicate with engineering agents.

I avoid open-ended prompts such as:

> "Build this feature."

Instead, every task is framed with context, constraints, expected outputs, and review criteria.

The objective is predictable engineering rather than unpredictable generation.

---

# Pattern 1 — Repository Discovery

Purpose:

Understand the existing system before proposing changes.

Example

```
Inspect the repository.

Identify:

- existing architecture
- related modules
- affected files
- dependencies
- technical risks
- assumptions that should not be made

Do not implement anything.

Only produce an engineering assessment.
```

Why?

Engineering begins with understanding the current system.

---

# Pattern 2 — Technical Specification Review

Purpose:

Challenge the specification before implementation.

Example

```
Review this specification.

Identify:

- ambiguous requirements
- missing edge cases
- conflicting business rules
- security concerns
- scalability concerns
- opportunities to simplify

Do not write code.
```

Why?

A weak specification produces weak implementations.

---

# Pattern 3 — Workstream Planning

Purpose:

Decompose implementation into independent engineering streams.

Example

```
Break this specification into independent engineering workstreams.

For each workstream define:

- responsibility
- dependencies
- expected output
- acceptance criteria
```

Why?

Smaller workstreams reduce risk and improve review quality.

---

# Pattern 4 — Controlled Implementation

Purpose:

Generate implementation for a single workstream.

Example

```
Implement only the database layer.

Do not modify unrelated files.

Follow the specification exactly.

Explain every architectural decision.

List any assumptions.
```

Why?

Small, controlled changes are easier to review.

---

# Pattern 5 — Diff Review

Purpose:

Review generated code before merging.

Example

```
Review the implementation.

Identify:

- bugs
- regressions
- security issues
- architectural inconsistencies
- business-rule violations

Recommend improvements before merge.
```

Why?

AI-generated code is treated as a candidate implementation.

---

# Pattern 6 — Production Readiness

Purpose:

Validate release quality.

Example

```
Review this implementation for production readiness.

Verify:

- acceptance criteria
- performance
- security
- analytics
- permissions
- testing
- deployment readiness

Do not modify code.

Produce a release assessment.
```

Why?

Shipping software requires more than working code.

---

# Pattern 7 — Post-Release Reflection

Purpose:

Improve the engineering system itself.

Example

```
Review the completed delivery.

What slowed development?

What should become part of future specifications?

Which prompt patterns should improve?

Which engineering checklist should change?
```

Why?

Every completed project improves the next one.

---

# Engineering Principle

I don't use prompts as instructions.

I use prompts as engineering contracts.

The AI's responsibility is producing the best candidate implementation possible.

My responsibility is ensuring the delivered system satisfies the specification, protects the architecture, and achieves the intended business outcome.
