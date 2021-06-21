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

maybe need different version of R? binder has v4.0.5 no. specifying r version has installation failure for tximeta
```
> install.packages('DESeq2')
Warning in install.packages :
  package ‘DESeq2’ is not available for this version of R

A version of this package for your version of R might be available elsewhere,
see the ideas at
https://cran.r-project.org/doc/manuals/r-patched/R-admin.html#Installing-packages
```

- trying separate r env yml...this works but is not ideal, because you have to launch R from terminal (vs. console) to use the conda env.
- trying a suggestion from https://discourse.jupyter.org/t/glibcxx-3-4-26-not-found-from-rstudio/7778/7. this adds a [start config](https://mybinder.readthedocs.io/en/latest/config_files.html?highlight=start#start-run-code-before-the-user-sessions-starts) file. it seems to fix the bioconductor R package install fails!


[![Binder](https://binder.pangeo.io/badge_logo.svg)](https://binder.pangeo.io/v2/gh/marisalim/2020-ggg-201b-rnaseq/marisa-test-rdeps?urlpath=rstudio)
