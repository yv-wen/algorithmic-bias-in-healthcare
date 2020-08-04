# Algorithmic Bias In Healthcare

### Introduction
While machine learning has brought about many positive improvements and solutions in our lives today, the use of it has also surfaced problematic issues that need to be addressed. One particular issue is that machine learning can amplify bias if the bias is not addressed in the first place. A [recent study](https://www.washingtonpost.com/health/2019/10/24/racial-bias-medical-algorithm-favors-white-patients-over-sicker-black-patients/) has raised such an issue in the field of healthcare. In response to these types of issues that machine learning poses, we're aiming to first appreciate the scope of the embedded bias in data that we face today, and then diagnose the source of the bias. The bias of interest in this research is historical or systemic bias, particularly against certain demographics. How we'll go about in achieving this aim is based on the methodology laid out in the paper, "Predicting Bias in Machine Learned Classifiers Using Clustering" (R.Thomson, E.Alhajjar, J.Irwin and T.Russell). 

### Methodology 
We'll first use clustering methods to find distinct clusters or patterns in the dataset, analyze those patterns if there are any, and then create a predictive algorithm to test its performance against those clusters to identify and diagnose any embedded bias in the data. The assumption behind this methodology is that the clusters are "unbiased", since clusters are distance or density-based. In our approach, we'll make the clustering and the predictive modeling race and gender-blind, though we recognize that excluding sensitive personal data does not completely remove bias. 

The following machine learning techniques are used:
- Clustering
  - K-Means
  - DBSCAN
  - HDBSCAN
  - Agglomerative Clustering
- Predictive Modeling
  - RandomForestClassifier

### Dataset
Our data of interest is in-patient data on diabetic patients over a span of 10 years (1999-2008) from 130 hospitals and integrated delivery networks in the U.S. The dataset is available on UCI Machine Learning Repository, contributed by the Center for Clinical and Translational Research at Virginia Commonwealth University. It includes 50 features, giving information on patients' demographics, hospital outcomes, medical history, and diabetic treatments.

### Contents
Initial EDA steps, preprocessing, and modeling for both the unsupervised and unsupervised portions of the project are detailed in the following order:
- 1_EDA.ipynb
- 2_Preprocessing_Cluster.ipynb
- 3_Modeling_Clustering.ipynb
- 4_Preprocessing_Classifier.ipynb
- 5_Modeling_Classifier.ipynb
