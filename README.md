Name : Devdeep Shetranjiwala  
Email ID : devdeep0702@gmail.com

****

# GSoC Vision Transformers for End-to-End Particle Reconstruction for the CMS Experiment Project - 2023
# ML4Sci

---

## Task 1. Electron/photon classification
Datasets:</br>
https://cernbox.cern.ch/index.php/s/AtBT8y4MiQYFcgc (photons) </br>
https://cernbox.cern.ch/index.php/s/FbXw3V4XNyYB3oA (electrons) </br>
> Description: </br>
32x32 matrices (two channels - hit energy and time) for two classes of particles electrons and photons impinging on a calorimeter
Please use a deep learning method of your choice to achieve the highest possible
classification on this dataset.

> In this task, we will use deep learning to classify two classes of particles: electrons and photons impinging on a calorimeter. We will use two datasets, one for photons and one for electrons, which contains 32x32 matrices (two channels - hit energy and time) for each particle.</br>
We will use deep learning framework PyTorch and Keras/Tensorflow. Our goal is to achieve the highest possible classification accuracy on this dataset with a ROC AUC score of at least 0.80.

> Data Preprocessing : </br>
First, we will load the data and preprocess it.<br>
We will load the datasets for photons and electrons and preprocess them. We will convert the data into numpy arrays and normalize them by dividing each pixel value by the maximum pixel value.

> Pytorch : 
Best ROC AUC score (validate) : 0.8083 </br>
Best ROC AUC score (test) : 0.8004 </br>

> Keras/Tensorflow :
Best ROC AUC score (train) : 0.8703 </br>
Best ROC AUC score (validate) : 0.8093 </br>
Best ROC AUC score (test) : 0.7863 </br>

## Task 2.  Deep Learning-based Quark-Gluon Classification

> Datasets: https://cernbox.cern.ch/index.php/s/hqz8zE7oxyPjvsL 

> Description 125x125 matrices (three channel images) for two classes of particles quarks and gluons impinging on a calorimeter.
For a description of 1st dataset please refer to the link provided for the dataset.

> Please use a Convolutional Neural Network (CNN) architecture of your choice to achieve the highest possible classification on this dataset.
> The framework used in this solution is Tesorflow.

![image](https://user-images.githubusercontent.com/75716586/229305601-16339db9-2e0c-4325-b0ba-dbf27d8f3de4.png)

ROC AUC:
0.731256762325413

## Specific Task : Vision Transformers

Description:
> Train a Transformer model of your choice on the dataset below to achieve the performance closest to your CNN model’s performance in Task 1. </br>
> Discuss the resulting performance of the 2 chosen architectures.

> Datasets (Same as in Task 1): </br>
https://cernbox.cern.ch/index.php/s/AtBT8y4MiQYFcgc (Photons) </br>
https://cernbox.cern.ch/index.php/s/FbXw3V4XNyYB3oA (Electrons)

> I have used Vision Transformer based Model, with Dropout rates as 0. <br>
As the data is sparse, we cannot afford Dropout layers in the Transformer model. <br>
Used softmax as activation for last Dense layer for Electron and Photon Binary Classification. Model Implementation is in Tensorflow.

> PDF link : </br>
https://drive.google.com/drive/folders/1FNFpTBwtfDUgpojhPHhSAEsC4Wx2xMw_?usp=sharing

> Colab link : </br>
Task 1 (Pytorch) : https://colab.research.google.com/drive/1h0PrS4UT3XNnDRXF36BDx7bA5Vt9DGC1?usp=sharing </br>
Task 1 (Tenorflow) : https://colab.research.google.com/drive/1APEvXZl3gSjCRMOkPrZq99Zp2YAK_yv8?usp=sharing </br>
Task 2 : https://colab.research.google.com/drive/1zZ5FgT9YdyesceS46FGrWGmwnE66S9bn?usp=sharing </br>
Task 3 : https://colab.research.google.com/drive/1f6g8cYQEAMn1kqcFxKz7DCslfKv_GS4S?usp=sharing



