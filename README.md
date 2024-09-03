# Genomic-Features-Analysis

This repository contains three key scripts designed for genomic analysis, focusing on the investigation of DNA fragment profiles and RNA-seq data. Each script targets a specific aspect of the research, from generating fragment profiles to analysing RNA-seq expression data and comparing fragment coverage across genomic features. Below is a brief description of each script:

## 1. Create_Fragmentation_Profiles.Rmd
This script generates DNA fragmentation profiles for each sample. It uses BAM files to calculate the number of short (100-150 bp) and long (151-220 bp) DNA fragments within 5 Mbp genomic bins. The script outputs fragment profiles for individual samples and groups them by cancer status (e.g., CRC, BRCA, healthy).

### Key Features:

Reads BAM files and converts them to Genomic Ranges.
Computes the proportion of short and long fragments in each genomic bin.
Produces visualisations of fragment profiles for individual samples and groups.
Outputs fragment profile data in both raw and plotted formats.


## 2. RNAseq_analysis.Rmd
This script performs RNA-seq analysis to identify differentially expressed genes between cancer (CRC, BRCA) and healthy tissue samples. It integrates data from TCGA and GTEx to compare gene expression levels.

### Key Features:

Loads and processes RNA-seq data from multiple sources (TCGA, GTEx, and whole blood).
Identifies genes with high expression in cancer and low expression in healthy tissues and blood.
Uses edgeR and limma for differential expression analysis.
Outputs lists of highly expressed genes for downstream analysis.


## 3. Genomic_Features.Rmd
This script investigates the proportion of short and long DNA fragments overlapping key genomic features, such as exons, promoters, G4 regions, and 5' UTRs. It also explores the relationship between fragment coverage and transcriptionally active genes, focusing on genes with high and low expression in CRC, BRCA, and healthy tissues which were obtained in 02_RNAseq_analysis.Rmd.

### Key Features:

Compares short and long fragment coverage across different genomic features.
Analyses fragment distribution in highly expressed genes and random genomic regions.
Generates visualisations to compare fragment coverage in cancer vs control samples.
Outputs data and plots for further exploration of DNA fragmentation patterns.

## Usage:
Ensure all required input files (e.g., BAM files, RNA-seq count files, genomic feature files) are available and properly formatted.
Each script is designed to be run independently. Adjust file paths within the scripts to match your local directory structure.
Output data will be saved in the specified directories, including visualisations and RDS files for further analysis.
