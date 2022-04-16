# House-grade-Classification-Hackathon

My approach for 2021 Super AI Engineer Deleveopment program. Image Processing hackathon from AI & Robotics Ventures (ARV)

## Task 1 : House-grade-Classification

Predict house grade from image by implement various CNN and Transformer architecture.

First let's talk about problem.

The data has imbalance problem and also small training set. Instead of using upsamplig or downsampling method we use various augmentation tecnique such as
* [Automold--Road-Augmentation-Library](https://github.com/UjjwalSaxena/Automold--Road-Augmentation-Library) because we think make image similar to the real situation is a good idea like rain , sunny , fog , speed , night , sun flare etc

Example: (We cannot use dataset image here since we follow NDA rules)
![alt text](https://raw.githubusercontent.com/rsongphon/House-grade-Classification-Hackathon/main/output_27_0.png "Logo Title Text 1")

* [imgaug a library for image augmentation in machine learning experiments](https://imgaug.readthedocs.io/en/latest/index.html)Expand dataset futher by using augmentation sequence like crops and affine transformations to images, flips some of the images horizontally, adds a bit of noise and blur and also changes the contrast as well as brightness

Example

![alt text](https://imgaug.readthedocs.io/en/latest/_images/simple.jpg "ingaug")




ConvNet architecture and using various pre-
processing techniques to solve imbalance data and small training sample problem by doing

image augmentation and also using AutoGluon to learn about various state of the art deep
learning architecture for image classification from CNN to transformer(Visiontransformer,
Swintransformer) and find best architecture for the task. Receive honorable mention prize.
