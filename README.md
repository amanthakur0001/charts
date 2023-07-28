# Helm Charts

This is the Helm Charts repository.

## Setup

```bash
$ helm repo add amanthakur0001-charts https://amanthakur0001.github.io/charts
$ helm repo update

# Helm 2
$ helm install amanthakur0001-charts/my-first-chart

# Helm 3
$ helm install amanthakur0001-charts/my-first-chart --generate-name
```

## Documentation

The documentation for Kong's Helm Chart is available at
[here](https://github.com/Kong/charts/blob/main/charts/kong/README.md).

## Seeking help

If you run into an issue, bug or have a question, please reach out to the Kong
community via [Kong Nation](https://discuss.konghq.com) or open Github
issues in [this](https://github.com/kong/charts/issues) repository.

## Releasing and forking

This repo uses [chart releaser](https://github.com/helm/chart-releaser-action/)
to automatically update a GitHub pages branch containing a Helm repo. When you
[bump the `version` field in
Chart.yaml]
in one of the charts under `charts/` and merge to main, GitHub Actions will
trigger a release job to generate a GitHub release and add the new release to
the Helm repo:

1. Make a new branch and add a [release commit].
   This commit updates the Chart.yaml chart version, finalizes that version's changelog, and optionally adds upgrade instructions.
2. Open a PR to main and merge once approved.
3. Wait for CI to release the new version. Investigate errors if the release job fails.

Forks of this repo can use this release functionality without (much) additional
configuration. Enabling GitHub pages for the `gh-pages` branch will make a Helm
repo with your fork's changes available on your GitHub Pages URL. You can then
use this with:

```
helm repo add amanthakur0001-charts https://myuser.github.io/charts/
```