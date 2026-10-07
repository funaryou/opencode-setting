---
name: pencil-ops
description: |
  Use for all Pencil MCP and .pen operations.

  Triggers:
  - .pen
  - Pencil
  - pencilMCP
  - design editing
  - UI generation
  - dashboard creation
  - batch_design
  - batch_get
  - layout update
  - screenshot validation
---

# Pencil Ops Skill

Use this skill for all `.pen` design reads and edits through Pencil MCP tools.

## Safety Rules

- NEVER manually edit raw `.pen` JSON.
- ALWAYS use Pencil MCP tools.
- Always read before write.
- Keep edits small and scoped (one intent per operation).

## Required Workflow

1. Open the document and inspect current state (`open_document`, `get_editor_state`).
2. Read target nodes first with `batch_get`.
3. Plan minimal edits that preserve hierarchy and spacing.
4. Apply edits via `batch_design` (or `replace_all_matching_properties` for safe bulk updates).
5. Validate with `get_screenshot` and re-check critical nodes with `batch_get`.
6. If output is inconsistent, re-read state and apply a narrower follow-up edit.

## Preferred Tooling Patterns

- Use `find_empty_space_on_canvas` before adding new blocks.
- Use variables/tokens (`get_variables`, `set_variables`) instead of hardcoded values when possible.
- Use `search_all_unique_properties` before broad property replacement.
- Export only when requested (`export_nodes`).

## Output Style

- Report what was read, what was edited, and what was validated.
- State assumptions when node targets were inferred.
- Call out unresolved visual risks before handoff.
