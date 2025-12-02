# Healthcare Interoperability Basics

**Date:** 2025-12-02
**Type:** Research
**Status:** Example

## Overview

This is an example research folder demonstrating the folder structure for the Research Hub daily publishing workflow.

## Folder Structure

```
01-healthcare-interoperability-basics/
├── sources/           # Input materials
│   ├── pdfs/          # PDF documents
│   ├── docs/          # Word documents
│   ├── images/        # Source images
│   └── urls.md        # Reference URLs
├── parsed/            # Parsed document outputs
├── analysis/          # Generated analysis
│   ├── clinical-workflow.md
│   ├── technical-workflow.md
│   └── summary.md
├── visualizations/    # Mind maps and diagrams
│   ├── mindmap-concept.md
│   ├── mindmap-process.md
│   └── diagrams/
├── blog-post/         # Blog drafts and finals
│   ├── draft.md
│   ├── final.md
│   └── metadata.yml
└── README.md          # This file
```

## Workflow

1. Add source materials to `sources/`
2. Run `/research-start-analysis` on this folder
3. Review generated analysis in `analysis/`
4. Edit `blog-post/draft.md` and finalize as `blog-post/final.md`
5. Run `/queue-for-publish` to add to the publish queue
6. Run `/daily-publish` to publish to GitHub Pages

## Sources

- [Add your source materials here]

## Key Findings

[To be completed after analysis]

## Blog Post

See [blog-post/final.md](blog-post/final.md) for the publication-ready article.
