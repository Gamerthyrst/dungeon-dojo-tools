# Dungeon Dojo Tools

Browser-based infographic builders for Dungeon Dojo. No install, no account, no server: each tool is a single self-contained HTML file that runs entirely in your browser.

**Live site:** https://gamerthyrst.github.io/dungeon-dojo-tools/

## Tools

### This Week Builder (`/whats-on-builder/`)
Builds the weekly announcement graphics:
- **This Week Digest** - topic-based sections (Raid, Mythic+, Collectors, Micro-Holidays, Timewalking, Notable News, or custom)
- **What's On - EU / NA** - day-by-day itinerary layout, NA includes dual ET/PT times

Sections can be shown, hidden, reordered, and re-themed (five built-in themes including the official Dungeon Dojo brand theme). Exports straight to PNG or JPG. Everything, including your uploaded logo, stays in the browser; nothing is uploaded anywhere.

### Feature Infographic Builder (`/feature-infographic-builder/`)
Builds landscape 1920×1080 spotlight infographics with 8 resizable panels, a central glowing orb, six panel colour themes, and per-panel images. Exports to PNG or JPG via html2canvas.

## Updating a tool

There's no build step, just replace the file:

1. Open the relevant folder in this repo (`whats-on-builder/` or `feature-infographic-builder/`)
2. Open `index.html`, click the pencil (edit) icon, and paste in the new version, or use **Add file -> Upload files** to overwrite it directly
3. Commit to `main`

GitHub Pages redeploys automatically, usually within a minute or two. If a change doesn't seem to have landed, hard-refresh (`Ctrl/Cmd+Shift+R`) or check the **Actions** tab to confirm the deploy finished.

## Repo structure

```
index.html                        ← landing page, links to both tools
whats-on-builder/index.html       ← This Week Builder
feature-infographic-builder/index.html   ← Feature Infographic Builder
```

## Notes

- Both tools embed the Dungeon Dojo logo directly in the HTML (as base64) rather than as a separate image file, so nothing breaks if a file goes missing.
- The Feature Infographic Builder previously shipped with a separate Word doc user guide. That guide predates the Dungeon Dojo theme, JPG export, and logo update added since, so treat this README as the current source of truth rather than that doc.
