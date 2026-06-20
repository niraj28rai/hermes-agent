---
name: pm-clarify
description: "Generate 3–5 targeted clarifying questions from a raw idea or transcript."
version: 0.1.0
author: niraj28rai
license: MIT
platforms: [linux, macos, windows]
metadata:
  hermes:
    tags: [pm, product-management, clarify, prd]
    related_skills: [pm-outline-prd, pm-draft-prd, pm-generate-tickets]
---

# PM Clarify

## Overview

Given a raw product idea or call transcript, generate 3–5 targeted clarifying
questions that would help a senior PM write a complete PRD.

## Input schema

```json
{
  "raw_idea": "string — the idea or feature description",
  "transcript": "string | null — optional call transcript"
}
```

## Output schema

```json
{
  "questions": [
    {
      "id": "string — e.g. Q1, Q2",
      "text": "string — the question",
      "why_it_matters": "string — one sentence explanation",
      "optional": "boolean — false if PRD cannot proceed without the answer"
    }
  ]
}
```

## Prompt (STUB — filled in Phase 2)

> TODO: Write the 250–400 word system prompt with one full example in Phase 2.

Respond only with valid JSON matching the output schema above.
