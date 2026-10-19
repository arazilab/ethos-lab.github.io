# Hermes guide

This repository contains a static Astro version of the ETHOS Lab website. Hermes uses the lab's GitHub App and GitHub MCP tools to work with repository files. Keep changes small, use pull requests, and never commit directly to `main`.

## Project map

- `src/content/site.js` holds shared lab text and navigation labels.
- `src/content/research.js`, `team.js`, and `publications.js` hold page content.
- `src/components/` contains reusable page sections and elements.
- `src/layouts/SiteLayout.astro` contains the shared header, navigation, footer, and styles.
- `src/pages/` contains one Astro file per public page.

## Make a change

1. Read the current component and content data before editing.
2. For text or people updates, change the matching file in `src/content/` rather than copying markup into a page.
3. For a new repeated design element, add or extend a component in `src/components/`. Keep a short comment and a usage example with reusable component code.
4. Create a descriptive non-default branch, commit only the requested change, and open a pull request to `main`. Include a short summary and a screenshot for visual changes. Do not merge or change branch protection.
5. Check that the **Check website build / build** workflow passes on the pull request. If a local checkout is available inside `/srv/hermes-workspace`, run `npm ci` and `npm run build` there. Do not ask lab members to manage tokens or clone repositories for the GitHub MCP workflow.

## Example

To add a research area, add an object to `src/content/research.js` with `title` and `description` fields. `ResearchGrid.astro` renders the list automatically.

## Content and assets

- Preserve source meaning and names. Check current source details before changing time-sensitive people, publications, or links.
- Prefer locally stored, licensed assets. Do not copy private or restricted material.
- Keep images accessible with useful alternative text. Mark decorative images with empty alternative text.
- Use root-relative Astro asset helpers or normal relative links so assets work under `/ethos-lab.github.io/`.
- Keep keyboard focus visible, use semantic headings, and respect reduced-motion preferences.

## Pull request checklist

- The requested change is limited to its intended files.
- `npm run build` succeeds.
- Page links and local assets work under the GitHub Pages project path.
- The pull request explains what changed and how it was checked.
