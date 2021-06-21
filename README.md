testing a new binder for r dependencies - getting error like [this](https://discourse.jupyter.org/t/glibcxx-3-4-26-not-found-from-rstudio/7778) when trying to load `library(DESeq2)` after adding:

```
r-base
r-irkernel=1.1
r-devtools
```

not sure if one of these is causing the error.

```
> library(DESeq2)
Error: package or namespace load failed for ‘DESeq2’ in dyn.load(file, DLLpath = DLLpath, ...):
 unable to load shared object '/srv/conda/envs/notebook/lib/R/library/Rcpp/libs/Rcpp.so':
  /usr/lib/x86_64-linux-gnu/libstdc++.so.6: version `GLIBCXX_3.4.26' not found (required by /srv/conda/envs/notebook/lib/R/library/Rcpp/libs/Rcpp.so)
```

[![Binder](https://binder.pangeo.io/badge_logo.svg)](https://binder.pangeo.io/v2/gh/marisalim/2020-ggg-201b-rnaseq/marisa-test-rdeps?urlpath=rstudio)
