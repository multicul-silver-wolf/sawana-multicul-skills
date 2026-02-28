# sawana-multicul-skills

Minimal skill repository for Sawana/Multicul.

## Structure

- `skills/official-docs-to-mdx/` — download and normalize official documentation pages into local `.mdx` files.

## Conventions

- One skill per folder under `skills/`
- Each skill must include `SKILL.md`
- Keep scripts/resources inside the skill folder
- Keep this repo minimal and easy to publish/update via ClawHub

## Publish (example)

```bash
clawhub publish ./skills/official-docs-to-mdx \
  --slug sawana-multicul-official-docs-to-mdx \
  --name "sawana-multicul/official-docs-to-mdx" \
  --version 1.0.0
```
