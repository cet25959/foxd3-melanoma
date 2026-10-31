# foxd3-melanoma
This repository will contain the code used for the analysis of the FOXD3 gene signature in various aspects of melanoma biology

## Repository Structure

### `01_bulkRNAseq_processing.Rmd`
Processes bulk RNA-seq count data and generates the DESeq2 objects used in downstream analyses.

### `02_scRNAseq_processing.Rmd`
Processes publicly available single-cell RNA-seq datasets and generates the Seurat objects used in downstream analyses.

### `03_gene_signature_generation.Rmd`
Generates the gene signature used for downstream analyses.

### `04_gene_signature_validation.Rmd`
Validates the gene signature across internal and external datasets.

### `05_early_resistant_testing.Rmd`
Tests the gene signature at early and resistant timepoints when treated with targeted therapeutics or immunotherapies

### `06_immune_testing.Rmd`
Performs correlation analysis of gene signature against Tirosh immune signatures

### `07_tumor_growth_analyzing.Rmd`
Analyzes tumor growth rates for wet lab experiment

## Data Availability

Bulk RNA-seq and single-cell RNA-seq datasets used in these analyses are available through the Gene Expression Omnibus (GEO). Dataset-specific accession numbers and required input files are provided within the corresponding R Markdown files.

Additional metadata required for the analyses is provided in the `metadata/` directory.

## Gene Signatures

Gene signatures used in downstream analyses are provided in the `gmt/` directory.

The fixed HUGO gene signature corresponds to the gene-symbol version used for the analyses reported in the manuscript. Additional information regarding gene identifier conversion is provided in `03_gene_signature_generation.Rmd`.

## Running the Analyses

The R Markdown files are numbered according to the general analysis workflow.

Files `01` and `02` generate the DESeq2 and Seurat objects used as inputs for downstream analyses.

Files `03`–`07` perform the analyses used to generate the reported manuscript results.

Dataset-specific inputs and dependencies are described at the beginning of each R Markdown file.

## Computational Requirements

Some single-cell RNA-seq processing steps are memory intensive. Running these analyses in a fresh R session is recommended on systems with limited available memory.
