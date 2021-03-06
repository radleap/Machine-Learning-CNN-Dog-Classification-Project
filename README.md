﻿[//]: # (Image References)


[image2]: ./images/Results.JPG "Notebook Sample Output"
[image1]: ./images/readme_phone_image.jpg "App Sample Output"


## Project: Dog Vision Convolutional Neural Network Prediction Application

In this project, we build a pipeline that can be used within a web or mobile app to process real-world, user-supplied images. Given an image of a dog, this algorithm will identify an estimate of the canine’s breed. If supplied an image of a human, the code will identify the resembling dog breed.

The aim was to accurately detect a dog in an image and predict the breed of that dog, based on 133 classes. This is accomplished in three parts – separate algorithms that determine whether (1) a dog is in an image (2) or a human is in an image and (3) what dog breed is predicted for the image.  

Though many models were trained, this MobileNetV2 transfer-learning model was chosen due to performance (82% accuracy) , resource availability (time) and operational ability (less than 10MB).

![Sample Output][image2]

## General Project Details

## Proposal and Final Project Paper
The project includes the Capstone Proposal and Project Final Paper in the GitHub directory.

## General Deployment Details

See https://github.com/radleap/Application-Heroku-Dog-Class-Prediction

The application makes use of Heroku, an open source PaaS, with a Bootstrap framework. The CSS and HTML was customized for simplicity, but maintain the connectivity between the various components. This is our scaffolding, with all documents maintained on Github.

Computer vision has been implemented in order to detect if a human face was in the image, via the opencv python package. On the other hand to detect dogs, a pre-trained neural network (SqueezNet) was loaded to predict if in the image. Both maintained ~95% accuracy or better with test images.

In order to make the overall dog class prediction, a deep learning model was used that took two days to train on CPU. Though many models were trained, this iteration was chosen due to performance, resource availability and operationalability (not too big)! In particular, a convolutional neural network based on the MobileNetV2 algoritm was used, fine tuned for the last layers to select from 133 dog breeds/classes. The model was trained using the pytorch framework.

The selected MobileNetV2 trained model maintained an accuracy of 82% on unseen test data. To put this success into perspective, random chance would correctly select the dog breed less than 1% of attempts. This is pretty good!

## Build Status: 
   Deployed at this link https://whos-a-good-boy.herokuapp.com/

![Sample Output][image1]

## Requirements
See the requirements.txt file for necessary packages. 

## Data
See directories "dogImages", "haarcascades", and "images" for supporting data.

## Outputs
Apart from the "model_scratch" and "model_transfer", all models are saved in the "models" direcetory.

## Motivation
   CNN for dog detection, build something fun, and practice new learnings.

## License
### The MIT License (MIT)
### Copyright (c) 2020 Ben Jacobson
```
Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:
The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.
THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
```