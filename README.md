# Manuscript: ghedata

Collaborative manuscript using Quarto.

## Getting Started

1. Clone the repository and navigate to this directory

2. Restore R package dependencies:

```r
renv::restore()
```

3. Render the manuscript:

```bash
quarto render manuscript.qmd
```

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md) for our workflow using issues and pull requests.

## Dependencies

This project uses `renv` for R package management. The lockfile (`renv.lock`) tracks all package versions to ensure reproducibility.
