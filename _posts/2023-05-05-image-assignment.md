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
Before looking at the dendogram, my hypothesis was that since the curry based dishes are usually orange-ish in colour they would be paired together, the salads paired together because of the greens in them and desserts because of the general ingredients and colors they share throughout the globe. I was also interested to see if it could detect certain ingredients in the dishes and pair them according to the cuisines. I tried all the different types of image embeddings and although the clusters werent very remarkable accross all types, the VGG-19 Image embedding made the most reasonable groups. The dendogram that it generated is given below:
![Clustering Dendogram](/assets/clustering_dendogram.png)

Analyzing the cluster of first three food items, we can see 

## Classification Exercise

### Data Collection
For this step of the assignment, I aimed to collect a datatset of 100 images from different instagram nature photographers. I tried using internet tools to download instagram photos from photographers but soon realized that doing one by one image would take very long so I decided to write a python script for it. The script is available in the nature photographers folder in the assets folder. I came accross this website called instaloader and incorporated that in my script. The I shortlisted some photographers and downloaded photos from their top 10 most liked posts and saved into folders. A problem I came across was that it downloaded a lot of photos for posts with multiple photos and for some photographers, their most liked post was a video. So after examining the folders I decided to download top 15 most liked posts of some photographers and then filtered out 10 distinct photos that I liked. The script also downloaded metadata for the photos which I deleted for the purpose of this project but it is something that could be used if somebody wants to incorporate text analysis into this project.

## Data Processing
For this step, I just took the orange file template professor provided in his drive including the image grid, confusion matrix, logistic regression and more. Then I just used the import files feature to upload the folders together and rest of the processing happened itself.

## Data Analysis
My initial hypothesis was that since a lot of photographers used a lot of very distinct presets and colors they will be paired together in the classes however some of the photographers took photos of similar animals or landscapes so I thought that could lead to a picture of one photgrapaher linked to another photographer. Following is the confusion matrix of the images

![Confusion Matrix](/assets/confusion_matrix.png)

The testing statistics of the classification are given as follows:
- **AUC**: 0.932
- **CA**: 0.640
- **F1**: 0.622
- **Precision**: 0.611
- **Recall**: 0.640

Although the high AUC shows the ability of the classifier to distinguish between classes well, the Accuracy at 0.640 shows that the model was not able to put the images into their relevant classes as successfully as was expected because of the overlapping themes amongst the photographers

Lets look at first the david lloyd images whose pictures are all predicted correctly.
![David Lloyd](/assets/david.png)

Examining the pictures we can see that most of the pictures are of animals that have similar aesthetics or live in similar regions hence the similar background. All the photos seem to be have underwent similar colour grading and hence the program is probably detecting those

Another photographer for which the program detected the pictures correctly was Nick Brandt:
![Nick Brandt](/assets/nick.png)

Here the difference that sets out these set of images is very clear and its the grayscale images that the program detected very easily.


![Paul Nicklen](/assets/paul.png)
One interesting case to look at is of the photos of the photographer Paul Nicklen whose no actual photos were predicted as his own and were evenly divided amongst the other photographers. As we can see 






