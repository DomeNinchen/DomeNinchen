# Installation — DomeNinchen GitHub Profile

This version recreates the ORIGINAL dark mockup using local SVG panels. It is not a new page layout. GitHub README files do not support arbitrary CSS containers, so the cards are images, while the project links remain clickable Markdown badges. Unlike a full website, exact native Markdown layout rendering is not possible.

## Install via pull request

1. Create a branch in `DomeNinchen/DomeNinchen`.
2. Copy **all** files, including `assets/` and `.github/workflows/metrics.yml`, to the profile repository root.
3. Open a pull request, review and merge into `main`.
4. GitHub will load the local SVG panels automatically, including the rotating terminal status text (animation support depends on the browser and GitHub renderer).

## Enable developer metrics

1. Inspect `.github/workflows/metrics.yml` and the upstream project [lowlighter/metrics](https://github.com/lowlighter/metrics), especially token permissions.
2. Create a GitHub PAT with only the permissions necessary to gather your chosen metrics. Store it in the profile repo Actions secrets as `METRICS_TOKEN`. Never commit the token.
3. Enable Actions to create pull requests where repository policy permits it.
4. Trigger **Generate Developer Metrics** manually in the Actions tab after the workflow is merged.
5. Review and merge the generated PR containing `github-metrics.svg`.
6. Scheduled refreshes also create PRs; merge after reviewing.

**Notes:** The stats image will not appear before `github-metrics.svg` exists. SVG styling is baked into assets; users may use a light GitHub theme around the cards. Text embedded in SVGs is not selectable as README text. Metrics rely on the upstream action, and badges rely on Shields.io.
