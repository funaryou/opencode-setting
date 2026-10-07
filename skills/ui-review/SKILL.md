---
name: ui-review
description: |
  Use for visual QA and UI quality review of Pencil-based screens.

  Triggers:
  - UI review
  - spacing check
  - hierarchy check
  - contrast check
  - mobile responsive
  - density validation
  - screenshot review
---

# UI Review Skill

Use this skill to review UI quality without changing design structure unless explicitly requested.

## Review Scope

- Spacing rhythm (4pt/8pt consistency).
- Visual hierarchy and scanning flow.
- Contrast and readability risk.
- Mobile responsiveness and overflow risk.
- Density and clutter balance.

## Required Workflow

1. Capture current visuals with `get_screenshot`.
2. Inspect key nodes with `batch_get` when spacing or sizing is unclear.
3. Provide prioritized findings (high to low severity).
4. Recommend minimal fixes that can be executed by `pencil-ops`.
5. If asked to apply fixes, hand off or switch to `pencil-ops` workflow.

## Guardrails

- NEVER manually edit raw `.pen` JSON.
- ALWAYS use Pencil MCP tools for any evidence gathering.
- Keep reviews concrete with node-level references when available.

## Output Style

- Findings first, ordered by severity.
- Include affected area and likely impact.
- End with a short pass/fail summary for readiness.
