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
- **One line per bullet.** A bullet point must never wrap to a second line. Empirically measured at the current font/margins: 113 characters is the exact wrap boundary (visible output only, LaTeX commands don't count); stay at or under 110 characters as a safety margin, since exact width varies with which characters are used (proportional font). Always confirm by compiling and viewing — see the rule below.
- **ATS optimization.** Use industry-standard keywords throughout (e.g. specific languages, frameworks, tools, and methodologies). Avoid graphics, tables, or formatting that ATS parsers can't read for content. Spell out acronyms at least once where possible.
- **No aesthetic changes without explicit request.** Font, font size, spacing, margins, layout, and any other visual/formatting properties must never be changed unless the user explicitly asks. Content edits only.
- **Compile and view after every change.** After completing any edit, run `pdflatex "Suhaas Surapaneni Resume.tex"` and open the PDF to visually verify layout, line wrapping, and page count all meet requirements before reporting the task as done.

## Structure

Single-file LaTeX resume (`Suhaas Surapaneni Resume.tex`). Key custom commands defined in the preamble:

- `\resumeItem{text}` — a single bullet line
- `\resumeSubheading{title}{date}{subtitle}{subdate}` — two-row entry header: bold title + date on row 1, italic subtitle + subdate on row 2. Used for Experience and Education entries.
- `\resumeProjectHeading{name/type}{date}` — one-row header for Projects entries (name and type on the left, date on the right)
- `\resumeSubSubheading{subtitle}{subdate}` / `\resumeSubItem{text}` — defined but currently unused
- `\resumeSubHeadingListStart` / `\resumeSubHeadingListEnd` — wraps a section's list of entries
- `\resumeItemListStart` / `\resumeItemListEnd` — wraps an entry's bullet list

Sections in order: Summary, Experience, Projects, Technical Skills, Education.

## Conventions

- Dates use the format `Mon YYYY` or `Mon YYYY -- Mon YYYY` (e.g., `June 2025 -- Sept 2025`), except Projects headings which currently use the abbreviated `Mon YYYY` form (e.g., `Jul 2025 -- Aug 2025`)
- Escape percent signs as `\%` in bullet text
- Technical Skills section is one itemize item containing labeled lines (`\textbf{Label}{: value}`), separated by `\\`
- Education entries use `\resumeSubheading` like Experience: institution + dates on row 1, degree + GPA/detail on row 2
