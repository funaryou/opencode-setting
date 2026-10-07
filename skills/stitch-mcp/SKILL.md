---
name: stitch-mcp
description: Use Google Stitch MCP to generate, refine, and export UI screens from prompts with implementation-ready outputs.
---

# Google Stitch MCP Skill

Use this skill when the user wants UI design generation, screen iteration, visual variants, or HTML/image export from Google Stitch.

## Workflow

1. Confirm or create the target project first (`create_project` if needed).
2. Generate a screen from a focused prompt (`generate_screen_from_text`).
3. Iterate with edit/variant tools before export when quality is still exploratory.
4. Retrieve concrete artifacts (`get_screen`, HTML URL, image URL) and summarize what was produced.
5. If the user wants code integration, convert the generated result into implementation tasks (components, styling, responsive behavior).

## Prompting guidance

- Ask for one screen goal at a time (for example: "mobile onboarding", "desktop analytics dashboard").
- Include constraints: device type, tone/brand, layout priorities, required UI elements.
- Prefer explicit UX requirements over style-only prompts.

## Output style

- Report project ID and screen ID when available.
- Provide generated asset links (HTML/image) clearly.
- Separate generated design facts from implementation suggestions.
- Call out unresolved risks (accessibility, responsiveness, content realism) before handoff.
