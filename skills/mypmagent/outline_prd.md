---
name: pm-outline-prd
description: "Propose a PRD outline (sections + ticket estimate) from idea + clarifications."
version: 0.1.0
author: niraj28rai
license: MIT
platforms: [linux, macos, windows]
metadata:
  hermes:
    tags: [pm, product-management, prd, outline]
    related_skills: [pm-clarify, pm-draft-prd, pm-generate-tickets]
---

# PM Outline PRD

## Overview

Given a raw idea, optional transcript, and answered clarifications, propose a
PRD outline: an ordered list of sections with a brief description of each, plus
an estimate of how many Linear tickets this feature would generate.

## Input schema

```json
{
  "raw_idea": "string",
  "transcript": "string | null",
  "clarifications": [
    {
      "question": "string",
      "answer": "string | null"
    }
  ]
}
```

## Output schema

```json
{
  "sections": [
    {
      "id": "string — e.g. §1, §2",
      "title": "string — e.g. PROBLEM, USERS, GOALS",
      "what_it_covers": "string — one sentence"
    }
  ],
  "ticket_estimate": "number — estimated Linear ticket count"
}
```

## Prompt (STUB — filled in Phase 2)

> TODO: Write the 250–400 word system prompt with one full example in Phase 2.

Respond only with valid JSON matching the output schema above.
