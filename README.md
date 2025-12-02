# DATAGODZILLA Research Hub

A unified research and ML projects hub for daily blog publishing to GitHub Pages.

## Overview

This project combines:
- **Clinical Research** - Healthcare informatics, interoperability standards, clinical workflows
- **ML Projects** - Proof-of-concept machine learning projects with demos

All content is organized by date and automatically publishable to [datagodzilla.github.io](https://datagodzilla.github.io).

## Quick Start

### Daily Research Workflow

```bash
# 1. Create today's research folder
/daily-research "topic-name"

# 2. Add source materials to sources/
# 3. Run analysis
/research-start-analysis path/to/folder

# 4. Review and edit blog-post/draft.md
# 5. Finalize as blog-post/final.md

# 6. Queue for publishing
/queue-for-publish path/to/final.md

# 7. Publish to GitHub Pages
/daily-publish
```

### ML Project Workflow

```bash
# 1. Create ML project folder
/daily-research "project-name" --type ml

# 2. Develop in notebooks/ and src/
# 3. Save models to models/
# 4. Create demo in demo/
# 5. Generate blog post and publish
```

## Folder Structure

```
DATAGODZILLA/
├── .claude -> ~/agent-ai/profiles/research-hub/.claude
├── .github/
│   └── workflows/
│       ├── sync-to-blog.yml        # Auto-publish to GitHub Pages
│       └── daily-reminder.yml      # Daily publishing reminder
│
├── research/                        # Clinical research
│   └── YYYY/MonthName/DD/NN-topic/
│       ├── sources/                 # PDFs, docs, images, URLs
│       ├── parsed/                  # Parsed documents
│       ├── analysis/                # Generated analysis
│       ├── visualizations/          # Mind maps, diagrams
│       ├── blog-post/               # Draft and final posts
│       └── README.md
│
├── ml-projects/                     # ML POC projects
│   └── YYYY/MonthName/DD/NN-project/
│       ├── data/                    # Raw, processed, features
│       ├── notebooks/               # Jupyter notebooks
│       ├── src/                     # Source code
│       ├── models/                  # Trained models
│       ├── experiments/             # Experiment tracking
│       ├── visualizations/          # Charts, plots
│       ├── demo/                    # Streamlit/Gradio app
│       ├── blog-post/               # Project blog post
│       └── README.md
│
├── publish/                         # Publishing workflow
│   ├── queue/                       # Posts ready to publish
│   ├── published/                   # Archive of published
│   └── schedule.yml                 # Publishing calendar
│
├── shared/                          # Shared resources
│   ├── images/
│   ├── templates/
│   └── references/
│
├── logs/                            # Activity logs
│   ├── research/
│   ├── publishing/
│   └── sessions/
│
└── README.md                        # This file
```

## Date-Based Naming

All content uses the format: `YYYY/MonthName/DD/NN-topic/`

- **YYYY**: Year (2025)
- **MonthName**: Full month name (December)
- **DD**: Day with leading zero (02)
- **NN**: Post number for the day (01, 02, etc.)
- **topic**: URL-friendly slug

Examples:
```
research/2025/December/02/01-fhir-lab-orders/
research/2025/December/02/02-snomed-terminology/
ml-projects/2025/December/03/01-clinical-text-classifier/
```

## Available Commands

| Command | Description |
|---------|-------------|
| `/daily-research "topic"` | Create new research folder for today |
| `/daily-research "topic" --type ml` | Create new ML project folder |
| `/research-start-analysis path` | Run full analysis pipeline |
| `/research-summarize path` | Generate quick summary |
| `/research-generate-mindmap path` | Create mind maps |
| `/research-generate-blog-post path` | Generate blog post |
| `/queue-for-publish path` | Add post to publish queue |
| `/daily-publish` | Publish queued posts |
| `/research-github-publisher path` | Direct publish to GitHub Pages |

## GitHub Pages Publishing

### Two-Repository Architecture

1. **Research Storage**: `datagodzilla/research-hub`
   - All research artifacts
   - Full project history

2. **Blog Publishing**: `datagodzilla/datagodzilla.github.io`
   - Published blog posts
   - URL: https://datagodzilla.github.io

### Automatic Publishing

When posts are added to `publish/queue/`:
1. GitHub Actions syncs to the blog repo
2. Jekyll builds the site
3. Posts go live at datagodzilla.github.io

### Manual Publishing

```bash
/daily-publish --all
```

## CLI Aliases

Add to `~/.zshrc`:

```bash
alias dg="cd ~/00_PROJECTS/DATAGODZILLA"
alias daily-research="cd ~/00_PROJECTS/DATAGODZILLA && claude '/daily-research'"
alias daily-publish="cd ~/00_PROJECTS/DATAGODZILLA && claude '/daily-publish'"
alias research-status="cat ~/00_PROJECTS/DATAGODZILLA/publish/schedule.yml"
alias queue-status="ls -la ~/00_PROJECTS/DATAGODZILLA/publish/queue/"
```

## Categories & Tags

### Clinical Research
- **Category**: `clinical`
- **Tags**: fhir, hl7, loinc, snomed-ct, ehr, healthcare, interoperability

### ML Projects
- **Category**: `ml-projects`
- **Tags**: nlp, classification, deep-learning, computer-vision, python

## Agents

This profile includes 14 specialized agents:

### Research Agents
- `research-master` - Orchestrates complete analysis workflows
- `research-doc-parser` - Parses documents (PDF, DOCX, etc.)
- `research-ai-expert` - AI/ML technical analysis
- `research-clinical-expert` - Clinical healthcare expertise
- `research-mindmap-creator` - Visual knowledge structures
- `research-doc-generator` - Documentation generation
- `research-doc-formatter` - Professional formatting
- `research-blog-publisher` - Blog post optimization
- `research-github-publisher` - GitHub Pages publishing

### ML Agents
- `research-ml-design-engineer` - ML system design
- `research-ml-experiment-engineer` - Experiment management
- `research-ml-data-engineer` - Data pipeline development
- `research-ml-model-engineer` - Model development
- `research-mlops-engineer` - Deployment and operations

## Setup

### Prerequisites
- Claude Code CLI installed
- GitHub CLI (`gh`) authenticated
- Access to `datagodzilla/datagodzilla.github.io`

### Configuration

1. **Create GitHub Personal Access Token** with repo access
2. **Add as repository secret** named `BLOG_DEPLOY_TOKEN`
3. **Verify GitHub Pages** is enabled on master branch

### First Run

```bash
cd ~/00_PROJECTS/DATAGODZILLA
/daily-research "my-first-topic"
```

## Contributing

1. Create research in `research/` or `ml-projects/`
2. Use the analysis commands to generate content
3. Queue and publish via `/daily-publish`

## License

Private research repository. All rights reserved.
