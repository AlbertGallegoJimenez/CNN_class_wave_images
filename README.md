# CNN_class_wave_images
This repository is framed in the final project of "Introduction to Data Science and Machine Learning" postgraduate degree by Universitat de Barcelona (2021-2022 course).

## Overview
The main objective of this project is to develop a **Convolutional Neural Network** model that **classifies sea waves images** into different categories according to their energy (by using the significant wave height, Hs, as a proxy of the wave energy).  

This classification problem has been tackled in two ways:
+ As a **multiclass** problem, classifying the waves images into 4 categories: Calm, Low, Moderate and High energy waves.
+ As a **binary** problem, classifying the waves images into 2 categories: Low and High energy waves.

## Contents of the repository
This repository is organised in two folders:  

### <a href=https://github.com/AlbertGallegoJimenez/CNN_class_wave_images/tree/main/data>data folder</a>
#### <ins>wave height data</ins>  
Here, you will find the matrix with the timeseries of the waves in CSV format. This file contains the time, the significant wave height (Hs, in meters), and other wave parameters such as the peak wave period (Tp, in seconds), and the wave direction (Dir, in degrees).  

Due to the fact that the source of the wave Hs database is from numerical modelling (SIMAR dataset from <a href=https://www.puertos.es/es-es/oceanografia/Paginas/portus.aspx>Puertos del Estado</a>), a pre-process of validation and calibration with instrumental data is needed.
In the <a href=https://github.com/AlbertGallegoJimenez/CNN_class_wave_images/tree/main/scripts%20and%20notebooks/data%20pre-processing>data pre-processing</a> folder you can find the MATLAB script and some plots developed for wave calibration.

#### <ins>wave images data</ins>  
Here, you will find the images used to train and test the model. The images have been edited in order to "help" the model for the classification, again, in the <a href=https://github.com/AlbertGallegoJimenez/CNN_class_wave_images/tree/main/scripts%20and%20notebooks/data%20pre-processing>data pre-processing</a> folder you can find the notebook developed.

### <a href=https://github.com/AlbertGallegoJimenez/CNN_class_wave_images/tree/main/scripts%20and%20notebooks>scripts and notebooks folder</a>
Besides the data pre-processing folder explained before, here, you will find the notebooks developed as follows:  
+ 1- Preparing the data for the model.
+ 2- Training the model.
+ 3- Check the results of the model.

These notebooks are developed for both <a href=https://github.com/AlbertGallegoJimenez/CNN_class_wave_images/tree/main/scripts%20and%20notebooks/mutliclass%20approach>multiclass</a> and <a href=https://github.com/AlbertGallegoJimenez/CNN_class_wave_images/tree/main/scripts%20and%20notebooks/binary%20approach>binary</a> approach.







