# Contoso company profile (workshop starter)

Starter code for the **GitHub Agent-Native Engineering System** workshop.
It is the public company profile website of **Contoso**, a fictional company: static pages built with Node.js and EJS templates, tested with `node:test`, and deployed to **GitHub Pages** by GitHub Actions.

> **Training material.** This starter deliberately ships with **one outdated dependency** and **one insecure legacy widget**, so the security chapters of the workshop (code scanning, Copilot Autofix, Dependabot) have something real to find and fix. Do not reuse this code in production.

## Quick start

1. **Use this template → Create a new repository** (public), for example `contoso-company-profile`.
2. In the new repository: **Settings → Pages → Build and deployment → Source: GitHub Actions**.
3. **Code → Codespaces → Create codespace on main**, then in the terminal:

   ```bash
   npm install          # creates package-lock.json
   npm test             # builds the site and runs the checks
   npm run build && npm run serve   # preview on port 8080
   ```

## Project layout

| Path | What it is |
| --- | --- |
| `src/pages/*.ejs` | One template per page (home, about, services, news, contact) |
| `src/partials/` | Shared head, header, footer and icons |
| `src/data/*.json` | Site content; each file becomes a template variable |
| `src/assets/` | CSS, JavaScript and SVG images |
| `build.mjs` | Renders the pages into `dist/` |
| `test/site.test.mjs` | Checks pages, headings, alt text and links |
| `.github/workflows/ci.yml` | Tests every pull request |
| `.github/workflows/deploy-pages.yml` | Deploys `dist/` to GitHub Pages on every push to `main` |
| `.github/copilot-instructions.md` | Project rules that Copilot follows (and code review checks) |
| `.devcontainer/` | Codespaces configuration (Node.js 22 + GitHub CLI) |

## Workshop guide

Step-by-step guide with real screenshots: https://ibranibeny.github.io/gh-agentic-engineering-workshop/
