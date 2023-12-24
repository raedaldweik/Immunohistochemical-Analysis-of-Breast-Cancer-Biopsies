# Immunohistochemical-Analysis-of-Breast-Cancer-Biopsies

## Project Overview
This project is focused on evaluating the impact of chemotherapy on breast cancer patients, specifically from the ADAPT clinical trial dataset. The goal is to use advanced data analysis techniques to predict whether a patient, before undergoing treatment, will be a responder to the therapy. Responders are characterized by a reduced density of cancer cells and increased density of immune markers (CD4 or CD8).

## Data Preprocessing
Data Cleaning: Removed B3 rows from the dataset as these were inconsistent across patients.
Normalization: Divided all marker counts by the corresponding sample area (in pixels) to calculate the density of cells.
Data Structuring: Created a 3D matrix representing the processed data and provided the data in .mat format for MATLAB users.
Data Splitting: Utilized k-fold cross-validation to split data into training (90%) and test (10%) sets.

# Unsupervised Data Analysis
PCA Analysis: Performed Principal Component Analysis (PCA) to identify two distinct clusters for pre-treatment (B1) and post-treatment (B2) patients.
K-means Clustering: Conducted K-means clustering analysis for B1 and B2 patients and compared the results with PCA findings.
Marker Analysis: Generated boxplots for each marker within each cluster and identified key markers characterizing the clusters.
Responder Identification: Examined if B2 clusters can be classified as responders or non-responders based on their marker profiles.

# Statistical Testing
Multivariate Analysis: Conducted multivariate statistical tests to assess differences between clusters.
Cluster Transition Analysis: Analyzed transitions between B1 and B2 clusters to understand patterns of response to therapy.

# Data Classification
Implemented Linear Discriminant Analysis (LDA) with k-fold cross-validation to classify new patients as likely responders based on their initial marker profiles.

# Alternative Approach
Marker Difference Calculation: Calculated the difference in marker densities between pre-treatment (B1) and post-treatment (B2) states.
Statistical Significance Testing: Performed hypothesis testing to identify statistically significant changes in markers.
Marker Selection: Selected markers with significant differences to refine the classification of responders and non-responders.
