# Research Project Structure Template

This repository is a reusable skeleton for empirical research projects. `README.md` is the structure reference for the repository: it documents root files, directory purposes, and naming conventions.

## Required Root Files

- `AGENTS.md`: AI-facing project brief and operating rules for tools that read `AGENTS.md`.
- `CLAUDE.md`: symbolic link to `AGENTS.md` for tools that read `CLAUDE.md`.
- `PROJECT_REPORT.md`: research-progress summary covering project status, active theory decisions, empirical package, and current status.
- `MEASURES.md`: variable and measure registry, with sources and operationalization notes.
- `README.md`: repository structure reference and naming guide.

## Directory Purposes

- `compliance/`: IRB, consent, preregistration, DMP, and related governance materials.
- `literature/`: literature review source files, synthesis documents, and reading notes. Keep the main literature synthesis in `literature/LITERATURE_REVIEW.md`.
- `logs/`: dated project logs and the daily log template.
- `meetings/`: meeting notes and the meeting template.
- `presentation/`: conference, workshop, PDW, and internal presentation assets.
- `scripts/`: helper scripts for project health checks and repository-structure maintenance.
- `studies/`: study-level packages for active empirical work.
- `studies/archive/`: archived pilots, dropped studies, and mixed legacy materials.
- `submission/`: submission logs, journal-specific requirements, revision rounds, and reusable submission templates.
- `writing/`: manuscript drafts and reusable writing templates.

## Working Rules

- Keep `PROJECT_REPORT.md` lean. It should summarize only the literature decisions that currently affect theory, hypotheses, design, or next steps.
- Put detailed literature extraction, synthesis, contradictions, and reading queues in `literature/LITERATURE_REVIEW.md`.
- If literature notes become paper-specific and long, create files under `literature/notes/` and keep `literature/LITERATURE_REVIEW.md` as the synthesis layer.

## Directory Tree

This block is the only auto-generated section in `README.md`.
Its update position is fixed between the `BEGIN DIRECTORY TREE` and `END DIRECTORY TREE` markers.

<!-- BEGIN DIRECTORY TREE -->
```text
.
|-- compliance/
|   |-- consent/
|   |   `-- .gitkeep
|   |-- dmp/
|   |   `-- .gitkeep
|   |-- irb/
|   |   `-- .gitkeep
|   |-- other/
|   |   `-- .gitkeep
|   `-- preregistration/
|-- literature/
|   `-- LITERATURE_REVIEW.md
|-- logs/
|   `-- daily_log_template.md
|-- meetings/
|   |-- .gitkeep
|   `-- meeting_template.md
|-- presentation/
|   |-- conferences/
|   |   `-- .gitkeep
|   |-- internal/
|   |   `-- .gitkeep
|   |-- pdws/
|   |   `-- .gitkeep
|   `-- workshops/
|       `-- .gitkeep
|-- scripts/
|   |-- check_project_health.py
|   `-- update_readme_structure.py
|-- studies/
|   |-- archive/
|   |   `-- README.md
|   |-- study-01-field/
|   |   |-- analysis/
|   |   |-- data/
|   |   |-- design/
|   |   |-- materials/
|   |   |-- outputs/
|   |   `-- README.md
|   `-- study-02-experiment/
|       |-- analysis/
|       |-- data/
|       |-- design/
|       |-- materials/
|       |-- outputs/
|       `-- README.md
|-- submission/
|   |-- journal-specific/
|   |-- revision-rounds/
|   |   |-- r1/
|   |   |-- r2/
|   |   `-- r3/
|   |-- shared-templates/
|   |   |-- AOM manuscript template.md
|   |   |-- APA 7th cover letter template.md
|   |   |-- APA 7th manuscript template.md
|   |   `-- APA 7th title page template.md
|   `-- SUBMISSION_LOG.md
|-- writing/
|   |-- drafts/
|   |   `-- .gitkeep
|   `-- templates/
|       `-- .gitkeep
`-- Migration Playbook.md
```
<!-- END DIRECTORY TREE -->
