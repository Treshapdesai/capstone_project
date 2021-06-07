# capstone_project

## Problem Statement

Colorectal Cancer is one of the leading causes of cancer in the US. Preventive measures such as regular scopes and taking biopsies can detect abnormalities at an earlier stage. However, this increases the workload for pathologists. The upside is that there is an increasing amount of image and clinical text data that can be tapped into to create a platform (Interactive Website) that uses the database to generate predictions that serve as supportive tools to the pathologists. Not only pathologists, but researchers and training doctors can leverage on such platforms for research and education/learning purposes. 


## Project Structure
1) EDA --> Exploratory Data Analysis Notebook
2) RF Model --> Random Forest Model for Pixel Image Classification
3) KNN Model --> K Nearest Neighbour Model for Pixel Image Classification
4) CNN Model --> Convulated Neural Networks for Pixel Image Classification
5) SVC Model --> Support Vector Machines for Pixel Image Classification
6) Tumour VS Stroma --> Various Models to compare Tumour and Stroma Pixel Image Data
7) CNN image data --> Using CNN Model for Raw Image Classification between Tumour and Stroma
8) Clinical Text Data --> Natural Language Processing using various models and Executive Summary

## Models and Results

**Summary table for Colorectal Cancer Classification models for 8 Tissue type classes:**

| Model| Test Accuracy|Baseline score|
|:---------:|:---:|:--------:|
|  Random Forests |    0.684 |  0.125  |
|KNN| 0.432| 0.125|
|CNN|  0.603 |0.125|
|SVM| 0.637|0.125|

**Summary table for Colorectal Cancer Classification models for 2 Tissue type classes:**

| Model| Test Accuracy|Baseline score|
|:---------:|:---:|:--------:|
|  Random Forests |    0.947 |  0.5  |
|SVC|  0.925 |0.5|
|CNN| 0.960| 0.5|

**Summary table for Classification of Clinical Text data into 9 classes of mutation types:**

| Model| Test Accuracy|F1 score|Baseline score for largest class|
|:---------:|:---:|:--------:|:--------:|
|  Naiive Bayes |    0.594 | 0.580   |  0.379  |
|KNN|  0.524| 0.508   |0.379 |
|SVC| 0.616|  0.571 | 0.379 |
|Random Forests|0.584| 0.555   |0.379 |
|Logistic Regression|0.541| 0.515    |0.379 |

## Executive Summary

Using pixel values image data to classify into 8 tissue types showed that the results are generally poor, with the highest accuracy score of only 0.684 using Random Forests. In addition, it is crucial to classify 2 tissue types (Tumour and Stroma) as compared to all 8 classes. Tumour and Stroma images can be easily misclassified. Also, the tumour:stroma ratio sheds insights on overall survival. A paper showed that stroma-rich tissues had poorer disease-free and overall survival rate. This is because stroma (connective tissues) eventually promote growth, invasion and metastasis. 

Classifying Tumour VS Stroma pixel values data had a good score of 0.96 using CNN model. This model serve as a supporting tool for doctors to make more accurate diagnosis. However, in reality, the images are a mixture of Tumour and Stroma (instead of seperate images). Therefore, an interactive software can be designed which allows pathologists to input an image. They can annotate (draw a line) across the area of interest. The software will convert the image to pixel values and provide an output of which tissue type the area of interest belongs to. 

There are advantages to using pixel values as data as compared to raw images. Firstly, the CNN model performs better (seen in the table below), in addition, pixel values take up lesser storage space then raw images. 
 
 | Pixel Values| Raw Image|
|:---------:|:---:|
|  0.96 accuracy score with CNN |    0.71 score using CNN |
|Lesser memory space since numbers|More memory space with images stored|
 |More data can be added for various types of cancers |Lesser data results in limited use of website created for classification|


