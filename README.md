![](https://travis-ci.org/zmjones/edarf.svg) ![](http://www.r-pkg.org/badges/version/edarf)
[![DOI](https://zenodo.org/badge/23669422.svg)](https://zenodo.org/badge/latestdoi/23669422)
[![status](http://joss.theoj.org/papers/d29df349c8450ef958c0fde5bf164371/status.svg)](http://joss.theoj.org/papers/d29df349c8450ef958c0fde5bf164371)

Functions useful for exploratory data analysis using random forests.

This package extends the functionality of random forests fit by [party](http://cran.r-project.org/web/packages/party/index.html) (multivariate, regression, and classification), [randomForestSRC](http://cran.r-project.org/web/packages/randomForestSRC/index.html) (regression, classification, and survival), and [randomForest](http://cran.r-project.org/web/packages/randomForest/index.html) (regression and classification).

The subdirectory `pkg` contains the actual package. The package can be installed with [devtools](https://cran.r-project.org/web/packages/devtools/index.html).

Documentation of functions as well as a vignette can be found [here](http://zmjones.github.io/edarf/).

```{r}
devtools::install_github("zmjones/edarf", subdir = "pkg")
```

Functionality includes:

 - `partial_dependence` which computes the expected prediction made by the random forest if it were marginalized to only depend on a subset of the features. `plot_pd` plots the results.
 - `variable_importance` which computes feature importance for arbitrary loss functions, aggregated across the training data or for individual observations. This may also be used for subsets of the feature space in order to detect interactions.
 - `extract_proximity` and `plot_prox` which computes or extracts proximity matrices and plots them using a biplot given a matrix of principal components of said matrix.

Pull requests, bug reports, feature requests, etc. are welcome!
