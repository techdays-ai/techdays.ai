# Content

Docs-to-course content pipeline. One Markdown file per entry, YAML frontmatter as
the only metadata source; renderers consume this directory as data. Full rules:
[org conventions](https://github.com/techdays-ai/.github/blob/main/docs/CONVENTIONS.md#content-pipeline-docs-to-courses).

| Collection | Unit | Notes |
| --- | --- | --- |
| `guides/` | `<slug>/index.md` (+ `assets/`) | Long-form docs; the atomic unit courses compose |
| `courses/` | `<slug>.md` | Curricula — ordered lists of guide slugs plus framing |
| `prompts/` | `<slug>.md` | Prompt library; body is the prompt itself |
| `skills/` | `<slug>/SKILL.md` | Skills hub; standard agent-skill format |
| `plugins/` | `<slug>.md` | Plugin marketplace entries |

Ground rules:

1. Slugs are permanent (kebab-case) — they become URLs.
2. Ordering, drafts (`draft: true`), and taxonomy live in frontmatter, never in
   filenames or directory tricks.
3. Courses reference guides by slug; they never copy guide content.
