> This repository documents the operating system I use to build production software with AI-assisted engineering.
>
> It is not a prompt collection.
>
> It is the repeatable process I use to translate business strategy into production-ready software through specification, engineering workstreams, AI-assisted implementation, disciplined review, and measurable releases.

# Spec-Driven Agentic Workflow

A practical engineering runbook for orchestrating AI-assisted software delivery using Antigravity, Codex, ChatGPT, Gemini and disciplined human review.

This is the workflow I use to design, build and ship production software such as MREN Africa and Dynasquare.

---

# Engineering Philosophy

AI is not my engineer.

AI is part of my engineering team.

Every feature starts with a business objective, becomes a technical specification, is decomposed into engineering workstreams, implemented with AI assistance, reviewed by a human and only then released.

The specification—not the prompt—is the source of truth.

---

# Delivery Lifecycle

```
Brand Strategy
        │
        ▼
Technical Specification
        │
        ▼
Engineering Planning
        │
        ▼
Workstream Decomposition
        │
        ▼
AI-assisted Implementation
        │
        ▼
Human Review
        │
        ▼
Testing
        │
        ▼
Release
        │
        ▼
Measurement
```

---

# Core Principles

- Business requirements drive engineering.
- Specifications drive implementation.
- AI generates candidate implementations.
- Humans own architecture.
- Every release is measurable.
- Every deployment should be reversible.

---

# My Tooling

## IDE

- Antigravity

## AI

- Codex
- ChatGPT
- Gemini

## Platform

- Git
- GitHub
- Supabase
- Next.js
- TypeScript
- PostgreSQL

---

# Engineering Workflow

## Phase 1 — Strategy Handover

Every project starts with a structured handover.

I first understand:

- Business objectives
- User personas
- Brand positioning
- KPIs
- Information architecture
- Success metrics

No code is written before this is clear.

---

## Phase 2 — Specification

Before implementation I write a specification covering:

- Architecture
- Database
- APIs
- User journeys
- Roles & permissions
- Validation
- Analytics
- SEO
- Performance
- Acceptance criteria

The specification becomes the contract for delivery.

---

## Phase 3 — Engineering Workstreams

The project is divided into independent workstreams such as:

- Platform Architecture
- Frontend
- Backend
- Database
- Authentication
- Analytics
- Technical SEO
- Testing
- Deployment

Each workstream has clearly defined outputs.

---

## Phase 4 — AI-assisted Delivery

Rather than asking AI to "build a feature", each workstream receives a bounded specification.

AI assists with:

- implementation
- refactoring
- migrations
- debugging
- documentation
- testing

Every generated change is reviewed before merging.

---

## Phase 5 — Review

Before anything reaches production I verify:

- business rules
- architecture
- security
- performance
- analytics
- accessibility
- regressions

Generated code is never trusted automatically.

---

## Phase 6 — Release

A release includes:

- build validation
- type checking
- migration verification
- analytics verification
- deployment review
- rollback validation

Only after all quality gates pass does deployment proceed.

---

# Human Responsibilities

AI accelerates engineering.

Humans remain responsible for:

- Architecture
- Product decisions
- Security
- Trade-offs
- Code review
- Release approval

---

# Continuous Improvement

Every completed project feeds back into the workflow.

Specifications improve.

Prompt patterns improve.

Engineering checklists improve.

Release quality improves.

The workflow evolves with every product shipped.
