
# Advanced GWAS Analysis: Aggregate Testing, Polygenic Scores, and Meta-Analysis

**Graduate Coursework Project | M.S. Genome Bioinformatics | University of Pittsburgh**

## Project Overview

This project was completed as part of my graduate coursework at the University of Pittsburgh. It builds upon a genome-wide association study (GWAS) of human height by exploring additional statistical approaches for evaluating genetic associations.

The analysis included assessment of individual GWAS signals, gene-region aggregate testing, polygenic score (PGS) evaluation, quality control and harmonization of GWAS summary statistics, and cross-study meta-analysis.

The project used R, GENESIS, PLINK, EasyQC, and METAL to investigate genetic contributions to height and interpret association results across datasets.

## Objectives

- Evaluate significant and suggestive GWAS signals.
- Annotate genetic variants and examine genotype–phenotype relationships.
- Perform regional aggregate association testing using Burden, SKAT, and SKAT-O.
- Evaluate the association between polygenic scores and height.
- Harmonize GWAS summary statistics across studies.
- Conduct fixed-effects meta-analysis to combine association results.
- Visualize and interpret genetic association findings.

## Tools and Technologies

| Tool | Purpose |
|------|---------|
| R / tidyverse | Data processing and statistical analysis |
| GENESIS | Single-variant and aggregate association testing |
| SeqArray / SeqVarTools | Genomic data management |
| PLINK | Polygenic score calculation |
| EasyQC | GWAS summary statistics quality control |
| METAL | Cross-study GWAS meta-analysis |
| qqman / ggplot2 | Association visualization |
| Ensembl VEP | Variant consequence annotation |

## Analysis Workflow

```text
GWAS of Human Height
          |
          v
Evaluate Top Association Signals
          |
          v
Variant Annotation (Ensembl VEP)
          |
          v
Aggregate Testing (GENESIS)
   Burden | SKAT | SKAT-O
          |
          v
Polygenic Score Evaluation (PLINK)
          |
          v
GWAS Harmonization (EasyQC)
          |
          v
Meta-Analysis (METAL)
          |
          v
Result Interpretation and Visualization
```

## Methods and Results

### 1. GWAS Signal Evaluation

- Identified the variant with the strongest association with height in the provided GWAS results.
- Extracted genotype dosage data and integrated it with phenotype information.
- Visualized height distributions across genotype groups using a sina plot.
- Annotated the variant using Ensembl Variant Effect Predictor (VEP).

**Top variant identified:**

| Attribute | Result |
|-----------|--------|
| Variant | rs45477898 |
| Chromosome | 19 |
| Position (hg38) | 28,492,903 |
| Effect allele | C |
| GWAS p-value | 4.21 × 10⁻⁶ |
| Effect estimate | -0.883 |
| Genotype status | Imputed |

The association did not reach the conventional genome-wide significance threshold of 5 × 10⁻⁸.

### 2. Aggregate Association Testing

Performed regional aggregate association tests for **HMGA1**, including variants within the gene region and 50 kb upstream and downstream.

Three statistical methods were evaluated:

| Test | Variants Tested | P-value |
|------|-----------------|---------|
| Burden | 4 | 0.4285 |
| SKAT | 4 | 0.8430 |
| SKAT-O | 4 | 0.5965 |

None of the three tests showed statistically significant evidence of association between the tested variants near HMGA1 and height.

### 3. Polygenic Score Analysis

- Evaluated a previously developed polygenic score for height (PGS002975).
- Used PLINK to calculate polygenic scores from the provided genotype data.
- Integrated polygenic scores with individual-level height measurements.
- Applied linear regression to evaluate the association between PGS and height.

**Reported results:**

| Metric | Result |
|--------|--------|
| PGS association p-value | 9.12 × 10⁻⁷ |
| Variance explained (R²) | Approximately 0.0094 |
| Regression coefficient | 4.90 |

The polygenic score showed a statistically significant association with height but explained approximately **0.94% of the observed variation** in this dataset.

### 4. GWAS Quality Control and Harmonization

Used EasyQC to process GWAS summary statistics from two studies:

- **Study 1:** GWAS of height (N = 2,548)
- **Study 2:** UK Biobank height GWAS (N = 360,388)

Quality-control procedures examined:

- Variant identifiers and genomic positions
- Allele consistency
- Allele frequency discrepancies
- Duplicate variants
- Missing or invalid association statistics

**Variants retained after EasyQC:**

| Study | Variants |
|-------|----------|
| Study 1 | 104,670 |
| Study 2 | 482,068 |

The harmonized results were prepared for meta-analysis.

### 5. GWAS Meta-Analysis

- Combined the two GWAS datasets using METAL.
- Applied inverse-variance weighted fixed-effects meta-analysis.
- Compared variant effect directions across studies.
- Identified shared and study-specific variants.
- Generated Manhattan and Q-Q plots.
- Created a forest plot to compare effect estimates and confidence intervals for a selected shared variant.

The analysis examined how combining association statistics from different studies can improve precision and provide additional evidence about genetic associations.

Differences in effect estimates across studies were also considered when interpreting the results.

## Visualizations

| Visualization | Purpose |
|---------------|---------|
| Sina plot | Height distribution across genotype groups |
| PGS scatter plot | Relationship between polygenic score and height |
| Manhattan plot | Genome-wide association signals |
| Q-Q plot | Distribution of observed versus expected p-values |
| Forest plot | Comparison of effect estimates across studies |

## Repository Contents

**Main analysis file:** [Advanced_GWAS_Analysis.Rmd](Advanced_GWAS_Analysis.Rmd)

The R Markdown file contains the analytical code, statistical tests, visualizations, and interpretation of results.

The project used coursework-provided datasets, starter code, and configuration files. External input paths must be updated to reproduce the analysis in another environment.

## Limitations

- The analysis was performed as part of a guided graduate coursework assignment.
- Aggregate testing was limited to four variants in the selected HMGA1 region.
- Although the PGS was statistically associated with height, its explanatory power was low.
- Differences in sample sizes and population characteristics may affect cross-study comparisons.
- The meta-analysis used a fixed-effects model, which assumes a common underlying genetic effect across studies.
- Interpretation of potential heterogeneity requires additional statistical evaluation.

## Skills Demonstrated

- GWAS signal evaluation and variant annotation
- Genetic association testing using GENESIS
- Burden, SKAT, and SKAT-O aggregate testing
- Polygenic score calculation and regression analysis
- GWAS summary statistics harmonization
- Fixed-effects meta-analysis using METAL
- Statistical visualization and interpretation using R

## Coursework Acknowledgment

This project was completed as part of the M.S. Genome Bioinformatics curriculum at the University of Pittsburgh.

The coursework provided starter code and datasets. The assignment was completed in collaboration with Gagan Heda and Sanika Kamath, with individual responsibility for the submitted analysis and report.

## Author

**Lakshita Arunkumar**

M.S. Genome Bioinformatics  
University of Pittsburgh

[GitHub Profile](https://github.com/LakshitaArunkumar)
