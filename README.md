# Multi-omics integration of transcriptomics and metabolomics with machine learning uncovers novel risk factors for Alzheimer's disease

**Transcriptomics · Metabolomics · Cooperative learning · Alzheimer’s disease research**

This repository provides a public overview of our study, **“Multi-omics integration of transcriptomics and metabolomics with machine learning uncovers novel risk factors for Alzheimer's disease,”** published in the *Journal of Alzheimer's Disease* (2026).

**Publication:** [Read the paper](https://journals.sagepub.com/doi/10.1177/13872877261487621)  
**Authors:** Jerome J. Choi, Corinne D. Engelman, Tianyuan Lu

## Research overview

Alzheimer’s disease involves interconnected molecular and clinical processes. Our study examined whether information from two omics layers—**genetically imputed whole-blood gene expression** and **measured plasma metabolites**—could be integrated to predict cognitive performance and identify relevant molecular features.

The target was the **Preclinical Alzheimer's Cognitive Composite 3 (PACC3)**, a measure of cognitive performance. The goal was not to diagnose Alzheimer's disease, but to investigate molecular correlates of cognition using multi-omics prediction and feature interpretation.

## Study design

![Figure 1: Study design for multi-omics integration and cognitive-score prediction](https://cdn.ncbi.nlm.nih.gov/pmc/blobs/ee96/13653362/3cc3e4a6bb3c/nihms-2213225-f0001.webp)

*Figure 1. Study design: gene expression imputation, biomarker screening, multi-view prediction, feature importance, and independent validation. Source: [published manuscript](https://pmc.ncbi.nlm.nih.gov/articles/PMC13653362/).*

1. **Data preparation:** Impute gene expression from genotype information and assemble measured plasma metabolomics.
2. **Feature screening:** Evaluate transcriptomic and metabolomic associations with PACC3, adjusting for age, sex, APOE score, and education.
3. **Multi-view modeling:** Use **cooperative learning** to integrate the two omics views and predict PACC3.
4. **Interpretation:** Examine model coefficients and enriched biological processes to identify candidate molecular contributors.
5. **Validation:** Evaluate predictions on a held-out subset of the Wisconsin Registry for Alzheimer’s Prevention (WRAP) and an independent Wisconsin Alzheimer’s Disease Research Center (ADRC) cohort.

## Data and evaluation

| Cohort | Role | Participants |
| --- | --- | ---: |
| Wisconsin Registry for Alzheimer's Prevention (WRAP) | Model development and holdout evaluation | 1,046 |
| Wisconsin Alzheimer’s Disease Research Center (ADRC) | Independent external validation | 85 |

**Reported performance**

| Evaluation | Normalized RMSE | R² |
| --- | ---: | ---: |
| WRAP holdout | 0.707 | 0.338 |
| ADRC external validation | 0.915 | 0.061 |

*Normalized RMSE was calculated relative to the interquartile range of observed cognitive scores. External validation performance was substantially lower than holdout performance and should be interpreted cautiously given the small independent cohort.*

## Selected results

- The multi-omics model explained **33.8% of variance** in cognitive performance in the WRAP holdout cohort (R² = 0.338), versus **22.7%** for the covariate-only baseline (R² = 0.227).
- In the independent Wisconsin ADRC cohort, the model achieved **NRMSE = 0.915** and **R² = 0.061**. Results should be interpreted cautiously given the relatively small external cohort (n = 85).
- Screening identified **354 candidate genes** out of 6,678 imputed expression features and **150 metabolites** out of 1,125 measurements for downstream modeling.

## Biological findings

The analysis identified candidate genes and metabolites associated with cognitive performance. Important transcriptomic features included *RIPK1*, *IL6ST*, *BIN1*, *UGP2*, *NDUFB5*, and *TMOD2*. Metabolomic contributors included **benzoate, 3-phenylpropionate, imidazolelactate, and hexanoylcarnitine**, among others.

The findings pointed to molecular processes involving inflammatory signaling, mitochondrial function, and lipid metabolism. These are **candidate associations and predictive features**, not evidence that individual biomarkers causally determine cognitive outcomes.

## Code and data availability

**The underlying research data and analysis code are not distributed in this public repository.** The study used research-cohort data subject to access and governance requirements. This repository is intended as a **research summary and figure showcase**, not an executable or reproducible software distribution.

For study methods, evaluation details, and interpretation, please consult the [published article](https://journals.sagepub.com/doi/10.1177/13872877261487621).

## Related links

- [Published article — *Journal of Alzheimer's Disease* (2026)](https://journals.sagepub.com/doi/10.1177/13872877261487621)
- [Personal research website](https://jeromejchoi.com)
- [Publications](https://jeromejchoi.com/#publications)
