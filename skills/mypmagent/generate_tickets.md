---
name: pm-generate-tickets
description: "Generate Linear-ready tickets with acceptance criteria from a completed PRD."
version: 0.1.0
author: niraj28rai
license: MIT
platforms: [linux, macos, windows]
metadata:
  hermes:
    tags: [pm, product-management, tickets, linear, acceptance-criteria]
    related_skills: [pm-clarify, pm-outline-prd, pm-draft-prd]
---

# PM Generate Tickets

## Overview

Given the completed PRD markdown and a ticket estimate, generate a set of
Linear-shaped tickets. Each ticket includes a title, description, acceptance
criteria, priority (P0/P1/P2), size estimate (S/M/L), and labels.

Acceptance criteria is the part most AI tools skip — this skill always includes
at least one criterion per ticket.

## Input schema

```json
{
  "prd_markdown": "string — the full PRD as markdown",
  "ticket_estimate": "number — expected ticket count from the outline step"
}
```

## Output schema

```json
{
  "tickets": [
    {
      "id": "string — T-001, T-002, ...",
      "title": "string",
      "description": "string — 2–4 sentence context",
      "acceptance_criteria": ["string — each criterion is one testable statement"],
      "priority": "P0 | P1 | P2",
      "estimate": "S | M | L",
      "labels": ["string"]
    }
  ]
}
```

## Prompt (STUB — filled in Phase 2)

> TODO: Write the 250–400 word system prompt with one full example in Phase 2.

Respond only with valid JSON matching the output schema above.
