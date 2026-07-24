# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Build

Compile the PDF from the `.tex` source:

```bash
pdflatex "Suhaas Surapaneni Resume.tex"
```

Run twice if cross-references change. Generated files (`.aux`, `.log`, `.out`) are build artifacts and should not be committed.

## Hard Rules

- **One page only.** The resume must never exceed one page. Cut or condense content before letting it spill.
- **One line per bullet.** A bullet point must never wrap to a second line. Each bullet may be at most ~104 characters (visible output only, LaTeX commands don't count). 
- **ATS optimization.** Use industry-standard keywords throughout (e.g. specific languages, frameworks, tools, and methodologies). Avoid graphics, tables, or formatting that ATS parsers can't read for content. Spell out acronyms at least once where possible.
- **No aesthetic changes without explicit request.** Font, font size, spacing, margins, layout, and any other visual/formatting properties must never be changed unless the user explicitly asks. Content edits only.
- **Compile and view after every change.** After completing any edit, run `pdflatex "Suhaas Surapaneni Resume.tex"` and open the PDF to visually verify layout, line wrapping, and page count all meet requirements before reporting the task as done.

## Structure

Single-file LaTeX resume (`Suhaas Surapaneni Resume.tex`). Key custom environments defined in the preamble:

- `jobshort{title}{date}` — one-liner entry with no bullet points
- `joblong{title}{date}` — entry with a `--`-prefixed bullet list (`\item`)

Sections in order: Summary, Skills, Work Experience, Projects, Education.

## Conventions

- Dates use the format `Mon YYYY` or `Mon YYYY -- Mon YYYY` (e.g., `June 2025 -- Sept 2025`)
- Escape percent signs as `\%` in bullet text
- Skills table uses two columns: bold label + value, separated by `&`, with `\\[2pt]` row spacing
- Education table uses `date & description \hfill (detail)` layout
