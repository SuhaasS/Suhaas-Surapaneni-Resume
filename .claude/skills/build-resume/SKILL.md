---
name: build-resume
description: Compile and open Suhaas Surapaneni's LaTeX resume in this repo. Use whenever the user asks to build, compile, render, preview, view, or open the resume, or wants to see how edits look, or says things like "compile my resume", "show me the PDF", "build and open it". Always run this after editing the .tex file so the user can visually verify layout, line wrapping, and page count per this repo's CLAUDE.md rules.
---

# Build Resume

Compiles `Suhaas Surapaneni Resume.tex` to PDF and opens it for visual review.

## Steps

1. From the repo root, run pdflatex twice (cross-references need a second pass):

```bash
pdflatex -interaction=nonstopmode "Suhaas Surapaneni Resume.tex"
pdflatex -interaction=nonstopmode "Suhaas Surapaneni Resume.tex"
```

2. Check the output for `! ` prefixed lines (LaTeX error marker). If present, stop and fix the `.tex` source before continuing — do not open a stale or broken PDF.

3. Open the resulting PDF:

```bash
open "Suhaas Surapaneni Resume.pdf"
```

4. Verify against this repo's CLAUDE.md hard rules: exactly one page, no bullet wraps to a second line. Report page count and flag any wrapped bullets you notice.

## Cleanup

Build artifacts (`.aux`, `.log`, `.out`) are gitignored/uncommitted per CLAUDE.md — leave them, don't commit them, no need to delete them either.
