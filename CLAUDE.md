# Claude Artifacts Gallery

This repo stores all Claude-created static artifacts, browsable via GitHub Pages.

## How to Add an Artifact

1. Save the artifact to `artifacts/YYYY-MM-DD-slug/index.html` (must be a fully self-contained HTML file — all CSS and JS inline or in the same folder)
2. Add an entry to `artifacts/manifest.json`
3. Stage and commit both files

## Manifest Entry Format

```json
{
  "slug": "YYYY-MM-DD-kebab-case-title",
  "title": "Human-readable title",
  "description": "One-sentence description of what this artifact does",
  "date": "YYYY-MM-DD",
  "path": "artifacts/YYYY-MM-DD-slug/index.html"
}
```

## Naming Convention

Slug format: `YYYY-MM-DD-kebab-case-description`

Example: `2026-03-04-color-playground`

## Rules

- **Never modify** the gallery `index.html` structure or `manifest.json` array format
- Only **append** new entries to the manifest array (do not reorder or remove existing entries)
- Every artifact must be **fully self-contained** (no external CDN dependencies)
- Use the **artifact-gallery** skill when creating new artifacts — it handles all registration steps automatically
