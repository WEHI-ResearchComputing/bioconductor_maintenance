# Bioconductor

Bioconductor is a software ecosystem of software tools, packages and resources tailored specifically for the analysis and interpretation of high-throughput biological data. It is a pivotal and highly influential tool used by researchers in the field of Bioinformatics and computational Biology.

Many researchers at WEHI contribute to Bioconductor. We would like to find out if we can streamline some of the processes around Bioconductor to reduce the maintenance burden, or perhaps share best practices that we found were useful. Things such as removing dependencies, Continuous integration etc.

## Schex 

[Schex](https://github.com/SaskiaFreytag/schex) is an R-package inside Bioconductor, created by Saskia Freytag with the goal of providing hexagonal cell representations of single cell data stored in [SingleCellExperiment](https://bioconductor.org/packages/release/bioc/html/SingleCellExperiment.html). More information is contained in the [Schex repository](https://github.com/SaskiaFreytag/schex)

### Installation
#### Installing R:
Download R: https://cran.r-project.org/bin/windows/base/rdevel.html<br>
Download RStudio IDE: https://posit.co/download/rstudio-desktop/

Follow all instructions in this video for proper installation: https://www.youtube.com/watch?v=YrEe2TLr3MI

### Package Installation:
In the R console, install the necessary packages:

**Install development version of Bioconductor**
```
if (!requireNamespace("BiocManager", quietly=TRUE))
    install.packages("BiocManager")
BiocManager::install(version="devel")
BiocManager::valid()
```

**Install the Development Version of Schex**
```
install.packages("devtools")
devtools::install_github("SaskiaFreytag/schex@devel")
```

**Additional packages to install**
* SingleCellExperiment:
```
install.packages('SingleCellExperiment')
```
* TENXPBMCData (The dataset):
```
if (!require("BiocManager", quietly = TRUE)) 
    install.packages("BiocManager") 
BiocManager::install("TENxPBMCData") 
```
* Scater:
```
if (!require("BiocManager", quietly = TRUE)) 
    install.packages("BiocManager") 
BiocManager::install("scater") 
```
* Scran: 
```
if (!require("BiocManager", quietly = TRUE)) 
    install.packages("BiocManager") 
BiocManager::install("scran") 
```
* Seurat (only used to show conversion from Seurat to SingleCellExperiment):
```
install.packages('Seurat')
```
