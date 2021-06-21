# testing binder dependencies

- binder that updated the salmon/tbb issue: [![Binder](https://binder.pangeo.io/badge_logo.svg)](https://binder.pangeo.io/v2/gh/marisalim/2020-ggg-201b-rnaseq/marisa-binder?urlpath=rstudio)
- binder that is trying to fix bioconductor R install without messing up salmon/tbb fix: [![Binder](https://binder.pangeo.io/badge_logo.svg)](https://binder.pangeo.io/v2/gh/marisalim/2020-ggg-201b-rnaseq/marisa-test-rdeps?urlpath=rstudio)

Original repo/binder:

## 2020-ggg-201b-rnaseq

Last updated Jan 6, 2021.

[GGG201b, Intro to Bioinformatics](https://github.com/ngs-docs/2020-GGG201b-lab)

UC Davis

[![Binder](https://binder.pangeo.io/badge_logo.svg)](https://binder.pangeo.io/v2/gh/ngs-docs/2020-ggg-201b-rnaseq/stable?urlpath=rstudio)

Authors: Taylor Reiter and N. Tessa Pierce

Technical updates by Titus Brown.

### To run in binder --

1) start the binder

2) at the command line, run

```
snakemake -j 4 --use-conda
```

3) open `rnaseq-workflow.Rmd`

4) knit to HTML
