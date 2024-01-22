# Sample chart

## Goal
This chart is a sample chart to show how to release helm chart within GitHub.


```bash
helm template --output-dir generated test .
helm install --name sample-chart .
```

## Release

I use [chart-releaser](https://github.com/helm/chart-releaser) to release the chart. It is wrapped in [chart-releaser-action](https://github.com/helm/chart-releaser-action). More details in [release.yml](.github/workflows/release.yml).

The chart is released to [GitHub Pages](https://pages.github.com/) and can be accessed via https://tomaszmichalak.github.io/sample-chart/index.yaml.