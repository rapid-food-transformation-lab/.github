# CLAUDE.md — rapid-food-transformation-lab GitHub Organisation

## Project overview

This repository (`.github`) hosts the public-facing profile for the **Rapid Food Transformation Lab** GitHub Organization at the Oxford Martin School, University of Oxford. The lab is led by Professor Paul Behrens and focuses on how food, energy, and economic systems can transform rapidly enough to avoid the worst climate impacts.

The primary file here is `profile/README.md` — the markdown document that appears on the organisation's GitHub landing page at https://github.com/rapid-food-transformation-lab.

## Organization structure

### Teams
```
rapid-food-transformation-lab (org)
├── @core-admin         — PI + lab manager + 2 senior postdocs (Admin)
├── @research-leads     — Project leads (project management)
├── @researchers        — All internal Oxford researchers
├── @external-collaborators  — Trusted long-term external members
└── [outside collaborators] — Repo-level only, via "Outside collaborators"
```

### Repositories

| Repo | Visibility | Purpose |
|---|---|---|
| `.github` | Public | This repo — org profile README |
| `lab-docs` | Public | Lab objectives, paper annotations, high-level documentation |
| `lab-notes-vault` | Private | Obsidian vault — meeting notes, literature, working thoughts |
| `lab-template` | Public | Standard project scaffold with CLAUDE.md, meta/, docs/ |
| `teaching` | Public | Workshop and course materials |

Project-specific repos follow the naming convention:
- `{project}-project` — private WIP research project
- `{project}-paper` — public reproduction package (on submission)
- `raft-{toolname}` — shared R packages, Python libraries, pipelines

## Standard repository structure

All project repos are scaffolded from `lab-template` and follow this structure:

```
{project}-analysis/
├── CLAUDE.md                  # AI context: project summary, data locations, pipeline entry points
├── README.md
├── src/
│   ├── r/
│   ├── python/
│   └── shared/                # YAML configs, shared schemas
├── docs/
│   └── links.md               # e.g. Obsidian or note links
├── meta/
│   └── dataset.yaml           # Dataset versions, SHA256 checksums, paths
├── outputs/                   # Figures, tables (gitignored if large)
└── .github/

```

## Data infrastructure

- **Large datasets** (FABIO, EXIOBASE and other MRIO files): stored on OneDrive (internal) or Zenodo (public archiving) — never committed to git
- **Dataset versioning:** tracked in `meta/dataset.yaml` with SHA256 checksums

## Key conventions

- All repos include a `CLAUDE.md` at root with project-specific AI context
- Branch protection on `main` is relaxed (PRs optional); linear history preferred
- Base org permissions: Read — Write granted via teams only
- Repo creation restricted to `core-admin`
- Outside collaborators added at repo level only, never as org members (unless elevated to `external-collaborators` team)
- UK English throughout all documentation
- Open science defaults: public on publication, private during WIP

## Current setup status

This organisation is in active setup. The following has been configured:
- [x] Org created and profile description set
- [x] Base permissions set to Read
- [x] 2FA enforcement enabled
- [x] Four teams created: `core-admin`, `research-leads`, `researchers`,  `external-collaborators`
- [ ] Repositories created and scaffolded
- [ ] Team permissions assigned per repo
- [ ] Org profile README published (`profile/README.md` — must be at this path for GitHub to render it)
- [ ] `lab-template` populated with standard scaffold
