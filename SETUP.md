# Profile setup — DomeNinchen

Place `README.md` and `.github/workflows/metrics.yml` in the **DomeNinchen/DomeNinchen** repository using a feature branch and a pull request.

## Enable Developer Metrics

1. Create a GitHub personal access token for metrics. For public-only metrics, use the least privileges supported by the metrics project and your selected token type. Do not commit the token.
2. In the profile repository, add it under **Settings → Secrets and variables → Actions → New repository secret**, named `METRICS_TOKEN`.
3. In **Settings → Actions → General → Workflow permissions**, allow GitHub Actions to create pull requests, if necessary. Repository / organization policy may override this setting.
4. Merge the README and workflow PR, then manually run **Generate Developer Metrics** using **Actions → Run workflow**.
5. Review and merge the generated metrics pull request. The `github-metrics.svg` image will then appear on your profile.
6. Weekly subsequent runs generate PRs for metrics updates; review and merge them rather than committing directly to main.

The terminal header uses external services (`capsule-render.vercel.app` and `readme-typing-svg.demolab.com`), and badges use `img.shields.io`. If a service goes offline, the corresponding graphic may be unavailable. The custom dark styling is for embedded assets; GitHub's surrounding page is controlled by the viewer's theme.

The `lowlighter/metrics@latest` action is a floating release reference. For higher supply-chain assurance, pin the action to a reviewed commit SHA and periodically update it.
