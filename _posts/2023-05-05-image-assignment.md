---
layout: post
title: Assignment 3 Draft- Working with a Corpus of Images 
excerpt: "Image Assignment"
modified: 04/21/2023, 2:40:00
tags: [artificial intelligence, images, image analysis]
comments: true
category: blog
permalink: /image-assignment/
---
**From**: Muhammad Faizan Raza

## Clustering Exercise

### Data Collection
For this step of my assignment, I decided to go with 30 different food pictures from around the world. I selected foods from different cuisines such as Mexican, Indian, Chinese and Thai. However I chose different types of foods such as salads, main courses and desserts so the cuisine is not the only classification they are based on as instructed by the Professor. The data collection process involved me searching up a list of famous traditional foods from the mentioned cuisines and then going to different websites and downloading images of the shortlisted foods.

### Data Processing
After the pictures were downloaded, labelled relevantly and put into the folder, I loaded the folder into orange using the import photos tool. Then I followed the pipeline mentioned in [video 14](https://youtu.be/Iu8g2Twjn9U) of the orange tutorial playlist to pass the images into the data table, then into the image embeddings, then into the distances calculator and then the hierarchical clustering tool. At the end I connected the image viewer to the clustering tool to visualize the images in the clusters together. 

### Analysing Clusters
Before looking at the dendogram, my hypothesis was that since the curry based dishes are usually orange-ish in colour they would be paired together, the salads paired together because of the greens in them and desserts because of the general ingredients and colors they share throughout the globe. I tried all the different types of image embeddings and although the clusters werent very remarkable accross all types, the VGG-19 Image embedding made the most reasonable groups. The dendogram that it generated is given below:
![Clustering Dendogram](/assets/clustering_dendogram.png)
## Classification Exercise
