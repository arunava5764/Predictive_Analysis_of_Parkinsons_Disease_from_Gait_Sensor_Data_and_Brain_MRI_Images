<div align="center">
<!-- <h1>Predictive_Analysis_of_Parkinsons_Disease_from_Gait_Sensor_Data_and_Brain_MRI_Images: Predictive Analysis of Parkinsons Disease from Gait Sensor Data and Brain MRI Images</h1> -->
<h2><a href="MTP Report.pdf">Predictive Analysis of Parkinsons Disease from Gait Sensor Data and Brain MRI Images</a></h2>
    
[Arunava Chaudhuri](https://github.com/arunava5764)<sup></sup>,        [Dr. Deepti R. Bathula](https://www.iitrpr.ac.in/deepti-r-bathula)<sup></sup>
    
<sup></sup>[Indian Institute of Technology, Ropar](https://www.iitrpr.ac.in/)
</div>

<p align="center">
<img src="Diagrams/siamese.PNG" width=100% height=100% 
class="center">
</p>

This experiment is an extension to the experiment on achieving higher accuracy and lower error using newly developed feature level fusion technique used aggressively in Computer Vision. We have tried to add more functionality to use features coming from different subjects. The unavailability of MRI, SPECT, f-MRI, CT images of patients in many occasions make the situation harder for a doctor to detect Parkinson’s disease based on only clinical diagnosis. Our experiment shows that even if patient have only Gait data or only PPMI data, we can still detect if he/she has the disease or not. This will eventually help us to implement this facility in situations where some doctor has to diagnosis a patients based on several modality’s data. We have successfully evaluated the possibility of achieving better accuracy using feature level fusion of several modalities where data comes from different subjects. The attempt to combine the features of different domain comes out to be an unique combination to find pattern in Parkinson’s disease patient data. While the aim is for accurate prediction in medical domain it has also eliminate the need for having all kinds of information required for classifying a particular disease of a patient.

<details>
  <summary>Table of Contents</summary>
  <ol>
    <li><a href="#catalog">Catalog</a></li>
    <li><a href="#Comparison-Between-Multi-Modality-and-Baseline-Single-Modality">Comparison Between Multi-Modality and Baseline Single Modality</a></li>
    <li><a href="#Comaprison-With-Previous-PPMI-Experiment">Comaprison With Previous PPMI Experiment</a></li>
    <li><a href="#Comaprison-With-Previous-Gait-Experiment">Comaprison With Previous Gait Experimen</a></li>
    <li><a href="#acknowledgement">Acknowledgement</a></li>
  </ol>
</details>



## catalog

## Comparison Between Multi-Modality and Baseline Single Modality

So, if we consider our previous experiment on individual dataset using individual model it is evident that, proposed architecture has able to improve the accuracy along with Cohen Kappa score and ROC AUC value using those multi-modal features. The same scenario is described in the below comparison chart.

| Topic | Gait Model | PPMI Model | Multi-Model |
|---|:---:|:---:|:----:|
| Features | 128 Features | 1595 Features | 1721 Features |
| Parameters | 2214 | 211,852 | 218,676 |
| Loss Function | Sparse Categorical CrossEntropy | Sparse Categorical CrossEntropy | Triplet Loss |
| Optimizer | RMSprop | RMSprop | RMSprop |
| Accuracy | 89.61% | 92.13 | Gait : 98.7, PPMI : 99.11 |
| ROC AUC Score | 85% | 84% | Gait : 0.9782, PPMI : 0.9864 | 
| Cohen Kappa Score | 0.7310 | 0.74 | Gait : 0.9686, PPMI : 0.9613 | 

## Comaprison With Previous PPMI Experiment

We have compared our model several other previous research works produced using same Gait dataset and almost similar features collected from PPMI datasets. We have tried to verify how our experiment with multi-modal analysis stands in front of those results to create an overview of model’s ability to classify data in case of missing modalities. Below are the comparison tables for results with Gait datasets and PPMI datasets respectively.

| Authors | Model | Accuracy | Sensitivity | Specificity | AUC | Kappa | 
|-------|:-------:|:--:|:--:|:--:|:--:|:---:|
| Prashantha et al. (2016) [[Link](https://pubmed.ncbi.nlm.nih.gov/27103193/)<sup></sup>] | SVM | 96.40% | 97.03% | 95.01% | 98.88% | NA |
| Leger et al. (2020) [[Link](https://pubmed.ncbi.nlm.nih.gov/32477243/)<sup></sup>] | GAM | 89.80% | 92.30% | 85% | 94.60% | 0.768 |
| Cingireddy et al. (2022) [[Link](https://www.igi-global.com/gateway/article/290011#pnlRecommendationForm)<sup></sup>] | Random Forest | 98% | NA | NA | NA | NA |
| Hema et al. (2023) [[Link](https://www.researchgate.net/publication/370151906_Prediction_analysis_for_Parkinson_disease_using_multiple_feature_selection_classification_methods)<sup></sup>] | Random Forest | 94.50% | 93.40% | 89.20% | 97% | NA |
| Proposed Method | Multi-Modal Network | 99.23% | 98% | 97.36% | 98.95% | 0.9613 |

From above comparison table for PPMI dataset it is evident that this experiment has successfully crossed all the benchmark accuracy of previous research in recent times. Also in terms of AUC score, Cohen Kappa Score, Sensitivity and specificity this architecture performed better than previous studies.

## Comaprison With Previous Gait Experimen

While considering Gait dataset, the below table describes little bit different scenario compared to PPMI result. Recent studies have already got an highest accuracy over 99% and our experiment is almost similar to those results. Not only that, sensitivity, specificity and F1 Score, all these evaluation metrics are also near about similar to recent research studies. So we can say that as all the recent research experiment already achieved near to 100% accuracy that is why our framework does not achieved much more than that result. So there is no scope of improvement as of now for Gait Dataset.

| Authors | Accuracy | Sensitivity | Specificity | F1 Score | 
|-------|:--:|:--:|:--:|:--:|
| Zeng et al. (2016) [[Link](https://pubmed.ncbi.nlm.nih.gov/27693437/)<sup></sup>] | 98.8 | 98.92 | 98.63 | NR |
| Açici et al. (2017) [[Link](https://link.springer.com/chapter/10.1007/978-3-319-65172-9_51)<sup></sup>] | 98 | 99.1 | 95.7 | 0.98 |
| A¸suro˘glu et al. (2018) [[Link](https://linkinghub.elsevier.com/retrieve/pii/S0208521617304321)<sup></sup>] | 99 | 97.8 | 99.5 | NR |
| Zhao et al. (2018) [[Link](https://www.sciencedirect.com/science/article/abs/pii/S0925231218303242)<sup></sup>] | 98.61 | NR | NR | NR |
| Noella et al. (2019) [[Link](https://www.sciencedirect.com/science/article/pii/S1877050920300107)<sup></sup>] | 97 | NR | NR | NR |
| Veeraragavan et al. (2020) [[Link](https://pubmed.ncbi.nlm.nih.gov/33240106/)<sup></sup>] | 97.7 | 97.05 | 97.41 | 0.97 |
| Xia et al. (2020) [[Link](https://pubmed.ncbi.nlm.nih.gov/31603824/)<sup></sup>] | 99.07 | 99.1 | 99.01 | NR |
| Priya et al. (2020) [[Link](https://ieeexplore.ieee.org/abstract/document/9075785)<sup></sup>] | 98.82 | NR  | NR | NR |
| Ghaderyan and Fathi (2021) [[Link](https://www.sciencedirect.com/science/article/pii/S0263224121002591)<sup></sup>] | 97.22 | 98.22 | 95.86 | NR |
| Liu et al. (2021) [[Link](https://link.springer.com/article/10.1007/s10489-020-02182-5)<sup></sup>] | 99.22 | 98.04 | 100 | 0.99 |
| Tong et al. (2021) [[Link](https://www.mdpi.com/2076-3417/11/4/1834)<sup></sup>] | 99.23 | NR | NR | NR |
| Proposed Method | 99.2 | 98.52 | 100 | 0.99 |

## Acknowledgement

I would like to thank my guide [Dr. Deepti R. Bathula](https://www.iitrpr.ac.in/deepti-r-bathula)<sup></sup> (Associate Professor, Indian Institute
of Technology, Ropar) for her continuous support and motivation throughout my project. I
would also like to thank [Mr. Abhishek Singh Sambyal](https://abhisheksambyal.github.io/)<sup></sup> (PhD Student, Computer Science and
Engineering Department, IIT Ropar) for his guidance.

<p align="right">(<a href="#top">back to top</a>)</p>


