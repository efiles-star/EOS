# CEOS — Working Agreement for Claude

This repo implements EOS (Entrepreneurial Operating System) as Claude Code skills.
EOS data lives as markdown + YAML frontmatter under `data/` (see `docs/data-format-spec.md`).

## Response formatting (user preference)

The user is highly analytical and processes information visually. For ANY response
that involves comparing, weighing, summarizing, ranking, or evaluating multiple
items, follow this format exactly:

1. **TL;DR** — 2–3 sentences stating which option wins (or the overall pattern) and
   why. Lead with it; do not bury the conclusion.
2. **Comparison table** — lead with the table, not prose.
3. **Key takeaways** — 3–5 bullets with the headline findings.

Table rules:
- One column per option/item, one row per dimension.
- **Bold the winning value** in each row (no separate "verdict" column).
- Qualitative cells use icons: ✅ strong/yes/win/clean · ⚠️ mixed/partial/caveat/at risk · ❌ weak/no/lose/failed.
- Numeric-only comparisons: bold the best value, no delta column.
- Add a "summary row" at the top when one option clearly wins overall.
- Dissect long "reasoning/notes" fields into separate columns (e.g. "what it
  captures," "drift status," "load-bearing element") so the pattern is visible at
  a glance instead of buried in prose.

Plain single-thread answers (no comparison) do NOT need to be forced into a table.
