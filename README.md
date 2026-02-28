# sawana-multicul-skills

Battle-tested AI skills by **multicul-silver-wolf**.

This repository is structured for direct discovery/install via **skills.sh** and `npx skills add`.

## Install

Install all skills from this repo:

```bash
npx skills add multicul-silver-wolf/sawana-multicul-skills
```

Install a specific skill:

```bash
npx skills add multicul-silver-wolf/sawana-multicul-skills --skill official-docs-to-mdx
```

## Skills in this repo

### 1) official-docs-to-mdx

Path: `skills/official-docs-to-mdx`

Convert official docs URLs into clean local `.mdx` snapshots with normalized frontmatter (`title`, `description`, `sourceUrl`, `retrievedAt`).

Use it when you need to:
- mirror official docs into your local knowledge base
- prepare stable markdown/mdx input for RAG
- refresh docs snapshots reproducibly from upstream URLs

## Quick example

```bash
scripts/mdnew_to_mdx.sh \
  https://docs.convex.dev/agents/agent-usage \
  docs/convex/agent-usage.mdx
```

## Repository structure

```text
skills/
  <skill-name>/
    SKILL.md            # required
    scripts/            # optional
    references/         # optional
    assets/             # optional
```

## Compatibility

Designed to work with agents supported by the `skills` ecosystem (for example: OpenClaw, Codex, Cursor, Claude Code, OpenCode).

## Curated external skills

See [CURATED_SKILLS.md](./CURATED_SKILLS.md).

## Maintainer

- GitHub: [@multicul-silver-wolf](https://github.com/multicul-silver-wolf)

## License

MIT
