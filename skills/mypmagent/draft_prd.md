---
name: pm-draft-prd
description: "Stream a full PRD section-by-section from an approved outline."
version: 0.1.0
author: niraj28rai
license: MIT
platforms: [linux, macos, windows]
metadata:
  hermes:
    tags: [pm, product-management, prd, draft, streaming]
    related_skills: [pm-clarify, pm-outline-prd, pm-generate-tickets]
---

# PM Draft PRD

## Overview

Given the full context (idea, transcript, clarifications, approved sections),
stream the PRD one section at a time. Each chunk in the stream is one completed
section. The frontend renders sections as they arrive via Server-Sent Events.

## Input schema

```json
{
  "context": {
    "raw_idea": "string",
    "transcript": "string | null",
    "clarifications": [{ "question": "string", "answer": "string | null" }]
  },
  "approved_sections": [
    {
      "id": "string — e.g. §1",
      "title": "string",
      "what_it_covers": "string"
    }
  ]
}
```

## Output schema (streamed — one object per section)

```json
{
  "section_id": "string — e.g. §1",
  "content": "string — markdown content for this section (≥80 words)"
}
```

## Prompt (STUB — filled in Phase 2)

> TODO: Write the 250–400 word system prompt with one full example in Phase 2.
> Note: this skill uses streaming=true — the frontend consumes SSE chunks.

Respond only with valid JSON matching the output schema above, one object per section.
