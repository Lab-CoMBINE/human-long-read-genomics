# Human Long-Read Genomics Explorer

**Interactive companion to “The long-read era of human genomics”** by Marta Baragli and Alberto Magi (Department of Information Engineering, University of Florence; COMBINE Lab).

A static, read-only resource for exploring the benchmark results and computational tools discussed in the review. **This repository does not claim that all underlying benchmark pipelines are reproducible from this release.** The source analysis scripts will be added after verification.

## Open the Explorer

After enabling GitHub Pages (**Settings → Pages → Deploy from a branch → main → /docs**), the site will be served at `https://<organization>.github.io/<repository>/`. Replace placeholders with the actual organization and repository name. The interface is in [`docs/index.html`](docs/index.html).

To test locally from the repository root:

```bash
python -m http.server 8765 --directory docs --bind 127.0.0.1
```

Open `http://127.0.0.1:8765`. Port 8765 is an example; choose another free port if occupied.

## Content

- **Explore:** browse by analytical task or sequencing technology.
- **Tools:** curated computational software directory; “Benchmarked” identifies tools evaluated in this study, not an independent recommendation.
- **Benchmarks:** sequencing accuracy, SNV/InDel/SV detection, phasing, DNA methylation.
- **Compare:** descriptive within-pair visualization; normalized values must not be interpreted as absolute performance rankings.
- **Underlying data:** tab-separated tables in [`docs/data/benchmarks/`](docs/data/benchmarks/). `table_manifest.tsv` reports row counts and file sizes.

## Repository layout

```text
docs/                 GitHub Pages site and frozen benchmark tables
scripts/              Placeholder for verified reproduction scripts
config/               Placeholder for portable pipeline configurations
environment/          Placeholder for pinned software environments
CITATION.cff          Citation metadata for this software resource
README.md             Project documentation
```

## Provenance and interpretation

The quantitative tables are carried forward from the working v0.8 Explorer, **without reanalysis**. The benchmarks are conditional on the datasets, tools, versions and evaluation procedures described in the associated manuscript. The website is not a continuously updated benchmark service. Methylation calling and concordance comparisons can depend on platform-specific thresholds.

Some tool-to-publication associations were assembled during manuscript processing and **have not all been independently checked against primary publications**. Do not use the tool bibliography as a verified citation registry until this review is complete.

The companion manuscript is currently identified by its working title; its journal, DOI and final bibliographic citation should be inserted once confirmed.

## Reproducibility roadmap

A subsequent release will document original input datasets, reference genomes, software versions, commands, evaluation tools, and Python/R scripts for each benchmark. In the present release, the published TSV tables allow inspection and replotting of the summarized results, not a complete end-to-end re-run.

## Attribution and licensing

Authors: **Marta Baragli and Alberto Magi**, University of Florence. **A public reuse license has not yet been selected or approved.** Before publishing, confirm the appropriate software and data licenses with the rights holders and add the corresponding LICENSE files. Do not assume the repository is MIT- or CC BY-licensed until that decision is made.

## Release

**v1.0.0**: first GitHub Pages-ready packaging of the tested v0.8 interface and frozen benchmark data.
