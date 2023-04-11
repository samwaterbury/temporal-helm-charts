# Temporal Helm Charts

This repository publishes Helm charts for Temporal.

## Usage

To use the charts, first add the repository:

```bash
helm repo add temporal-unofficial https://samwaterbury.github.io/temporal-helm-charts
```

Then you can install the charts as you normally would:

```bash
helm install temporal temporal-unofficial/temporal
```

## Development

### How it Works

The original charts can be found in Temporal's [`helm-charts`](https://github.com/temporalio/helm-charts) repository. They are downloaded and copied into the `charts/temporal` directory and then published via GitHub Actions. The artifacts are published as GitHub releases and an `index.yaml` is created on the `gh-pages` branch of this repository, allowing the GitHub Pages site to constitute as a Helm repository.

### Updating the Charts

To update the charts, first fetch the latest updates from the `helm-charts` repository:

```bash
./scripts/fetch_latest
```

Then commit the changes and push to `main`. The GitHub Actions workflow will publish the charts to GitHub Pages.
