---
name: browser-operation-guard
description: Enforce a consistent browser workflow for manual and automated web tasks. Use when any task requires opening a website, logging in, clicking/filling UI, scraping page data, screenshots, or browser troubleshooting. Always open/attach browser via OpenClaw browser tooling (so credentials/session can be reused), then execute interactions via the agent-browser skill. If any browser/tool command fails, run the corresponding --help command before retrying.
---

# Browser Operation Guard

## Workflow

1. Open browser context with OpenClaw browser tooling first.
2. Use `agent-browser` skill for all page interactions and automation.
3. Keep actions in the same browser tab/session unless task requires otherwise.
4. On any error, inspect command usage with `--help`, then retry with corrected arguments.

## Hard Rules

- Never start browser automation by ad-hoc scripts first; initialize browser through OpenClaw browser tooling.
- Prefer credential/session reuse from OpenClaw browser context.
- Use `agent-browser` skill as the default operator for click/type/navigate/snapshot/screenshot tasks.
- When a command fails, do not guess flags repeatedly. Run help first:
  - OpenClaw browser CLI/help for browser-side commands.
  - Agent-browser tool help for automation-side commands.

## Error-Handling Checklist

- Capture exact error text.
- Run the matching `--help` command.
- Verify required args/options, then rerun once.
- If still failing, report blocker + attempted commands + error output.

## Success Criteria

- Browser opens via OpenClaw path.
- Interaction runs via `agent-browser` skill.
- Errors are handled with `--help`-first debugging behavior.
