# Project AI Brief

## Rules

- At the start of each session, load:
  - `README.md`
  - `PROJECT_REPORT.md`
  - `literature/LITERATURE_REVIEW.md`
  - the two most recent notes in `logs`

- Each time this file is loaded at the start of a session, run `python3 scripts/update_readme_structure.py` before relying on the folder structure documented in `README.md`.

- Use `AGENTS.md` as the single source of truth for AI guidance documents.

- `CLAUDE.md` must be a symbolic link to `AGENTS.md` (create/update with `ln -sf AGENTS.md CLAUDE.md`).

- Use these naming conventions unless the project explicitly defines a stricter one:
  - Analysis scripts: `YYYY-MM-DD_study{N}_{analysis-type}_v{NN}.{ext}`
    - Example: `2026-03-11_study2_mediation-analysis_v01.R`
  - Draft files: `YYYY-MM-DD_{journal-name}_draft_v{NN}.{ext}`
    - Example: `2026-03-11_JCR_draft_v03.docx`
  - Meeting notes: `YYYY-MM-DD_meeting_{attendee-initials}.{ext}`
    - Example: `2026-03-11_meeting_YY-TL-GT.md`
  - Log files: `YYYY-MM-DD.{ext}`
    - Example: `2026-03-11.md`
  
- Update `PROJECT_REPORT.md` when project stage, literature decisions, theory structure, conceptual model, hypotheses, empirical package, analysis method, or next steps change. Keep literature content there at summary level only.

- Update `literature/LITERATURE_REVIEW.md` when search scope, paper screening, synthesis, tensions in the literature, reading queue, or paper notes change.

- Update `MEASURES.md` when variables, measures, source citations, coding rules, aggregation rules, or sample/wave usage change.
- update `Logs` when the conversation is complete. 

## Custom Rules

Do not modify the rules above. Add all new project-specific rules below this line.

### Word Manuscript Revision Rule

- Do not revise manuscripts in Word Track Changes mode. Instead, create a new edited Word document and make direct edits there, so the user can later use Word's Compare/Combine features to generate the reviewed version.
- Preserve the manuscript's argument structure while improving local and paragraph-level coherence.
- Pay particular attention to context continuity, transition sentences, logical flow, and whether each revision supports the surrounding argument.
- Prefer clear, concise sentence structures; reduce unnecessarily complex sentences and avoid overusing passive voice.
- Preserve Zotero citation fields. Do not flatten, unlink, retype, or manually rewrite citation text; fix citations through Zotero or remove them.

### Literature Management Rule

- For core literature, locate the source PDF from the local Zotero library when available.
- Convert core literature PDFs into Markdown using MinerU or another appropriate PDF-to-Markdown/OCR tool; prefer direct text extraction for machine-readable PDFs and OCR for scanned PDFs.
- Save the converted Markdown files under `literature/` with clear filenames that include author, year, and short title when possible.

### R Script Rule

- Write R work as complete runnable `.R` scripts rather than REPL or console fragments.
- Accept inputs through `commandArgs(trailingOnly = TRUE)` and avoid manual input, menus, the Viewer pane, or RStudio-specific features.
- Use Linux/WSL paths and write reusable outputs explicitly to project files.
- On failure, print a useful error message to stderr and exit with `quit(status = 1)`.
