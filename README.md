# **TS ACADEMY Capstone Project - Group 19 (March 2026)**

## Brain Cancer Gene Expression Analysis for Subtype Classification and Biomarker Discovery

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![scikit-learn](https://img.shields.io/badge/scikit--learn-1.0%2B-orange)
![Pandas](https://img.shields.io/badge/pandas-1.3%2B-green)
![Genomics](https://img.shields.io/badge/Genomics-Bioinformatics-ff69b4)
![Google Colab](https://img.shields.io/badge/Colab-F9AB00?style=flat&logo=googlecolab&color=525252)
![Kaggle](https://img.shields.io/badge/Kaggle-20BEFF?style=flat&logo=kaggle&logoColor=white)
![License](https://img.shields.io/badge/license-Apache%202.0-blue)
![Status](https://img.shields.io/badge/status-Completed-success)
![Last Updated](https://img.shields.io/badge/last%20updated-March%202026-brightgreen)

# Team Members (Group 19)

| S/N | Name | Role | GitHub | Email |
|------|--------------|----------------|---------------|-------------|
| 1 | **EIJE, OLOCHE CELESTINE** | Team Lead | [@Eije1](https://github.com/Eije1) | eijeoloche1@gmail.com |
| 2 | **AREMU, JACOBS OPEYEMI** | Member | [@aremu-jacobs](https://github.com/aremu-jacobs) | jacobsage4ril@gmail.com |
| 3 | **IKHALEA, EMMANUEL** | Member | [@DeveloperIkhalea](https://github.com/DeveloperIkhalea) | Dev.ikhalea@gmail.com |
| 4 | **DAVID, BRAINERD** | Member | [@Brainerd007](https://github.com/Brainerd007) | brainerddavid9@gmail.com |
| 5 | **EZEOKWELUME, MARY** | Member | [@obyokwelume-coder](https://github.com/obyokwelume-coder) | obyokwelume@gmail.com |
| 6 | **ITUNU, IFEOLUWA ADENIJI** | Member | [@Ife-ahav](https://github.com/Ife-ahav/Ife.git) | itunuadeniji31@gmail.com |
| 7 | **AJIBOLA, JOSHUA** | Member | [@JManBoss](https://github.com/JManBoss/joshman.github.io.git) | joshuaajibola00@gmail.com |
| 8 | **RAJI, RIDWANULLAH** | Member | [@DevRSR](https://github.com/DevRSR) | rajiridwanullah25@gmail.com |
| 9 | **SULE, WASIU AYINDE** | Member | [@Engrbolajipraise1](https://github.com/Engrbolajipraise1) | bolajipraise1@gmail.com |
| 10 | **MUHAMMED, OLATUNJI TIAMIYU** | Member | [@olatunjee9](https://github.com/olatunjee9) | tiamiyuolatunji1@gmail.com |

# **Project Overview**
Brain cancer remains one of the most aggressive and life-threatening malignancies worldwide. Studies shows that different subtypes (glioblastoma vs ependymoma) require vastly different treatment approaches, making accurate classification essential. Thus, this capstone project leverages machine learning and gene expression analysis to classify brain cancer subtypes and identify potential biomarkers for diagnostic and therapeutic applications.This capstone project focuses on the computational analysis of the Brain_GSE50161 dataset, containing 54,676 gene expression features across 130 samples representing four distinct brain cancer types (ependymoma, glioblastoma, medulloblastoma, pilocytic astrocytoma) and normal tissue. The primary objective is to develop machine learning models capable of accurately classifying brain cancer subtypes while identifying potential biomarkers for diagnostic and therapeutic applications.

## **Aims and Objectives:**
- Analyze gene expression patterns across 4 brain cancer subtypes and normal tissue, which drives tumor growth and subtype differentiation
- Develop supervised learning models for accurate brain cancer subtype classification
- Identify "Elite" genes (potential biomarkers) with highest diagnostic value
- Evaluate therapeutic insights for precision oncology applications
- Contribute to research output on oncology and genetics engineering
- Address challenges of high dimensionality and small sample size
  
# **Dataset Description and Importance**
The Brain_GSE50161 dataset contains gene expression profiles from 130 human brain tissue samples, comprising four distinct tumor types and normal tissue controls. This microarray data provides a comprehensive molecular portrait of brain cancer subtypes.
- **Data Name:** Brain_GSE50161.csv 
- **Size of Data:** >120MB
- **Missing Values:** None
- **Source:** Kaggle [https://www.kaggle.com/datasets/brunogrisci/brain-cancer-gene-expression-cumida]

## **Dataset Statistics**

| Attribute of the Dataset | Corresponding Values|
|--------------|-------------|
| **Total Samples** | 130 patient samples |
| **Gene Features** | 54,676 gene expression probes |
| **Classes** | 5 (4 tumor types  + normal) |
| **Data Type** | Microarray gene expression |

## **Class Distribution**

| Class of the Tumor (Types) | Count of the Tumor Types| Percentage of the Tumor Types|
|------------------|-------------------|---------------------|
| Ependymoma | 46 | 35.4% |
| Glioblastoma | 34 | 26.2% |
| Medulloblastoma | 22 | 16.9% |
| Pilocytic Astrocytoma | 15 | 11.5% |
| Normal | 13 | 10.0% |


## **Clinical Relevance**

| Brain Cancer Type | Annual Cases (Global Records) | 5-Year Survival | Challenge |
|-----------------------|---------------------------|---------------------|---------------|
| **Glioblastoma** | ~3-4 per 100,000 | <10% | Most aggressive; treatment resistance |
| **Medulloblastoma** | ~0.5 per 100,000 | 70-80% (children) | Pediatric focus; treatment toxicity |
| **Ependymoma** | ~0.2 per 100,000 | 50-80% | Location-dependent outcomes |
| **Pilocytic Astrocytoma** | ~0.8 per 100,000 | >90% | Often curable but requires surgery |

## **Comparison with Alternatives and Literature**

| Dataset | Samples | Genes | Tumor Types | Why We Chose This |
|---------|---------|-------|-------------|-------------------|
| **Brain_GSE50161** | 130 | 54,676 | 4 + normal | **Ideal balance** of size and complexity |
| TCGA-GBM | 500+ | ~20,000 | 1 | Too homogeneous |
| REMBRANDT | 671 | ~22,000 | 3 | Older platform |
| GSE4290 | 180 | ~54,000 | 3 + normal | Similar but fewer tumor types |

# **Methodology**
We imported the dataset via Google Colab, removed non-informative columns, and encoded categorical labels. We utilized StandardScaler to normalize gene expression values and audited the data for consistency. After which we carried out an Exploratory Data Analysis (EDA) where we performed class distribution analysis using df.info() and df.describe(). Data visualization was conducted using Matplotlib and Seaborn to identify trends and feature correlations. Furthermore, we did feature selection to employ a multi-stage pipeline which includes variance threshold filtering, ANOVA F-tests (SelectKBest), and feature importance ranking using Random Forest. After we finished the above steps, we developed Machine Learning Models where we developed a Logistic Regression baseline model and a high-performance Random Forest Classifier model. After which we went ahead to develop a RFE selection and a Hyperparameter Tuning. Below is the summary workflow of our methodology. In addition to this, we utilized an 80/20 Train-Test split and 5-Fold Cross-Validation to ensure model stability while investigating and measuring our model performance using Accuracy, Precision, Recall, and F1-score. Finally, Confusion Matrices were generated to visualize classification performance across subtypes. Below is the summary workflow of our project:
  
## **Data Preprocessing**
- Data cleaning and missing value check
- Feature renaming (Gene 1 to Gene 54675)
- Visualizing of our data to discover trends
- StandardScaler normalization
- Label encoding for target variable

## **Feature Selection**
- Variance threshold filtering
- ANOVA F-tests (SelectKBest)
- Random Forest feature importance
- Recursive Feature Elimination (RFE)

## **Machine Learning Models**
- Logistic Regression (Baseline)
- Random Forest Classifier**
- Random Forest with RFE + Hyperparameter Tuning

## **Evaluation Strategy**
- 80/20 Train-Test split
- 5-Fold Cross-Validation
- Metrics: Accuracy, Precision, Recall, F1-score
- Confusion Matrix analysis

## **Why Machine Learning**
Traditional bioinformatics approaches struggle with high-dimensional gene expression data, missing complex non-linear interactions between genes. Machine learning excels by identifying multivariate patterns across thousands of features simultaneously. Our Random Forest model captures subtle gene-gene interactions invisible to conventional statistics, enabling 92.31% accurate classification—a feat impossible with single-gene biomarkers or traditional methods.

| Bioinformatics Approach | Limitation of the Approach| Why Machine Learning Solves It |
|--------------------|-------------------------|---------------------------|
| Single-gene biomarkers | Low specificity | **Multivariate patterns** capture complex biology |
| Statistical tests | Miss interactions | **Tree-based models** find gene-gene interactions |
| Expert review | Subjective, variable | **Reproducible** algorithms |
| Full sequencing | Expensive | **30-gene panel** reduces cost by 99.95% |


# **Results and Conclusion**
From our results, We can now diagnose brain cancer subtypes with 92.31% accuracy using 30 genes instead of 54,676. We achieved this because our machine learning pipeline shows that Random Forest outperformed Logistic Regression, reaching a peak accuracy of 88.46% from 84.62% by capturing complex, non-linear biological relationships. However, to improve efficiency, we employed feature selection. Thus, we reduced the gene count from 54,675 to a 30-gene signature using the RFE method and Hypertuning which significantly improved model robustness and accuracy to 92.31% and also reduced overfitting. After this, we noticed that our final model maintained a solid 89.23% average Cross-Validation score which led to a team conclusion that computational analysis of microarray data is a powerful ally for precision oncology, enabling faster and more reliable tumor subtyping. In addition to this conclusion, we discovered our elite genes (biiomarkers and subsclassified these tumor types as shown below). Furthermore, we identified Gene 54638 and Gene 33848 as top discriminators. Below is the summary of our results:

## **Model Performance Evolution**

| Phase | Model | Features | Accuracy |
|-------|-------|----------|----------|
| 1 | Logistic Regression | 100 | 84.62% |
| 2 | Random Forest | 100 | 88.46% |
| 3 | RFE + Random Forest | 30 | 92.31% |
| 4 | GridSearchCV Tuned | 30 | 92.31% |


## **Elite Genes (Biomarker Discovery)**


| Rank | Probe ID | Importance Score |
|------|----------|------------------|
| 1 | 206502_s_at | 0.0765 |
| 2 | 242162_at | 0.0646 |
| 3 | 240065_at | 0.0615 |
| 4 | 230373_at | 0.0605 |
| 5 | 244239_at | 0.0597 |
| 6 | 229487_at | 0.0582 |
| 7 | 1554572_a_at | 0.0571 |
| 8 | 227404_at | 0.0558 |
| 9 | 235198_at | 0.0543 |
| 10 | 243296_at | 0.0529 |
| 11 | 1568603_at | 0.0514 |
| 12 | 229585_at | 0.0498 |
| 13 | 1556318_at | 0.0482 |
| 14 | 1563162_at | 0.0467 |
| 15 | 239439_at | 0.0451 |
| 16 | 1557691_s_at | 0.0436 |
| 17 | 1569600_at | 0.0422 |
| 18 | 1562491_at | 0.0408 |
| 19 | 1564282_at | 0.0395 |
| 20 | 1569482_at | 0.0381 |
| 21 | 1562990_at | 0.0368 |
| 22 | 1562238_at | 0.0354 |
| 23 | 1564281_at | 0.0341 |
| 24 | 1556602_at | 0.0327 |
| 25 | 1563029_at | 0.0314 |
| 26 | 1565690_at | 0.0301 |
| 27 | 1562052_at | 0.0288 |
| 28 | 1560116_at | 0.0275 |
| 29 | 1556548_at | 0.0262 |
| 30 | 1561486_at | 0.0122 |

## **Model Performance Comparison**

| Model | Accuracy | Precision | Recall | F1-Score |
|-------|----------|-----------|--------|----------|
| Logistic Regression | 84.62% | 0.85 | 0.85 | 0.84 |
| Random Forest | 88.46% | 0.88 | 0.88 | 0.88 |
| **Random Forest (Tuned + RFE)** | **92.31%** | **0.92** | **0.92** | **0.92** |


### ** Model Metrics**

                            precision    recall  f1-score   support
           ependymoma       1.00      0.89      0.94         9
         glioblastoma       0.88      1.00      0.93         7
      medulloblastoma       1.00      0.75      0.86         4
               normal       1.00      1.00      1.00         3
    pilocytic_astrocytoma   0.75      1.00      0.86         3

             accuracy                           0.92        26
            macro avg       0.93      0.93      0.92        26
         weighted avg       0.94      0.92      0.92        26

### **Confusion Matrix**

                     Predicted
                     
    Actual           Epi  Glio  Med  Nor  Pil
    
    Ependymoma        8    1    0    0    0
    Glioblastoma      0    7    0    0    0
    Medulloblastoma   1    0    3    0    0
    Normal            0    0    0    3    0
    Pilocytic Astro   0    0    0    0    3


# **Licence**

- This project is licensed under the Apache License 2.0
- Copyright (c) 2026 Group 19 - TS ACADEMY Capstone Project

Thus, you may not use this file except in compliance with the License and Copyright.
You may obtain a copy of the License at:

    http://www.apache.org/licenses/LICENSE-2.0


# Acknowledgments
- Hart Ofigwe (Data Science Tutor)
- The TS Academy Scholarship Board
- Kaggle for the Brain Cancer Gene Expression Dataset
- The Group 19 Team for their collaboration and team spirit
- Scikit-learn team for developing machine learning libraries
- GitHub for the deployment platform of our Brain Cancer Capstone Project


# References

- M S, K., S R, S. C., & R Nair, A. (2024). Performance enhancement of classifiers through Bio inspired feature selection methods for early detection of lung cancer from microarray genes. Heliyon, 10(16), e36419. https://doi.org/10.1016/j.heliyon.2024.e36419
- Brändl, B., Steiger, M., Kubelt, C., Rohrandt, C., Zhu, Z., Evers, M., Wang, G., Schuldt, B., Afflerbach, A.-K., Wong, D., Lum, A., Halldorsson, S., Djirackor, L., Leske, H., Magadeeva, S., Smičius, R., Quedenau, C., Schmidt, N. O., Schüller, U., … Müller, F.-J. (2025). Rapid brain tumor classification from sparse epigenomic data. Nature Medicine. Advance online publication. https://doi.org/10.1038/s41591-024-03435-3 [PubMed Link]
- Yadav, K., & Ranga, V. (2025). Integrated analysis of gene expressions and targeted mirnas for explaining crosstalk between oral and esophageal squamous cell carcinomas through an interpretable machine learning approach. Medical & Biological Engineering & Computing, 63(2), 483–495. https://doi.org/10.1007/s11517-024-03210-z PubMed Link
- Feng, J., Zhao, L., Fu, L., Wang, X., Ma, D., Shang, M., Xu, B., Zhou, J., Chen, Z., & Zhao, H. (2024). KDELR3 overexpression as a novel prognostic and diagnostic biomarker in glioma: comprehensive bioinformatic analysis insights. Scientific Reports, 14(1). https://doi.org/10.1038/s41598-024-75322-1 Nature Link
- Suita, Y., Bright, H., Pu, Y., Toruner, M. D., Idehen, J., Tapinos, N., & Singh, R. (2025). Machine learning on multiple epigenetic features reveals H3K27Ac as a driver of gene expression prediction across patients with glioblastoma. PLOS Computational Biology, 21(8), e1012272. https://doi.org/10.1371/journal.pcbi.1012272 PLOS Link
- Suarez-Meade, P., Clemenceau, J. R., Barnfather, I., Edgar, M., Basil, A., Hwang, T. H., & Quinones-Hinojosa, A. (2025). Multi-Omics Integration and Mapping of Invasion Markers Reveal Tumor-Specific Druggable Targets in Primary Human Glioblastoma. Neurosurgery, 71(Supplement_1), 121–122. https://doi.org/10.1227/neu.0000000000003360_494 LWW Link

