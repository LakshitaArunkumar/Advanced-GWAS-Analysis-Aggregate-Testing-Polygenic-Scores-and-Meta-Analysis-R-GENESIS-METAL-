## Advanced GWAS Analysis: Aggregate Testing, Polygenic Scores, and Meta-Analysis (R, GENESIS, METAL)

This project extends a genome-wide association study (GWAS) of height by implementing advanced analytical approaches, including variant-level evaluation, gene-based aggregate testing, polygenic risk scoring, and cross-study meta-analysis.

---

## Project Overview

Genome-wide association studies identify variants associated with complex traits, but deeper biological insight requires additional analyses. This project builds upon GWAS results to evaluate signal validity, test gene-level associations, assess predictive genetic scores, and integrate results across studies.

---

## Objectives

- Evaluate top GWAS signals and their biological relevance  
- Perform gene-based aggregate association tests  
- Assess predictive performance of polygenic scores (PGS)  
- Harmonize GWAS datasets across studies  
- Conduct meta-analysis to improve statistical power  

---

## Workflow Summary

### GWAS Signal Evaluation

- Identified most significant variant from GWAS results  
- Extracted genotype data and merged with phenotype information  
- Visualized genotype–phenotype relationships  
- Assessed strength and validity of association signals  

---

### Variant Annotation

- Mapped top variants to known identifiers  
- Evaluated predicted functional consequences  
- Interpreted biological relevance of associated loci  

---

### Aggregate Testing (Gene-Level Analysis)

- Focused on variants within and around a candidate gene region  
- Performed:
  - Burden test  
  - SKAT (Sequence Kernel Association Test)  
  - SKAT-O  

- Compared results across methods to assess gene-level association  

---

### Polygenic Score (PGS) Analysis

- Applied external polygenic score model for height  
- Integrated PGS with phenotype data  
- Evaluated predictive performance using:
  - Linear regression  
  - Effect size estimates  
  - Variance explained (R²)  

---

### GWAS Harmonization

- Performed quality control using EasyQC  
- Standardized variant information across studies  
- Identified and removed problematic variants:
  - Allele mismatches  
  - Frequency discrepancies  
  - Duplicates  

---

### Meta-Analysis

- Combined GWAS results from multiple studies using METAL  
- Applied inverse-variance weighted fixed-effects model  
- Evaluated consistency of effect directions across studies  
- Identified shared and study-specific variants  

---

### Result Interpretation

- Generated:
  - Manhattan plots  
  - Q-Q plots  
  - Forest plots  

- Assessed:
  - Signal consistency  
  - Effect size agreement  
  - Evidence of heterogeneity  

---

## Technologies Used

- R  
- GENESIS  
- SeqArray / SeqVarTools  
- EasyQC  
- METAL  
- tidyverse  
- qqman  
- ggplot2  

---

## Key Features

- Multi-level genetic analysis pipeline  
- Integration of single-variant and gene-based methods  
- Polygenic risk score evaluation  
- Cross-study harmonization and meta-analysis  
- Visualization and interpretation of association results  

---

## Key Skills Demonstrated

- Advanced GWAS analysis  
- Rare variant and aggregate testing (Burden, SKAT, SKAT-O)  
- Polygenic score modeling  
- Data harmonization across studies  
- Meta-analysis of genetic association results  
- Interpretation of heterogeneous genetic effects  

---

## Notes

- Aggregate tests assess cumulative effects of variants within a genomic region  
- Polygenic scores capture small effects across many variants  
- Meta-analysis increases statistical power by combining studies  
- Differences across studies may indicate heterogeneity in genetic effects  

---

## Author

Lakshita Arunkumar
