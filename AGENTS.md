# Repository Guidelines

## Project Structure & Module Organization
This repository is a LaTeX manuscript with supporting PDFs.
- `qmul_probe_Latex/`: LaTeX source and bibliographies (`main.tex`, `mainNotes.bib`, `xxx.bib`) plus build artifacts (`main.pdf`, `.aux`, `.log`, `.bbl`).
- `probe_adv_Papers/`: reference papers (PDF only).
- `probe_adv_Notes/`: working notes (PDF only).
Treat PDFs as binary assets; edit only the LaTeX and `.bib` files in `qmul_probe_Latex/`.

## Build, Test, and Development Commands
Run these from `qmul_probe_Latex/`:
- `latexmk -pdf main.tex`: build the manuscript PDF with bibliography support.
- `latexmk -c`: clean auxiliary files.
- If `latexmk` is unavailable: `pdflatex main.tex && bibtex main && pdflatex main.tex && pdflatex main.tex`.

## Coding Style & Naming Conventions
- LaTeX: keep the preamble organized, use `\section{}`-based structure, and avoid inline formatting that complicates diff reviews.
- BibTeX keys follow `AuthorYear` (e.g., `Kubo1966`, `Clerk2010`); keep full metadata fields (title, journal, volume, pages, year, DOI, URL).
- Keep `main.tex` as the entry point; add new sources in `qmul_probe_Latex/` with descriptive names and update bibliographies accordingly.

## Testing Guidelines
There are no automated tests. Validation is the LaTeX build:
- Ensure `latexmk -pdf main.tex` completes without errors.
- Scan `main.log` for missing references or citation warnings before finalizing changes.

## Commit & Pull Request Guidelines
The Git history only contains `Initial commit`, so no established convention exists. Use short, imperative commit messages such as `Update abstract` or `Add citation for Kubo`.
For pull requests:
- Include a concise summary and the build command used.
- Mention whether `main.pdf` was regenerated and committed.
- Link related issues or references when applicable.
