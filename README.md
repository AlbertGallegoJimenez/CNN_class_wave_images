# CNN_class_wave_images
This repository is framed in the final project of "Introduction to Data Science and Machine Learning" postgraduate degree by Universitat de Barcelona (2021-2022 course).

## Overview
The main objective of this project is to develop a **Convolutional Neural Network** model that **classifies sea waves images** into different categories according to their energy (by using the significant wave height, Hs, as a proxy of the wave energy).  

This classification problem has been tackled in two ways:
+ As a **multiclass** problem, classifying the wave images into 4 categories: Calm, Low, Moderate and High energy waves.
+ As a **binary** problem, classifying the wave images into 2 categories: Low and High energy waves.

## Contents of the repository
This repository is organised in two folders:  

### <a href=https://github.com/AlbertGallegoJimenez/CNN_class_wave_images/tree/main/data>data folder</a>
It is important to note that the two datasets in this folder are already pre-processed. The data found here can already be used directly for the developed model.
#### <ins>wave height data</ins>  
Here, you will find the matrix with the timeseries of the waves in CSV format. This file contains the time, the significant wave height (Hs, in meters), and other wave parameters such as the peak wave period (Tp, in seconds), and the wave direction (Dir, in degrees).  

Due to the fact that the source of the wave Hs database is from numerical modelling (SIMAR dataset from <a href=https://www.puertos.es/es-es/oceanografia/Paginas/portus.aspx>Puertos del Estado</a>), a pre-process of validation and calibration with instrumental data were needed.
In the <a href=https://github.com/AlbertGallegoJimenez/CNN_class_wave_images/tree/main/scripts%20and%20notebooks/data%20pre-processing>data pre-processing</a> folder you can find the MATLAB script and some plots developed for wave calibration.

#### <ins>wave images data</ins>  
Here, you will find the images used to train and test the model. The images have been edited in order to "help" the model for the classification, again, in the <a href=https://github.com/AlbertGallegoJimenez/CNN_class_wave_images/tree/main/scripts%20and%20notebooks/data%20pre-processing>data pre-processing</a> folder you can find the notebook developed.  

The source of the original images is from the <a href=https://coo.icm.csic.es/service/video-monitoring>Video Monitoring System of Castelldefels beach</a> managed by Coastal Morphodynamics (UPC) and Coastal Ocean Observatory (ICM-CSIC).

### <a href=https://github.com/AlbertGallegoJimenez/CNN_class_wave_images/tree/main/scripts%20and%20notebooks>scripts and notebooks folder</a>
Besides the data pre-processing folder mentioned before, here, you will find the notebooks developed as follows:  
+ 1- Preparing the data for the model.
+ 2- Training the model.
+ 3- Check the results of the model.

These notebooks are developed for both <a href=https://github.com/AlbertGallegoJimenez/CNN_class_wave_images/tree/main/scripts%20and%20notebooks/mutliclass%20approach>multiclass</a> and <a href=https://github.com/AlbertGallegoJimenez/CNN_class_wave_images/tree/main/scripts%20and%20notebooks/binary%20approach>binary</a> approach.

## Results
The following confusion matrices show the results obtained from the **test set** for both multiclass and binary approach.

| **Multiclass Approach** | **Binary Approach** |
| :---: | :---: |
| ![cf_m_multiclass!](https://github.com/AlbertGallegoJimenez/CNN_class_wave_images/blob/main/scripts%20and%20notebooks/mutliclass%20approach/test_accuracy_multiclass_approach.PNG) | ![cf_m_binary!](https://github.com/AlbertGallegoJimenez/CNN_class_wave_images/blob/main/scripts%20and%20notebooks/binary%20approach/test_accuracy_binary_approach.PNG) |
| Test accuracy = 0.627  | Test accuracy = 0.863  |

