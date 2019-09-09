
<!-- README.md is generated from README.Rmd. Please edit that file -->

# CNAqc

<!-- badges: start -->

[![Travis build
status](https://travis-ci.org/caravagn/CNAqc.svg?branch=master)](https://travis-ci.org/caravagn/CNAqc)
<!-- badges: end -->

CNAqc is a package to provide a set of metrics to assess the quality of
Copy Number Alteration (CNA) calls.

The package provides statistical measures to quantify the concordance
between mutation and Copy Number calls, exploitinng the relation between
allelic imbalance in CNA segements and allelic frequencies of somatic
mutations. Quantitative metrics and plots for data exploration and
quality check are available.

## Statistical Model

CNAqc implements a linear score where the relative size of each of a set
of karyotypes is used to weight the offset between an estimated peak in
the data, and its expectation. The expectations are determined by
standard CNA computations accouting for normal plodiy, tumour purity and
tumor ploidy. The peaks are determined after a KDE of the data, run
through a dedicated peak-detection package.

## Motivation

With this package it is easy to visually assess the concordance of
somatic mutation calls, and the CNA segements where they map.
Quantitative measures can be used to suggest adjustemnts of the current
estimates as modifications of the input purity.

## Installation

You can install the released version of CNAqc from
[GitHub](https://github.com/) with:

``` r
# install.packages("devtools")
devtools::install_github("caravagn/CNAqc")
```

-----

**Author:** [Giulio
Caravagna](https://sites.google.com/site/giuliocaravagna/), *Institute
of Cancer Research, UK*.

**Contact:** \[@gcaravagna\](<https://twitter.com/gcaravagna>)
<giulio.caravagna@icr.ac.uk>
