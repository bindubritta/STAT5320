# Unraveling Multicollinearity between Predictors with PCLR and PLSLR Techniques

## Project Description
Regression models use dimension reduction techniques for an extensive dataset with multiple correlated predictor variables. However, these methods avoid multicollinearity between predictors, which significantly influences the variance related to the analysis and may misinterpret the problem since it impairs the statistical significance of the removed independent variables.

This project intended to analyze how to deal with a dataset having high dimensionality and low variance and when the target strongly correlated with some directions in the data. It followed Principal Component Regression (PCR), an extended version of Principal Component Analysis (PCA), and Partial Least-Squares Regression (PLSR) to solve this kind of situation. As the observed response variable is binary categorical, logistic regression was used. It compared the Principal Component Logistic Regression (PCLR) model with the Partial Least-Squares Logit Regression (PLSLR) model on their performance.

## Dataset
In order to simulate the techniques, a leukemia cancer dataset was used. This tumor dataset was pre-processed and previously used for gene expression analysis [1] [2]. It was downloaded from online [3], given as "S1 Dataset". 

The characteristics of this dataset are 
- High dimensionality: The dataset has 3,571 predictor variables (genes) with only one response variable. It has 72 samples, classified into two classes (Tumor: 25 + Normal: 47). 
- Low variance: The Standard Deviation (SD) of predictor variables varies from 0.2 to 1.85, where 3,455 variables have an SD value less than 1.0. 
- Highly correlated predictor variables: As per the correlation matrix, 308 predictor variables, i.e., 8.6% of the total, have a correlation coefficient value of more than |0.8| with others.

## Remarks
Based on the cancer dataset and the same percentage of variance (i.e., 91% of the total) explained by different PCA and PLS components, the PLSLR model outperformed the PCLR model. The result was verified with multiple subsets of the cancer dataset. However, the PLSLR result demands further in-depth investigation with other datasets to confirm it was not overfitted. Finally, this project found another method named Partial Least-Squares Discriminant Analysis (PLS-DA), a variant used for the categorical response variable, interesting to analyze this cancer dataset.

## List of files
- README.md : README file
- PCLR.ipynb : Google Colab codes with results for PCLR analysis
- PLSLR.ipynb : Google Colab codes with results for PLSLR analysis
- Leukemia_Dataset.csv : Cancer Dataset
- journal.pone.0246039.s001.csv

## References
1. T. R. Golub, D. K. Slonim, P. Tamayo, C. Huard, M. Gaasenbeek, J. P. Mesirov, H. Coller, M. L. Loh, J. R. Downing, M. A. Caligiuri, C. D. Bloomfield, and E. S. Lander, “Molecular classification of cancer: class discovery and class prediction by gene expression monitoring,” Science, no. 5439, pp. 531–537, 1999.
2. S. S. Hameed, F. F. Muhammad, R. Hassan, and F. Saeed, “Gene Selection and Classification in Microarray Datasets using a Hybrid Approach of PCC-BPSO/GA with Multi Classifiers,” Journal of Computer Science, vol. 14, no. 6, pp. 868–880, 2018.
3. S. S. Hameed, R. Hassan, W. H. Hassan, F. F. Muhammadsharif, and L. A. Latiff, “HDG-select: A novel GUI based application for gene selection and classification in high dimensional datasets,” PloS one, vol. 16, no. 1, 2021, doi: 10.1371/journal.pone.0246039, https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0246039#sec016.
