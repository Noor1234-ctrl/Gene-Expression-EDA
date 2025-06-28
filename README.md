# Gene-Expression-EDA
Gene Expression Data Analysis — Breast Cancer Progression
This project focuses on the cleaning, preprocessing, and exploratory analysis of a breast cancer gene expression dataset. The goal is to prepare a clean, manageable subset for analysis and visualization to better understand gene expression patterns across different breast tissue conditions.

The dataset originally contains microarray gene expression profiles from 12 patients across various stages of breast cancer progression, including normal tissue, atypical ductal hyperplasia (ADH), ductal carcinoma in situ (DCIS), and invasive ductal carcinoma (IDC).

For this analysis, the dataset was filtered to focus on 5 patients and a subset of ~200 genes, making it computationally efficient for demonstration, learning, and analysis purposes.

Data Cleaning Process:
The original dataset contained approximately 22,283 genes (rows) and 32 samples (columns).

The cleaning steps were:

Sample Selection:
Selected data corresponding to 5 patients representing multiple conditions:

Normal (HN)

Atypical Ductal Hyperplasia (ADH)

Ductal Carcinoma In Situ (DCIS)

Stromal (SH)

Gene Annotation Merge:
Merged the gene expression data with an annotation file to include gene symbols and gene titles for easier biological interpretation.

Null Value Handling:
Removed rows where gene symbols were missing (NaN) to ensure all genes are properly annotated.

Duplicate Handling:
For genes with duplicate gene symbols, the mean of their expression values was taken.

Subset Creation:
A filtered dataset of 200 genes was created. After removing nulls and duplicates, the final subset contained 195 genes across 17 samples (for the selected 5 patients).

Cleaned Dataset Information:
File: cleaned_gene_expression_subset.csv

Content:
Contains expression levels of 195 genes across 17 samples, with metadata columns for gene symbol and condition labels (e.g., Normal, ADH, DCIS, SH).

Exploratory Data Analysis (EDA):
Analysis Performed:
Distribution Analysis:
Plotted histograms to inspect the overall distribution of gene expression values. Most genes exhibited low expression, with a few highly expressed genes — indicating a right-skewed distribution typical in gene expression data.

Boxplots:
Visualized the spread, median, and variability of expression levels for each sample. This helped detect variability and potential outlier patterns across conditions.

Correlation Heatmap:
Displayed sample-to-sample correlation to check consistency and similarity between biological conditions. Observed which samples are more or less correlated (e.g., some DCIS samples were less correlated with others).

Principal Component Analysis (PCA):
Applied PCA for dimensionality reduction. This allowed us to observe clustering patterns of samples based on conditions, showing separation between different tissue types (e.g., Normal vs. DCIS).

Key Insights:
Biological Variation:
Samples cluster based on biological conditions, confirming meaningful variation between Normal, ADH, DCIS, and Stromal tissues.

High Variability Genes:
PCA and boxplots highlighted that certain conditions exhibited greater variability, which may represent key biological changes during cancer progression.

Data Readiness:
This subset is now suitable for further analysis such as differential expression analysis, clustering, or supervised machine learning tasks.



