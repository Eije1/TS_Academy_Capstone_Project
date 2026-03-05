# **TS ACADEMY Capstone Project - Group 19 (March 2026)**

### Title: Brain Cancer Gene Expression Analysis for Subtype Classification and Biomarker Discovery

## Project Overview

This capstone project focuses on the computational analysis of the Brain_GSE50161 dataset, containing 54,676 gene expression features across 130 samples representing four distinct brain cancer types (ependymoma, glioblastoma, medulloblastoma, pilocytic astrocytoma) and normal tissue. The primary objective is to develop machine learning models capable of accurately classifying brain cancer subtypes while identifying potential biomarkers for diagnostic and therapeutic applications.

**Aims and Objectives:**
- Analyze gene expression patterns driving tumor growth and subtype differentiation
- Develop supervised learning models for accurate brain cancer subtype classification
- Identify "Elite" genes (potential biomarkers) with highest diagnostic value
- Evaluate therapeutic insights for precision oncology applications
- Address challenges of high dimensionality and small sample size

---

## Team Members (Group 19)

| S/N | Name | Role | GitHub | Email |
|---|----------|-------------|------------|----------|
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

---

## Dataset Description

- **Source:** Gene Expression Omnibus (GEO) - Brain_GSE50161
- **Samples:** 130 patient samples
- **Features:** 54,676 gene expression probes
- **Classes:** 5 categories (4 tumor types + normal tissue)
  - Ependymoma
  - Glioblastoma
  - Medulloblastoma
  - Normal
  - Pilocytic Astrocytoma

### Why This Matters

Brain cancer remains one of the most aggressive malignancies worldwide. Different subtypes (glioblastoma vs ependymoma) require vastly different treatment approaches. Our work demonstrates that:

- **Full genome sequencing isn't necessary** - just 30 genes provide 92%+ accuracy
- **Machine learning can identify subtle genetic patterns** invisible to traditional analysis
- **Cost-effective diagnostic panels** can be developed using our elite gene signature
- **Precision oncology** becomes more accessible with targeted genetic testing

## Metrics

                       precision    recall  f1-score   support
           ependymoma       1.00      0.89      0.94         9
         glioblastoma       0.88      1.00      0.93         7
      medulloblastoma       1.00      0.75      0.86         4
               normal       1.00      1.00      1.00         3
    pilocytic_astrocytoma   0.75      1.00      0.86         3
             accuracy                           0.92        26
            macro avg       0.93      0.93      0.92        26
         weighted avg       0.94      0.92      0.92        26

## Confusion Matrix

                     Predicted
                     
    Actual           Epi  Glio  Med  Nor  Pil
    
    Ependymoma        8    1    0    0    0
    Glioblastoma      0    7    0    0    0
    Medulloblastoma   1    0    3    0    0
    Normal            0    0    0    3    0
    Pilocytic Astro   0    0    0    0    3

## Model Performance Evolution

| Phase | Model | Features | Accuracy |
|-------|-------|----------|----------|
| 1 | Logistic Regression | 100 | 84.62% |
| 2 | Random Forest | 100 | 88.46% |
| 3 | RFE + Random Forest | 30 | 92.31% |
| 4 | GridSearchCV Tuned | 30 | 92.31% |


## Elite Genes (Biomarker Discovery)


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

## Methodology

- **Data Preprocessing:** We imported the dataset via Google Colab, removed non-informative columns, and encoded categorical labels. We utilized StandardScaler to normalize gene expression values and audited the data for consistency
- **Exploratory Data Analysis (EDA):** We performed class distribution analysis using df.info() and df.describe(). Data visualization was conducted using Matplotlib and Seaborn to identify trends and feature correlations.
- **Feature Selection:** We employed a multi-stage pipeline: Variance Threshold filtering, ANOVA F-tests (SelectKBest), and Feature Importance Ranking using Random Forest.
- **Machine Learning Models:** We developed a Logistic Regression baseline and a high-performance Random Forest Classifier. After which we went ahead to develop a RFE selection and a Hyperparameter Tuning.

## Model Evaluation

- **Strategy:** We utilized an 80/20 Train-Test split and 5-Fold Cross-Validation to ensure model stability.
- **Metrics:** Performance was measured using Accuracy, Precision, Recall, and F1-score.
- **Error Analysis:** Confusion Matrices were generated to visualize classification performance across subtypes.

## Results & Conclusion

- **Best Model:** Random Forest outperformed Logistic Regression, reaching a peak accuracy of 88.46% from 84.62% by capturing complex, non-linear biological relationships.
- **Efficiency:** Feature selection was vital; reducing the gene count from 54,675 to a 30-gene signature using the RFE method and Hypertuning significantly improved model robustness and accuracy to 92.31% and also reduced overfitting.
- **Stability:** Our final model maintained a solid 89.23% average Cross-Validation score.
- **Conclusion:** Computational analysis of microarray data is a powerful ally for precision oncology, enabling faster and more reliable tumor subtyping.

### Real-World Applications

- **Clinical Diagnostics**: Develop PCR-based test panels targeting the 30 elite genes
- **Drug Discovery**: Investigate top biomarkers as therapeutic targets
- **Treatment Planning**: Faster, more accurate subtype identification
- **Research Tool**: Open-source pipeline for other cancer type analysis


