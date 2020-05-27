# Dog-Breed-Classifier
## Overview
This project is part of my nano degree in data science for Udacity. It is basically a dog breed classifier responsible of determining whether a given picture is of a human or a dog and then classifying the breed. If the given picture is of a human, the app provides what dog breed the human looks like. In case the given picture was of a dog, it will classify its breed from over a 100 types of breeds.         
This project gives new data scientists a general idea of how real-life machine learning algorithms and products actually work.

## Main Libraries Used
* Numpy         
* Matplotlib          
* Pytorch          
* Torchvision             
* PIL           

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

## Introduction
The two datasets contain 8351 dog images (6680 used for training and the rest for testing) and 13233 images for humans.
Coloured images are turned to grayscale for easier and faster processing. The identification of human faces was 98% accurate in the humans dataset, whereas the face detector accuracy for dogs was 17%, which indicates that there is an issue. Hence, I have used VGG-16 Model, a pre-trained model to detect dogs in images. For the classification process, two CNNs were used to classify dog breeds, one made completely from scratch while the other using transfer learning.         

## Description
1. For the CNN made from scratch, the first layer will have 3 inputs for RGB because the in_channel is 3 and produces 16 output. Then the next layer will have a convolutional layer with 16 filters. Input = 224x224 RGB image Kernel Size = 3x3 Padding = 1 for 3x3 kernel MaxPooling = 2x2 with stride of 2 pixels, which will reduce the size of image and by the result the number of parameters will be half. Batch Normalization 2D is used to generate inputs which are zero mean. Activation Function is ReLu to prevent vanishing gradient. Dropout has a probability of 0.2. It’s a fully connected layer with 9216 inputs and 133 outputs as dog breeds. This model produced a test accuracy of 22% which is higher than the recommended 10%.  

2. For the CNN made using transfer learning, ResNet has been selected as the model of choice due to the fact that it has a feature aka identity shortcut connection, which skips some layers to prevent overfitting. The model also has 133 outputs as desired. The test accuracy of this model was 67% which is higher than the recommended 60%.        

3. Finally, I wrote an algorithm that accepts a file path to an image and first determines whether the image contains a human, dog, or neither.

## Conclusion
The face and dog detector both are working pretty nicely. However, the problem is with the breed. When the dog breed works quite well, the problem is for the human resemblence. to improve:           
1) hyperparameters tuning.           
2) bigger datasets to improve accuracy.          
3) improve the training of model_transfer to improve breed predictions.
