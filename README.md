# Dog-Breed-Classifier
## Overview
This project is part of my nano degree in data science for Udacity. It is basically a dog breed classifier responsible of determining whether a given picture is of a human or a dog and then classifying the breed. If the given picture is of a human, the app provides what dog breed the human looks like. In case the given picture was of a dog, it will classify its breed from over a 100 types of breeds.         
This project gives new data scientists a general idea of how real-life machine learning algorithms and products actually work.

## Main Libraries Used
* Numpy         
* Matplotlib          
* Pytorch          

## Datasets
Download the [dog dataset](https://s3-us-west-1.amazonaws.com/udacity-aind/dog-project/dogImages.zip).         
Download the [human dataset](https://s3-us-west-1.amazonaws.com/udacity-aind/dog-project/lfw.zip).         

## Steps to Accomplish this Project
* Step 0: Import Datasets        
* Step 1: Detect Humans          
* Step 2: Detect Dogs          
* Step 3: Create a CNN to Classify Dog Breeds (from Scratch)          
* Step 4: Create a CNN to Classify Dog Breeds (using Transfer Learning)           
* Step 5: Write your Algorithm           
* Step 6: Test Your Algorithm          

## Conclusion
The face and dog detector both are working pretty nicely. However, the problem is with the breed. When the dog breed works quite well, the problem is for the human resemblence. to improve:           
1) hyperparameters tuning.           
2) bigger datasets to improve accuracy.          
3) improve the training of model_transfer to improve breed predictions.
