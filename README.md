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

![Healthy Cell](https://imgur.com/soadlCj)

![Parasitized Cell](https://imgur.com/VKrSApD)

## Methods

<a name="methods"/>

The data was preprocessed before being used to train the model. First, all the images were turned into 150x150 pixel images, then each pixel getting 3 values from 0-1 based on the how much red, green, and blue was in each pixel.


## Results

<a name="results"/>

## Significance

<a name="significance"/>

## Report

<a name="report"/>

[Malaria Diagnosis Writeup and Report](https://docs.google.com/document/d/1w_sgKUJE5oynSWLSCtDYRpL3e5H3kFba/edit?usp=sharing&ouid=115965752044766156313&rtpof=true&sd=true)
