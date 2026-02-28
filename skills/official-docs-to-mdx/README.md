# official-docs-to-mdx

Turn official docs URLs into clean local `.mdx` snapshots for knowledge bases and RAG.

## Install

From this repository:

```bash
npx skills add multicul-silver-wolf/sawana-multicul-skills --skill official-docs-to-mdx
```

After indexing on skills.sh, this skill can be discovered under:

- `multicul-silver-wolf/sawana-multicul-skills@official-docs-to-mdx`

## What this skill does

- Fetches documentation via `markdown.new`
- Converts output to normalized `.mdx`
- Preserves useful frontmatter:
  - `title`
  - `description`
  - `sourceUrl`
  - `retrievedAt` (UTC date)
- Allows deterministic refresh by rerunning the same command

## Usage

```bash
scripts/mdnew_to_mdx.sh <source_url> <output_mdx_path>
```

Example:

```bash
scripts/mdnew_to_mdx.sh \
  https://docs.convex.dev/agents/agent-usage \
  docs/convex/agent-usage.mdx
```

## Good fit for

- Mirroring official docs to local project docs
- Building stable MDX inputs for RAG pipelines
- Keeping timestamped snapshots for reproducible updates

## Output contract

Generated MDX includes frontmatter:

- `title`
- `description`
- `sourceUrl`
- `retrievedAt`

## Included files

- `SKILL.md` — trigger/behavior definition for agents
- `scripts/mdnew_to_mdx.sh` — converter script
- `references/mdnew_to_mdx.md` — cleanup + implementation notes

## Notes

- Dependencies: `bash`, `curl`, `awk`, `mktemp`
- Existing output file is overwritten
- For folder-style docs, keep an `index.mdx` for better navigation/ingestion
