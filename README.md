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

## **1. Project Overview**
Brain cancer remains one of the most aggressive and life-threatening malignancies worldwide. Studies shows that different subtypes (glioblastoma vs ependymoma) require vastly different treatment approaches, making accurate classification essential. Thus, this capstone project leverages machine learning and gene expression analysis to classify brain cancer subtypes and identify potential biomarkers for diagnostic and therapeutic applications.This capstone project focuses on the computational analysis of the Brain_GSE50161 dataset, containing 54,676 gene expression features across 130 samples representing four distinct brain cancer types (ependymoma, glioblastoma, medulloblastoma, pilocytic astrocytoma) and normal tissue. The primary objective is to develop machine learning models capable of accurately classifying brain cancer subtypes while identifying potential biomarkers for diagnostic and therapeutic applications.

### 1.1 **Aims and Objectives:**
- Analyze gene expression patterns across 4 brain cancer subtypes and normal tissue, which drives tumor growth and subtype differentiation
- Develop supervised learning models for accurate brain cancer subtype classification
- Identify "Elite" genes (potential biomarkers) with highest diagnostic value
- Evaluate therapeutic insights for precision oncology applications
- Address challenges of high dimensionality and small sample size


### 1.2 **Why This Matters**

| Challenge | Our Solution |
|-----------|--------------|
| 54,676 genes make analysis complex | **30 genes** provide 92%+ accuracy |
| Traditional analysis misses subtle patterns | **ML identifies** hidden genetic signatures |
| Full genome sequencing is expensive | **Cost-effective** diagnostic panels possible |
| Treatment varies by subtype | **Precision oncology** becomes accessible |



## 2. Dataset Description
The Brain_GSE50161 dataset contains gene expression profiles from 130 human brain tissue samples, comprising four distinct tumor types and normal tissue controls. This microarray data provides a comprehensive molecular portrait of brain cancer subtypes.
- **Data Name:** Brain_GSE50161.csv 
- **Size of Data:** >120MB
- **Missing Values:** None
- **Source:** Kaggle [https://www.kaggle.com/datasets/brunogrisci/brain-cancer-gene-expression-cumida]

### **2.1 Dataset Statistics**
---
| Attribute | Value |
|-----------|-------|
| **Total Samples** | 130 |
| **Gene Features** | 54,676 |
| **Classes** | 5 (4 tumor types + normal) |
| **Data Type** | Microarray gene expression |

### **2.2 Class Distribution**
---
| Class | Count | Percentage |
|-------|-------|------------|
| Ependymoma | 46 | 35.4% |
| Glioblastoma | 34 | 26.2% |
| Medulloblastoma | 22 | 16.9% |
| Pilocytic Astrocytoma | 15 | 11.5% |
| Normal | 13 | 10.0% |

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




# Brain Cancer Gene Expression Analysis for Subtype Classification and Biomarker Discovery

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![scikit-learn](https://img.shields.io/badge/scikit--learn-1.0%2B-orange)
![License](https://img.shields.io/badge/license-MIT-green)
![Last Updated](https://img.shields.io/badge/last%20updated-March%202025-brightgreen)

## 📋 Table of Contents
- [Project Overview](#project-overview)
- [Team Members](#team-members)
- [Key Findings](#key-findings)
- [Dataset](#dataset)
- [Methodology](#methodology)
- [Results](#results)
- [Installation](#installation)
- [Usage](#usage)
- [Model Performance](#model-performance)
- [Biomarker Discovery](#biomarker-discovery)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

## 🎯 Project Overview

Brain cancer remains one of the most aggressive and life-threatening malignancies worldwide. This project leverages machine learning and gene expression analysis to classify brain cancer subtypes and identify potential biomarkers for diagnosis and treatment.

**Key Objectives:**
- 🔬 Analyze gene expression patterns across 4 brain cancer subtypes and normal tissue
- 🤖 Develop ML models for accurate subtype classification
- 🧬 Identify "Elite" genes as potential biomarkers
- 💊 Evaluate therapeutic insights for precision oncology
- ⚡ Optimize high-dimensional data processing

## 👥 Team Members (Group 19)

| Name | Role | GitHub | Email |
|------|------|--------|-------|
| **Eije, Oloche Celestine** | Team Lead | [@Eije1](https://github.com/Eije1) | eijeoloche1@gmail.com |
| Aremu, Jacobs Opeyemi | Member | [@aremu-jacobs](https://github.com/aremu-jacobs) | jacobsage4ril@gmail.com |
| Ikhalea, Emmanuel | Member | [@DeveloperIkhalea](https://github.com/DeveloperIkhalea) | Dev.ikhalea@gmail.com |
| David, Brainerd | Member | [@Brainerd007](https://github.com/Brainerd007) | brainerddavid9@gmail.com |
| Ezeokwelume, Mary | Member | [@obyokwelume-coder](https://github.com/obyokwelume-coder) | obyokwelume@gmail.com |
| Itunu, Ifeoluwa Adeniji | Member | [@Ife-ahav](https://github.com/Ife-ahav/Ife.git) | itunuadeniji31@gmail.com |
| Ajibola, Joshua | Member | [@JManBoss](https://github.com/JManBoss/joshman.github.io.git) | joshuaajibola00@gmail.com |
| Raji, Ridwanullah | Member | [@DevRSR](https://github.com/DevRSR) | rajiridwanullah25@gmail.com |
| Sule, Wasiu Ayinde | Member | [@Engrbolajipraise1](https://github.com/Engrbolajipraise1) | bolajipraise1@gmail.com |
| Muhammed, Olatunji Tiamiyu | Member | [@olatunjee9](https://github.com/olatunjee9) | tiamiyuolatunji1@gmail.com |

## 📊 Key Findings

- **Best Model:** Random Forest achieved **92.31% accuracy** after hyperparameter tuning
- **Feature Reduction:** Reduced from 54,675 genes to **30-gene signature** using RFE
- **Cross-Validation:** Maintained **89.23%** average CV score
- **Key Biomarkers:** Identified Gene 54638 and Gene 33848 as top discriminators
- **PCA Analysis:** First 2 components explain significant variance in tumor subtypes

## 📁 Dataset

**Source:** Brain_GSE50161.csv from Gene Expression Omnibus (GEO)

| Attribute | Value |
|-----------|-------|
| Samples | 130 |
| Features | 54,676 genes |
| Classes | 5 (4 tumor types + normal) |
| Tumor Types | Ependymoma, Glioblastoma, Medulloblastoma, Pilocytic Astrocytoma, Normal |

**Class Distribution:**
- Ependymoma: 46 samples
- Glioblastoma: 34 samples
- Medulloblastoma: 22 samples
- Pilocytic Astrocytoma: 15 samples
- Normal: 13 samples

## 🔬 Methodology

### Data Preprocessing
- ✅ Data cleaning and missing value check
- ✅ StandardScaler normalization
- ✅ Label encoding for target variable

### Feature Selection
- ✅ Variance threshold filtering
- ✅ ANOVA F-tests (SelectKBest)
- ✅ Random Forest feature importance
- ✅ Recursive Feature Elimination (RFE)

### Machine Learning Models
1. **Logistic Regression** (Baseline)
2. **Random Forest Classifier**
3. **Random Forest with RFE + Hyperparameter Tuning**

### Evaluation Strategy
- 80/20 Train-Test split
- 5-Fold Cross-Validation
- Metrics: Accuracy, Precision, Recall, F1-score
- Confusion Matrix analysis

## 📈 Results

### Model Performance Comparison

| Model | Accuracy | Precision | Recall | F1-Score |
|-------|----------|-----------|--------|----------|
| Logistic Regression | 84.62% | 0.85 | 0.85 | 0.84 |
| Random Forest | 88.46% | 0.88 | 0.88 | 0.88 |
| **Random Forest (Tuned + RFE)** | **92.31%** | **0.92** | **0.92** | **0.92** |

### Top 10 Biomarkers Identified

| Rank | Gene | Log2FC | p-value | -log10p |
|------|------|--------|---------|---------|
| 1 | Gene 54638 | ... | ... | ... |
| 2 | Gene 33848 | ... | ... | ... |
| 3 | Gene 51378 | ... | ... | ... |
| 4 | Gene 15466 | ... | ... | ... |
| 5 | Gene 31086 | ... | ... | ... |
| 6 | Gene 18487 | ... | ... | ... |
| 7 | Gene 19603 | ... | ... | ... |
| 8 | Gene 11886 | ... | ... | ... |
| 9 | Gene 19474 | ... | ... | ... |
| 10 | Gene 15637 | ... | ... | ... |




## 📋 Table of Contents
- [Project Overview](#project-overview)
- [Key Findings](#key-findings)
- [Team Members](#team-members)
- [Dataset](#dataset)
- [Methodology](#methodology)
- [Results](#results)
- [Biomarker Discovery](#biomarker-discovery)
- [Installation](#installation)
- [Usage](#usage)
- [Model Performance](#model-performance)
- [Repository Structure](#repository-structure)
- [Real-World Applications](#real-world-applications)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)
- [Acknowledgments](#acknowledgments)

---


---

## 📊 Key Findings

| Metric | Value |
|--------|-------|
| **Best Model Accuracy** | **92.31%** |
| Feature Reduction | 54,675 → 30 genes (99.95% reduction) |
| Cross-Validation Score | 89.23% |
| Top Biomarkers | Gene 54638, Gene 33848 |
| Baseline Improvement | +7.69% over Logistic Regression |


## Dataset
---
**Source:** [Gene Expression Omnibus (GEO)]([https://www.ncbi.nlm.nih.gov/geo/](https://www.kaggle.com/datasets/brunogrisci/brain-cancer-gene-expression-cumida)) - Brain_GSE50161

### Dataset Statistics

| Attribute | Value |
|-----------|-------|
| **Total Samples** | 130 |
| **Gene Features** | 54,676 |
| **Classes** | 5 (4 tumor types + normal) |
| **Data Type** | Microarray gene expression |

### Class Distribution

| Class | Count | Percentage |
|-------|-------|------------|
| Ependymoma | 46 | 35.4% |
| Glioblastoma | 34 | 26.2% |
| Medulloblastoma | 22 | 16.9% |
| Pilocytic Astrocytoma | 15 | 11.5% |
| Normal | 13 | 10.0% |

<p align="center">
  <img src="figures/class_distribution.png" alt="Class Distribution" width="500"/>
</p>

---

## Methodology

### Data Preprocessing Pipeline

```python
# Key preprocessing steps
1. Data loading and inspection
2. Missing value check (none found)
3. Feature renaming (Gene 1 to Gene 54675)
4. StandardScaler normalization
5. Label encoding for target variable


---

## 📊 Key Findings

| Metric | Value |
|--------|-------|
| **Best Model Accuracy** | **92.31%** |
| Feature Reduction | 54,675 → 30 genes (99.95% reduction) |
| Cross-Validation Score | 89.23% |
| Top Biomarkers | Gene 54638, Gene 33848 |
| Baseline Improvement | +7.69% over Logistic Regression |

---



---

## Dataset

**Source:** [Gene Expression Omnibus (GEO)](https://www.ncbi.nlm.nih.gov/geo/) - Brain_GSE50161

### Dataset Statistics

| Attribute | Value |
|-----------|-------|
| **Total Samples** | 130 |
| **Gene Features** | 54,676 |
| **Classes** | 5 (4 tumor types + normal) |
| **Data Type** | Microarray gene expression |

### Class Distribution

| Class | Count | Percentage |
|-------|-------|------------|
| Ependymoma | 46 | 35.4% |
| Glioblastoma | 34 | 26.2% |
| Medulloblastoma | 22 | 16.9% |
| Pilocytic Astrocytoma | 15 | 11.5% |
| Normal | 13 | 10.0% |

<p align="center">
  <img src="figures/class_distribution.png" alt="Class Distribution" width="500"/>
</p>

---

## 🔬 Methodology

### Data Preprocessing Pipeline

```python
# Key preprocessing steps
1. Data loading and inspection
2. Missing value check (none found)
3. Feature renaming (Gene 1 to Gene 54675)
4. StandardScaler normalization
5. Label encoding for target variable
