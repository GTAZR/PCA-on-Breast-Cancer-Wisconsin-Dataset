# PCA-on-Breast-Cancer-Wisconsin-Dataset
1. Background

Breast cancer is one of the most common cancers worldwide.
The Breast Cancer Wisconsin (Diagnostic) Dataset provides 569 samples, each with 30 numerical features extracted from microscopic images of tumor cells. These features describe the size, shape, and texture of the cells.

Features are grouped into three categories:

Mean values (e.g., radius_mean, texture_mean)

Standard error values (SE) (e.g., radius_se, texture_se)

Worst or maximum values (e.g., radius_worst, area_worst)

Each sample is also labeled as Benign (B) or Malignant (M), which we can use to visualize whether PCA successfully separates the two groups.

2. Research Question

Can PCA reduce the 30 tumor features to just 2–3 main components while still separating benign and malignant tumors clearly?

Which original features contribute most to these components, and do they represent medically meaningful factors such as tumor size or shape complexity?

3. Methodology

Data Preprocessing

Remove non-informative columns (id, empty column).

Standardize all 30 features (center and scale).

PCA Analysis

Perform PCA and select the first 2–3 principal components.

Create score plots, coloring by diagnosis label (B/M).

Loadings Analysis

Identify which features have the largest loadings in PC1 and PC2.

Interpret them as “tumor size factor” or “shape complexity factor.”

Residual/Explained Variance Analysis

Calculate R² to check how much variance is captured.

Look at residuals to identify outliers or unusual cases.

4. Expected Results

The first 2–3 principal components will capture about 80% of the variance.

PC1 is likely linked to tumor size (radius, area, perimeter).

PC2 may represent tumor irregularity or texture (smoothness, fractal dimension).

The score plot should show a clear separation between benign and malignant tumors when colored by diagnosis.

Some misclassified or outlier samples may appear, which are interesting to analyze further.

5. Significance

This project will demonstrate how PCA can:

Simplify a high-dimensional medical dataset.

Reveal latent variables such as size and complexity that are most important for diagnosis.

Provide insights into how statistical methods can support medical decision-making.
