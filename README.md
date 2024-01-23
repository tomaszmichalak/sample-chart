# Sample chart

## Goal
This chart is a sample chart to show how to release helm chart within GitHub.

## Run

Run from local chart:

```bash
helm install --name sample-chart .
```

Run the released chart:

```bash
helm repo add sample-chart https://tomaszmichalak.github.io/sample-chart
helm upgrade --install sample-chart sample-chart/sample-chart
```

or

```bash
helm upgrade --install release-name sample-chart --repo https://tomaszmichalak.github.io/charts --version 0.1.0
```

## Release

I use [chart-releaser](https://github.com/helm/chart-releaser) to release the chart. It is wrapped in [chart-releaser-action](https://github.com/helm/chart-releaser-action). More details in [release.yml](.github/workflows/release.yml).

The chart is released to [GitHub Pages](https://pages.github.com/) and can be accessed via https://tomaszmichalak.github.io/sample-chart/index.yaml.