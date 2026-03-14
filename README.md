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
npx skills add multicul-silver-wolf/sawana-multicul-skills --skill project-memory-system
```

## Skills in this repo

### 1) official-docs-to-mdx

Path: `skills/official-docs-to-mdx`

Convert official docs URLs into clean local `.mdx` snapshots with normalized frontmatter (`title`, `description`, `sourceUrl`, `retrievedAt`).

Use it when you need to:
- mirror official docs into your local knowledge base
- prepare stable markdown/mdx input for RAG
- refresh docs snapshots reproducibly from upstream URLs

### 2) browser-operation-guard

Path: `skills/browser-operation-guard`

Enforce a consistent browser workflow for manual and automated web tasks:
- always open/attach browser via OpenClaw browser tooling first (credential/session reuse)
- perform page interactions with agent-browser workflow
- when errors happen, run `--help` first before retrying

### 3) project-memory-system

Path: `skills/project-memory-system`

Bootstrap and maintain repository memory conventions around `AGENTS.md`, `MEMORY.md`, and `.memory/*.md`:
- set up or audit layered memory files for long-term and domain-specific knowledge
- keep `.memory/index.md` and `.memory/template.md` consistent with actual domain files
- record durable user corrections and reusable project decisions in the right memory layer

## Quick usage prompt examples

```text
Use official-docs-to-mdx to snapshot https://docs.convex.dev/agents/agent-usage into docs/convex/agent-usage.mdx with clean frontmatter.
```

```text
Use project-memory-system in this repo. Audit AGENTS.md / MEMORY.md / .memory, then bootstrap missing files and sync .memory/index.md.
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
