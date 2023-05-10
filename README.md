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
    <li><a href="#Comaprison With Previous Gait Experiment">Comaprison With Previous Gait Experimen</a></li>
    <li><a href="#acknowledgement">Acknowledgement</a></li>
  </ol>
</details>



## catalog

## Comparison Between Multi-Modality and Baseline Single Modality

| Topic | Gait Model | PPMI Model | Multi-Model |
|---|:---:|:---:|:---:|
| Features | 128 Features | 1595 Features | 1721 Features |
| Parameters | 2214 | 211,852 | 218,676 |
| Loss Function | Sparse Categorical CrossEntropy | Sparse Categorical CrossEntropy | Triplet Loss |
| Optimizer | RMSprop | RMSprop | RMSprop |
| Accuracy | 89.61% | 92.13 | Gait : 98.7, PPMI : 99.11 |
| ROC AUC Score | 85% | 84% | Gait : 0.9782, PPMI : 0.9864 | 
| Cohen Kappa Score | 0.7310 | 0.74 | Gait : 0.9686, PPMI : 0.9613 | 

## Comaprison With Previous PPMI Experiment

## Comaprison With Previous Gait Experimen

## Acknowledgement

I would like to thank my guide [Dr. Deepti R. Bathula](https://www.iitrpr.ac.in/deepti-r-bathula)<sup></sup> (Associate Professor, Indian Institute
of Technology, Ropar) for her continuous support and motivation throughout my project. I
would also like to thank [Mr. Abhishek Singh Sambyal](https://abhisheksambyal.github.io/)<sup></sup> (PhD Student, Computer Science and
Engineering Department, IIT Ropar) for his guidance.

<p align="right">(<a href="#top">back to top</a>)</p>


