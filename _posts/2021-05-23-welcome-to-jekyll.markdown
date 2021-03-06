---
layout: post
title:  "Week 1"
date:   2021-05-23 19:37:20 +0530
categories: jekyll update
---

## 24-05-2021

Had a short meet with the professor. We discussed about the project in detail. I was then given 3 videos and the task is to segregate ripe, unripe strawberries and flowers and also find the level of ripeness(unripe, partially ripe, almost ripe, fully ripe) of the strawberries. Before starting with the task I had to research a bit and submit my plan of action. I will start coding from tomorrow.

## 25-05-2021

Started coding!  
Explored different color spaces. HSV was the best. Tuned color ranges for segmentation. As HSV doesnot take into consideration the structural composition of the class, there are a lot of misclassifications. Also, lighting condition affect this algorithm a lot. Got 82% accuracy for flower detection and ~52% accuracy for ripe strawberry detection. So, now as the baseline accuracy is set I can move on to the second method.  

## 26-05-2021

Most of my day went into setting up Darknet and then annotating 86 images. Plan is to train a model partially and then getting predictions and using them to create a new dataset. 

Trained YOLO tiny to check if YOLO is good at classifying flowers, ripe, unripe strawberries. Well, it was working extremely well. 

## 27-05-2021

Tested the trained YOLO tiny weights on different videos. The results were good. 

Made a script to get predictions and these predictions were stored in such a way that the data generated can be used to create a bigger dataset and then trained the model again with bigger and better data for better accuracy. Astonishingly after 6000 epochs the loss of both the models was approximately the same.

Modified the dataset to create a dataset with only 2 classes strawberry and flower. It might be difficult for the model to distingish between ripe and unripe as some strawberries are partially ripe. Also, I had to process the predictions further to get the % of ripeness. So, I thought of clubbing both ripe and unripe strawberry classes. The results were very good. 

Started training the full YOLO model but as time didnot permit on 1000 epochs were done. I will resume training tomorrow from where I left off today.

## 28-05-2021

The training process was too slow so I tried to setup the training on google colab. Initially the speed of trainiing was good but then the session expired. This happend 3 times and each time I had to start from scratch. So, gave up and started training locally. Whole day went into this.

Meanwhile I wrote a report on the basic image processing algorithm and submitted it to the professor.