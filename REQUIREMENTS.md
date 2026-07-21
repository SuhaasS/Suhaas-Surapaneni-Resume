# Requirements

Compiling this resume needs a LaTeX install (`pdflatex`) plus these packages.

## Install

Mac, no LaTeX at all:

```bash
brew install --cask basictex
eval "$(/usr/libexec/path_helper)"   # or restart terminal
```

Then install packages (BasicTeX ships a minimal set, these aren't included):

```bash
sudo tlmgr update --self
sudo tlmgr install enumitem supertabular titlesec multirow fontawesome5 tools
```

`tools` bundle provides `tabularx` and `multicol`.

Already have MacTeX (full) instead of BasicTeX: skip all this, everything's bundled.

## Packages used (from the .tex `\usepackage` lines)

url, parskip, xcolor, geometry, tabularx, enumitem, supertabular, titlesec, multicol, multirow, hyperref, fontawesome5

## Verify

```bash
pdflatex -interaction=nonstopmode "Suhaas Surapaneni Resume.tex"
```

No `! LaTeX Error` lines in output means good. Or just run the `build-resume` skill.
