---
date: 2021-06-16
title: "Investigating the Classification of Breast Cancer Subtypes using KMeans"
linkTitle: AI in Healthcare
tags: ["project", "reu", "ai", "health"]
description: "This project provides an insight into an investigation of the classification of breast cancer sub-types using proetomic dataset through a machine learning approach." 
author: Kehinde, Ezekiel
github_url: https://github.com/cybertraining-dsc/su21-reu-362/edit/main/project/index.md
resources:
- src: "**.{png,jpg}"
  title: "Image #:counter"
---

[![Check Report](https://github.com/cybertraining-dsc/hid-example/workflows/Check%20Report/badge.svg)](https://github.com/cybertraining-dsc/su21-reu-362/actions)
[![Status](https://github.com/cybertraining-dsc/hid-example/workflows/Status/badge.svg)](https://github.com/cybertraining-dsc/su21-reu-362/actions)
Status: final, Type: Project

Kehinde Ezekiel, [su21-reu-362](https://github.com/cybertraining-dsc/su21-reu-362), [Edit](https://github.com/cybertraining-dsc/su21-reu-362/blob/main/project/index.md)

{{% pageinfo %}}


## Abstract

Breast cancer is an heterogenous disease that is characterized by abnormal growth of the cells in the breast region[^1]. There are four major molecular subtypes of breast cancer. This classification was based on a 50-gene signature profiling test called PAM50. Each molecular subtype has a specific morphology and treatment plan. Early diagnosis and detection of possible cancerous cells usually increase survival chances and provide a better approach for treatment and management. Different tools like ultrasound, thermography, mammography utilize approaches like image processing and artificial intelligence to screen and detect breast cancer. Artificial Intelligence (AI) involves the simulation of human intelligence in machines and can be used for learning or to solve problems. A major subset of AI is Machine Learning which involves training a piece of software (called model) to makwe useful predictions using dataset. 

In this project, a machine learning algorithm, KMeans, was implemented to design and analyze a proteomic dataset into clusters using its proteins identifiers. These protein identifiers were associated with the PAM50genes that was used to originally classify breast cancer into four molecular subtypes. The project revealed that further studies can be done to investigate the relationship between the data points in each cluster with the biological properties of the molecular subtypes which could lead to newer discoveries and developmeny of new therapies, effective treatment plan and management of the disease. It also suggests that several machine learning algorithms can be leveraged upon to address healthcare issues like breast cancer and other diseases which are characterized by subtypes. 

Contents

{{< table_of_contents >}}

{{% /pageinfo %}}

**Keywords:** AI, cancer, breast, algorithms, machine learning, healthcare, subtypes, classification.

## 1. Introduction

Breast cancer is the most common cancer, and also the primary cause of mortality due to cancer in females around the World. It is an heterogenous disease that is characterized by the abnormal growth of cells in the breast region[^1]. Early diagnosis and detection of possible cancerous cells in the breast usually increase survival chances and provide a better approach for treatment and management. Treatment and management often depend on the stage of cancer, the subtype, the tumor size, location and many other factors. During the last 20 years, four major intrinsic molecular subtypes for breast cancer- luminal A, luminal B, HER2-enriched and Basal-like have been identified, classified and intensively studied.  Each subtype has its distinct morphologies and clinical treatment. The classification is based on gene expression profiling, specificaly defined by mRNA expression of 50 genes (also known as, PAM50 Genes). This test is known as the PAM50 test. The accurate grouping of breast cancer into its relevant subtypes can improve accurate treatment-decision making[^2]. The PAM50 test is now known as the Prosigna Breast Cancer Prognostic Gene Signature Assay 50 (known as Prosigna) and it analyzes the activity of certain genes in early-stage, hormone-receptor-positive breast cancer[^3]. This classification is based on the mRNA expression and the activity of 50 genes and it aims to estimate the risk of distant reccurrence of breast cancer. Since the assay was based on mRNA expression, this project suggested that a classification based on the final product of mRNA, that is protein, can be implemented to investigate its role in the classifictaion of molecular breast cancer subtypes. As a result, the project was focused on the use of a proteomic dataset which contained published iTRAQ proteome profiling of 77 breast cancer samples and expression values for the proteins of each sample.

Most times, breast cancer is diagnosed and detected through a combination of different approaches such as imaging (e.g. mammogram and ultrasound), physical examination by a radiologist and biopsy. Biopsy is used to confirm the breast cancer symptoms. However, research has shown that radiologists can miss up to 30% of breast cancer tissues during detection[^4]. This gap has brought about the introduction of Computer aided Diagnosis (CAD) systems can help detect abnormalities in an efficient manner. CAD is a technology that includes utilizing the concept of artificial intelligence(AI) and medical image processing to find abnormal signs in the human body[^5].  Machine Learning is a subset of AI and it has several algorithms that can be used to build a model to perform a specific task or to predict a pattern. KMeans is one of such algorithm.

Building a model using machine learning involves selecting and preparing the appropriate dataset, identifying the accurate machine learnning algorithm to use, training the algorithm on the data to build a model, validating the resulting model's performance on testing data and using the model on a new data[^6]. In this project, KMeans was the algorithm used in this project, the datasets were prepared through several procedures like filtering, merging. KMeans clustering method was used to investigate the classification of the molecular subtypes. Its efficacy is often tested by a silhouette score. A silhouette score shows how similar an object is to its own cluster and it ranges from -1 to 1 where a high values indicates that an object is well matched to its own cluster. A homogeneity score determines if a cluster should only contain samples that belong to a particular class. It ranges from a value between 0 to 1 with low values indicating a low homogeneity. 

The project investigated the efficient number of clusters that could be generated for the proteome dataset which would consequetly provide an optimal classification of the protein expression values for the breast cancer samples. The proteins that were used in the KMeans analysis were the proteins that were associated with the PAM50 genes. The result of the project could provide insights to medical scientists and researchers to identify any interelatedness between the original classification of breast cancer molecular subtypes.

## 2. Datasets

Datasets are eseential in drawing conclusion. In the diagnosis, detection and classification of breast cancecr, datasets have been essential to draw conclusion by identifying patterns. These datasets range from imaging datasets to clinical datasets, proteomic datasets etc. Large amounts of data have been collected due to new technological and computational advances like the use of websites like NCBI, equipments like Electroencephalogram (EEG) which record clinical information.  Medical researchers leverage these datasets to make useful health care decisions that affect a region, gender or the world. The need for accuracy and reproducibilty has led to the use of machine learning as an important tool for drawing conclusions.

Machine Learning involves training a piece of software, also known as model, to idnetify patterns from a dataset and make useful predictions. There are several factors to be considered when using datasets. One of such is data privacy. Recently, measures have been taken to ensure that the privacy of data. Some of these measures include, replacing codes for patients name, using documents and mobile applications that ask for permission from patients before using their data. Recently, the World Health Organization (WHO) made her report on AI and provided priniples that ensure that AI works for all. On of such is that the designer of AI technologies should satisfy regulatory requirements for safety, accuracy and efficacy for well-defined use cases or indications. Measures of quality control in practice and quality improvement in the use of AI must be available[^7]. Building a model using machine learning involves selecting and preparing the appropriate dataset, identifying the accurate machine learnning algorithm to use, training the algorithm on the data to build a model, validating the resulting model's performance on testing data and using the model on a new data[^6]. In this project, KMEans was the algorithm used in this project, the datasets were prepared through several procedures like filtering, merging.

## 3. The KMeans Approach

KMeans clustering is an unsupervised machine learning algorithm that makes inferences from datasets without referring to a known outcome. It aims to identify underlying patterns in a dataset by looking for a fixed number of clusters, (known as k). The required number of clusters is chosen by the person building the model. KMeans was used in this project to classify the protein IDs (or RefSeq_IDs) into clusters. Each cluster was designed to be associated with related protein IDs.

Three datasets were used for the algorithm. The first and main dataset was a proteomic dataset. It contained published iTRAQ proteome profiling of 77 breast cancer samples generated by the Clinical Proteomic Tumor Analysis Consortium (NCI/NIH). Each sample contained expression values for ~12000 proteins, with missing values present when a given protein could not be quantified in a given sample. The variables in the dataset included the RefSeq_accession_number(also known as RefSeq protein ID), "the gene_symbol" (which was unique to each gene), "the gene_name" (which was the full name of the gene). The remaining columns were the log2 iTRAQ ratios for each of the 77 samples while the last three columns are from healthy individuals.

The second dataset was a PAM50 dataset. It contained the list of genes and proteins used in the PAM50 classification system. The variables include the RefSeqProteinID which matched the Protein IDs(or RefSeq_IDs) in the main proteome dataset. 

The third dataset was a clinical data of about 105 clinical breast cancer samples.  77 of the breast cancer samples were the samples in the first dataset. The excluded samples were as a result of protein degradation[^8]. The variables in the dataset are:
‘Complete TCGA ID', 'Gender', 'Age at Initial Pathologic Diagnosis', 'ER Status', 'PR Status', 'HER2 Final Status', 'Tumor', 'Tumor--T1 Coded', 'Node', 'Node-Coded', 'Metastasis', 'Metastasis-Coded', 'AJCC Stage', 'Converted Stage', 'Survival Data Form', 'Vital Status', 'Days to Date of Last Contact', 'Days to date of Death', 'OS event', 'OS Time', 'PAM50 mRNA', 'SigClust Unsupervised mRNA', 'SigClust Intrinsic mRNA', 'miRNA Clusters', 'methylation Clusters', 'RPPA Clusters', 'CN Clusters', 'Integrated Clusters (with PAM50)', 'Integrated Clusters (no exp)', 'Integrated Clusters (unsup exp).'

During the preparation of the datasets for KMeans analysis, unused columns like "gene_name" and "gene_symbol"  were removed in the first dataset. The first and third dataset were merged together. Prior to merging, the variable 'Complete TCGA ID' in the third dataset was found to be the same as the TCGAs in the first dataset. The Complete TCGA ID refered to a breast cancer patient, some patients were found in both datasets. The TCGA ID in the first dataset was renamed to match with the TCGA of the third dataset, thereby giving the same syntax. The first dataset was also transposed as a row and its gene expression as the columns. These processes were done in order to merge both dataset efficiently.

After merging, the "PAM5O RNA" variable from the second dataset was selected to join the merged dataset. This single dataset was named "pam50data". It contained all the variables that were needed for KMeans Analysis which included the genes that were used for the PAM50 classification (only 43 were available in the dataset), the complete TCGA ID of each 80 patient, and their molecular tumor type. Missing values in the dataset were imputed using SimpleImputer. Then, KMeans clustering was performed. The metrics were tested with cluster numbers of 3, 4, 5, 20 and 79. The bigger numbers (20 and 79) were tested just for comparison. Further details on the codes written can be found in [^9]. Also, [^10] and [^11] were kernels that provided insights for the written code.


## 5. Results and Images

Several codes were written to determine the best number of clusters for the model. The effectiveness of a cluster is often measured by scores such as silhouette score, homogeneity score and adjusted rand score.

The silhouette score for a cluster of 3, 4, and 5, 8, 20 and 79 were 0.143, 0.1393, 0.1193, 0.50968, 0.0872, 0.012 while the homogenenity scores were 0.4635, 0.4749, 0.1193, 0.5617, 0.6519 and 1.0 respectively.  The homogeneity score for 79 is 1.0 since the algorithm can assign all the points into sepearate clusters. However, it is not efficient for the dataset we used. A cluster of 3 works best since the silhouette score is high and the homogeneity score jumps ~2-fold. 

Figures 1 and 2 show the results of the visualization of the clusters of 3 and 4.

![Figure 1](https://github.com/cybertraining-dsc/su21-reu-362/raw/main/project/images/new.png)


**Figure 1:** The classification of Breast Cancer Moleecular Subtypes using KMeans Clustering. (k=3). Each data point represnt the expression value for the genes that were used for clustering.

![Figure 2](https://github.com/cybertraining-dsc/su21-reu-362/raw/main/project/images/k%3D4_image.png)

**Figure 2:** The classification of Breast Cancer Moleecular Subtypes using KMeans Clustering. (k=4). Each data point represnt the expression value for the genes that were used for clustering.


## 6. Benchmark

This program was executed on a Google Colab server and the entire runtime took 1.012 seconds Table 1 lists the amount of time taken to loop for n_components. The n_components is gotten from the code and it refers to the features of the dataset.

| Name        | Status  | Time(s)  |
|-------------|---------|-------   |
| parallel 1  |   ok    | 0.647    |
| parallel 3  |   ok    | 0.936    |
| parallel 5  |   ok    | 0.952    |
| parallel 7  |   ok    | 0.943    |
| parallel 9  |   ok    | 1.002    |
| parallel 11 |   ok    | 0.991    |
| parallel 13 |   ok    | 0.958    |
| parallel 15 |   ok    | 1.012    |

**Benchmark:** The table shows the parallel process time take the for loop for n_components. 
 
## 7. Conclusion

The results of the KMeans analysis showed that three clusters provided an optimal result for the classification using a proteomic dataset. A cluster of 3 provided a balanced silhouette and homogeneity score. This predict that some interrelatedness could exist between the original PAM50 subtype classfication, since the result of classifying a protein dataset using a machine learning algorithm identified a cluster of 3 as one with the optimal result.
Also, future research could be done by using other machine learning algorithms, possibly a supervised learning algotithm, to identify the correlation between the clusters and the four molecular subtypes.
This model can be improved on and if proven to show that there truly exist a relationship between the four molecular subtypes, more research could be done to identify the factors that contribure to the interelatedness. This would lead medical scientists and researchers to work on better innovative methods that will aid the treatment and management of breast cancer.

## 8. Acknowledgments

This projected was immensely supported by Dr. Gregor von Laszewski.
Also, a big appreciation to the REU Instructors (Carlos Theran, Yohn Jairo and Victor Adankai) for their contribution, support, teachings and advice.
Also, gratitude to my colleagues who helped me out; Jacques Fleischer, David Umanzor and Sheimy Paz Serpa. gratitude to my colleagues.
Lastly, appreciation to Dr. Byron Greene, the Florida A&M University, the Indiana University and Bethune Cookman University for providing a platform to be able to learn new things and embark on new projects. 


## 9. References

[^1]: Akram, Muhammad et al. "Awareness and current knowledge of breast cancer." Biological research vol. 50,1 33. 2 Oct. 2017, doi:10.1186/s40659-017-0140-9

[^2]: Wallden, Brett et al. "Development and verification of the PAM50-based Prosigna breast cancer gene signature assay." BMC medical genomics vol. 8 54. 22 Aug. 2015, doi:10.1186/s12920-015-0129-6

[^3]: Breast Cancer.org Prosigna Breast Cancer Prognostic Gene Signature Assay. <https://www.breastcancer.org/symptoms/testing/types/prosigna>

[^4]: L. Hussain, W. Aziz, S. Saeed, S. Rathore and M. Rafique, "Automated Breast Cancer Detection Using Machine Learning Techniques by Extracting Different Feature Extracting Strategies," 2018 17th IEEE International Conference On Trust, Security And Privacy In Computing And Communications/ 12th IEEE International Conference On Big Data Science And Engineering (TrustCom/BigDataSE), 2018, pp. 327-331, doi: 10.1109/TrustCom/BigDataSE.2018.00057. 

[^5]: Halalli, Bhagirathi et al. "Computer Aided Diagnosis - Medical Image Analysis Techniques." 20 Dec. 2017, doi: 10.5772/intechopen.69792

[^6]: Salod, Zakia, and Yashik Singh. "Comparison of the performance of machine learning algorithms in breast cancer screening and detection: A protocol." Journal of public health research vol. 8,3 1677. 4 Dec. 2019, doi:10.4081/jphr.2019.1677Articles

[^7]:  WHO, WHO issues first global report on Artificial Intelligence (AI) in health and six guiding principles for its design and use. <https://www.who.int/news/item/28-06-2021-who-issues-first-global-report-on-ai-in-health-and-six-guiding-principles-for-its-design-and-use>


[^8]: Mertins, Philipp et al. "Proteogenomics connects somatic mutations to signalling in breast cancer." Nature vol. 534,7605 (2016): 55-62. doi:10.1038/nature18003

[^9]: Kehinde Ezekiel, Project Code, <https://github.com/cybertraining-dsc/su21-reu-362/blob/main/project/code/final_breastcancerproject.ipynb>

[^10]: Kaggle_breast_cancer_proteomes <<https://pastebin.com/A0Wj41DP>

[^11]: Proteomes_clustering_analysis <https://www.kaggle.com/shashwatwork/proteomes-clustering-analysis>

[^12]: Gregor von Laszewski, Cloudmesh StopWatch and Benchmark from the Cloudmesh Common Library, [GitHub] 
      <https://github.com/cloudmesh/cloudmesh-common>

