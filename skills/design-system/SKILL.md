---
name: design-system
description: |
  Use for token/variable governance and reusable UI consistency in Pencil projects.

  Triggers:
  - design system
  - tokens
  - variables
  - semantic color
  - typography scale
  - reusable components
  - dark mode
  - light mode
---

# Design System Skill

Use this skill to keep UI output consistent across screens by standardizing variables, scales, and reusable patterns.

## System Responsibilities

- Define and maintain color/spacing/typography variables.
- Enforce semantic token usage over ad-hoc values.
- Keep reusable component patterns consistent.
- Coordinate dark/light theme parity.

## Required Workflow

1. Audit current variables and usage (`get_variables`, `batch_get`).
2. Identify drift (duplicate values, inconsistent type scales, one-off colors).
3. Propose or apply token updates with `set_variables`.
4. Migrate usage safely with targeted `batch_design` or property replacement.
5. Validate representative frames using `get_screenshot`.

## Guardrails

- NEVER manually edit raw `.pen` JSON.
- ALWAYS use Pencil MCP tools.
- Prefer additive and reversible token changes over wide destructive edits.
- Run broad replacements only after reading unique property distribution.

## Output Style

- Separate token policy decisions from implementation edits.
- List adopted naming conventions explicitly.
- Call out migration work that remains.
