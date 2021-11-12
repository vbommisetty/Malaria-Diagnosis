# Malaria-Diagnosis 🦟

### Table of Contents  
 - [Abstract](#abstract) 
 - [Install](#install)
 - [Methods](#methods) 
 - [Results](#results) 
 - [Significance](#significance) 
 - [Report](#report) 

<a name="abstract"/>

## Abstract

__Problem:__

Malaria is caused by single celled microorganisms called Plasmodium. There are many varieties of Plasmodium. In absence of timely diagnosis and care, Malaria can lead to serious complications and even death. On the other hand, early diagnosis can help cure the disease with low-cost medicines.

__Solution:__

The creation of a machine learning model that can takes images as input and outputs whether the red blood cell is infected with malaria or not.

<a name="install"/>

## Install

### Technologies

This project requires Python (v.3.7.12) and the following libraries installed:

 - NumPy
 - Matplotlib
 - Tensorflow
 - Keras

### Data

This project requires the download of tje "Malaria Cell Images Dataset" from the National Library of Medicine. 

```
!wget --no-check-certificate \

  https://ceb.nlm.nih.gov/proj/malaria/cell_images.zip \

  -O /tmp/cell_images.zip
```

This dataset includes around 25 thousand images of healthy and parasitized red blood cells.

![Healthy Cell](https://github.com/hsiFishsiF/Malaria-Diagnosis/blob/main/healthy.png)

_An example of a healthy cell._

![Parasitized Cell](https://github.com/hsiFishsiF/Malaria-Diagnosis/blob/main/parasitzed.png)

_An example of a parasitized cell._

## Methods

<a name="methods"/>

The data was preprocessed before being used to train the model. First, all the images were turned into 150x150 pixel images, then each pixel getting 3 values from 0-1 based on the how much red, green, and blue was in each pixel. The training algorithm would then try to find a pattern within these matricies to attempt to classify the image as either parasitized or healthy.

The batch size and step size were iterated through to find the most accurate model. 100 different models were tested, in which step sizes and batch sizes from 10 - 100 were tested. The epoch size was consistent at 10, as at around epoch 6 the models would start to lose accuracy.

## Results

<a name="results"/>

100 models were tested, and many had an accuracy between 90% and 95%. The model accuracy highlighted in red in the figure below had an accuracy of about 98% at Epoch 6. This model had a batch size of 10 and a step size of 100.

![Graph 1](https://github.com/hsiFishsiF/Malaria-Diagnosis/blob/main/accruacy%201.png)
![Graph 2](https://github.com/hsiFishsiF/Malaria-Diagnosis/blob/main/accuracy%202.png)

The other models had high accuracy, but usually peaked at around 96%-97% accuracy.

## Significance

<a name="significance"/>

This classification model was able to differentiate between parasitized and uninfected red blood cells, reaching an accuracy rate of 98%. There is a high need in many parts of the world for a machine learning model that can identify malaria. This level of accuracy enables diagnosis with minimal training. This is a proof of concept and can be used to detect other bloodborne pathogens that are diagnosed through blood microscopy.

![Malaria Map](https://github.com/hsiFishsiF/Malaria-Diagnosis/blob/main/malaria%20map.png)

## Report

<a name="report"/>

[Malaria Diagnosis Writeup and Report](https://docs.google.com/document/d/1w_sgKUJE5oynSWLSCtDYRpL3e5H3kFba/edit?usp=sharing&ouid=115965752044766156313&rtpof=true&sd=true)
