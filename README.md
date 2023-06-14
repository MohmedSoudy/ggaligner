# ggaligner: Visualizing Sequence Alignment by Generating Publication-Ready Plots

[![CRAN RStudio mirror downloads](https://cranlogs.r-pkg.org/badges/grand-total/ggaligner?color=blue)](https://CRAN.R-project.org/package=ggaligner) 
[![CRAN RStudio mirror downloads](https://cranlogs.r-pkg.org/badges/ggaligner)](https://CRAN.R-project.org/package=ggaligner) 
[![](https://www.r-pkg.org/badges/version/ggaligner?color=green)](https://CRAN.R-project.org/package=ggaligner) 

![](https://i.ibb.co/B44Z9dt/test-sample-P-v1.jpg)

```R
if (!require("BiocManager", quietly = TRUE))
    install.packages("BiocManager")

BiocManager::install("ggmsa")
install.packages("ggaligner")
```

# Description

Providing publication-ready graphs for Multiple sequence alignment. Moreover, it provides a unique solution for visualizing the multiple sequence alignment without the need to do the alignment in each run which is a big limitation in other available packages.

The package is mainly designed for researchers to facilitate generating publication-ready graphs for multiple sequence alignment of regions of interests in DNA or Protein sequences

# Documentation

For the documentation see: [ggaligner Documentation](https://cran.r-project.org/web/packages/ggaligner/index.html).

# Package information

- link to package on CRAN: [ggaligner](https://cran.r-project.org/package=ggaligner)

# Usage

**Example**

```R
library(Biostrings)
library(ggaligner)
library(msa)
#Read FASTA file
fasta_sample <- readAAStringSet("sample_data/test_sample.fasta")
#Perform Multiple sequence alignment 
aln_sample <- msa(fasta_sample)
#Visualize the alignment using ggaligner with default parameter
ggaligner(aln_sample)
#Change the visualization style
P <- ggaligner(aln_sample, start = 100, end = 125, color = "Shapely_AA", font = "TimesNewRoman")
#Save the alignment image to be used for publication 
ggsave(filename = "test_sample.jpeg",plot = P, width = 12, height = 7, dpi = 600)
```

# Contribution Guidelines

For bugs and suggestions, the most effective way is by raising an issue on the GitHub issue tracker. GitHub allows you to classify your issues so that we know if it is a bug report, feature request, or feedback to the authors.

**Email: MohmedSoudy2009@gmail.com**