# Gabriel Rodriguez — Résumé

Live site: <https://thagabe.github.io/>

A standalone HTML and CSS résumé with responsive layout and print styling.
No build step, JavaScript, package dependencies, external fonts, or third-party
asset requests are required.

Edit `index.html` for content and `styles.css` for presentation. Keep the files
together and open `index.html` in a browser to preview. Use Print → Save as PDF
for A4 or Letter output. The relative stylesheet URL also works in a subdirectory.

## Deployment

Push to `main` to run `.github/workflows/gh-pages.yml`, or run it manually from
the Actions tab. Pull requests check the files without publishing.

The workflow stages only `index.html`, `styles.css`, and `.nojekyll`, then
publishes them to the existing `gh-pages` branch with the built-in
`GITHUB_TOKEN`. GitHub Pages should remain configured under **Settings → Pages
→ Deploy from a branch → gh-pages → / (root)**. No custom secret is needed.
The `.nojekyll` marker tells Pages to serve the files without Jekyll processing.

`main` is the source of truth; do not edit the generated `gh-pages` branch.
Private interview/planning notes (`AGENT.md`) must stay outside this public
repository. README, workflow files, and Git metadata are excluded from the
published website.

## Refactoring

Replaced the previous Hugo/almeida-cv site with the standalone, print-focused
HTML/CSS résumé from the separate résumé workspace. Removed Hugo configuration,
theme submodule, YAML content, generated assets, and the Hugo build step.
Preserved the existing Git history and `gh-pages` publishing source, updated
the deployment actions, made write permission explicit only for deployment,
and added pull-request checks and a manual deployment trigger.

The résumé content and print styles were copied unchanged. Future public
updates belong in this repository. The older Hugo version remains available
in Git history before this refactor.
