#Comparative Analysis of DCIS vs Healthy Samples
Project Description
This project involves the analysis of gene expression data from breast tissue samples at various stages, including Healthy (HN), Atypical Ductal Hyperplasia (ADH), Ductal Carcinoma In Situ (DCIS), and Stromal (SH) tissue. The goal is to understand how gene expression patterns change between healthy and cancerous conditions, specifically focusing on DCIS vs. Healthy (HN) comparison.

The workflow includes:

Data Cleaning and Preprocessing

Exploratory Data Analysis (EDA)

Dimensionality Reduction (PCA)

Differential Gene Expression Analysis (Volcano Plot)

Dataset Source
Citation:
Emery LA, Tripathi A, King C, Kavanah M et al. Early dysregulation of cell adhesion and extracellular matrix pathways in breast cancer progression. Am J Pathol. 2009 Sep;175(3):1292-302. PMID: 19700746

Dataset Description
Expression File: Contains gene expression levels across various patient samples.

Annotation File: Provides mapping of gene IDs to gene symbols and descriptions.

Original Dataset Stats:
~22,000 genes

32 samples (12 patients across different conditions)

Subset for This Project:
195 genes after filtering for missing data and selecting top genes of interest.

17 samples (5 patients with conditions HN, ADH, DCIS, SH).

Data Cleaning Steps
Merged Expression Data with Annotation:
Matched gene IDs between expression and annotation files.

Removed Missing Values:
Dropped genes with missing gene symbols (null or '---').

Handled Duplicate Genes:
For genes appearing multiple times, calculated the mean expression value.

Removed Zero-Variance Genes:
Removed genes that had no variation across samples (i.e., same expression everywhere).

Exploratory Data Analysis (EDA)
Distribution Analysis:
Created histograms to check gene expression distributions.

Found that the data was right-skewed, meaning most genes have low expression while a few have very high expression.

Boxplot:
Visualized expression distributions for each sample.

Identified differences in median expression levels and variability across conditions.

Correlation Heatmap:
Assessed sample-to-sample correlation.

Observed that most biological replicates within the same condition have high correlation, while DCIS samples showed more variability, suggesting biological heterogeneity.

Principal Component Analysis (PCA)
Purpose of PCA:
Reduce dimensionality to capture the most important patterns in the data.

Visualize whether samples cluster based on conditions.

Key Findings:
PC1 (54.1% variance) and PC2 (16.4% variance) capture most variability.

Some clustering observed between conditions, but with overlap.

DCIS samples showed more spread, suggesting heterogeneity in gene expression patterns.

Differential Expression Analysis (Volcano Plot)
Comparison: DCIS vs Healthy (HN)
Thresholds Used:

Log2 Fold Change ≥ 1 (upregulated in DCIS)

Log2 Fold Change ≤ -1 (downregulated in DCIS)

p-value < 0.05 (statistical significance)

Results:
No genes were significantly upregulated in DCIS.

One gene (NM_004078) was significantly downregulated in DCIS, meaning it had higher expression in Healthy samples compared to DCIS.

CSRP1, a gene involved in cytoskeletal organization and cell adhesion, was found to be differentially expressed in DCIS compared to healthy breast tissue in this analysis. This observation aligns with previous studies highlighting the early dysregulation of cell adhesion pathways in breast cancer development (Emery et al., 2009).

This result reflects analysis on a small subset (195 genes). A full dataset analysis would likely yield more biologically meaningful results.








