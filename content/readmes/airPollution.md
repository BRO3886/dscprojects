---
title: airPollution
date: 2020-12-12T08:27:15+0000
draft: false
---
# Pollution Control by Identifying Potential Land for Afforestation 

The program aims at controlling the pollution in a given area by suggesting the number of trees and the areas where they should be planted. The heart of the program is Computer Vision. It can be divided into two phases:

## 1. Getting the suitable Satellite images for the given region.

The user is required to input the name of the area, on which the program has to be executed.The satellite images of that area will be scraped and are zoomed such as to generate a clear image of map on which image segmentation can be done.

## 2. Identifying the empty spaces for tree plantation

This process uses Computer vision to find the areas fit for plantation i.e. areas which are rid of any buildings,water bodies,trees,roads etc. It mainly consists of 3 parts:

### i) Segmentation of the Satellite image: 
The satellite image generated by the 1st step undergoes Image segmentation ,which separates all the objects in the image by focussing on edges and boundaries.The image is divided into objects such as the buildings, trees ,water bodies,roads ,barren land etc . Our first algorithm of choice is Mean Shift Algorithm for segmentation. 

![Image segemntation](https://s22.postimg.cc/6a67amyhd/IMG_20180326_003903_0.jpg)

### ii) Finding features for objects using Zernike Moments:
Zernike moments are powerful region-based shape descriptors that are invariant against linear transformations and especially against object boundary deformation. For each of the segments generated by Segmentation algorithm , Zernike moments are calculated and stored.

### iii)Classification :
In this process , we need to train a Classifier which can identify the buildings, the trees and most importantly, the free land. The Zernike moments used by the above method will be used as features for these segments. The classifier is trained with labels as 'buildings','trees','water','free land' and 'roads'. After the training , We only need to find the part coming under 'Free Land' label. 


## 3. Finding the Number of Trees to be planted:

We will be finding the pollution level of the given area . According to that level, we will find the number of trees required to bring that particular level to normal. 


