# House-grade-Classification-Hackathon

My approach for 2021 Super AI Engineer Deleveopment program. Image Processing hackathon from AI & Robotics Ventures (ARV)

## Task 1 : House-grade-Classification

Predict house grade from image into seperate class by implement various CNN and Transformer architecture.

First let's talk about problem.

The data has imbalance problem and also small training set. Instead of using upsamplig or downsampling method we use various augmentation tecnique such as
* [Automold--Road-Augmentation-Library](https://github.com/UjjwalSaxena/Automold--Road-Augmentation-Library) because we think make image similar to the real situation is a good idea like rain , sunny , fog , speed , night , sun flare etc

Example: (We cannot use dataset image here since we follow NDA rules)
![alt text](https://raw.githubusercontent.com/rsongphon/House-grade-Classification-Hackathon/main/output_27_0.png "Logo Title Text 1")

* [imgaug a library for image augmentation in machine learning experiments](https://imgaug.readthedocs.io/en/latest/index.html)Expand dataset futher by using augmentation sequence like crops and affine transformations to images, flips some of the images horizontally, adds a bit of noise and blur and also changes the contrast as well as brightness

Example

![alt text](https://imgaug.readthedocs.io/en/latest/_images/simple.jpg "ingaug")

After we preprocess the image how do we choose the right architecture for our task?

We have helper! [AutoGluon](https://auto.gluon.ai/stable/index.html) AutoML for Text, Image, and Tabular Data

With AutoGluon we can automate hyperparameter tuning, model selection/ensembling, architecture search utilize state-of-the-art techniques. model we tried such as

* Resnet50
* Efficient
* Visiontrasnformer
* InceptionV3
* Swintransformer
* ConvNet(2020)

The result is ConvNet(2020) archve best accuracy but we did not stop here. We think wecan improve further and we think AutoGluon may overfit the data so we replicate and create this architecture with some modify top-layer to add something like more dense layer,dropout, batch, normalization layer. Get better accuracy!.

Note that in the EDA and data pre-processing process we tried to use GAN (Generative adversarial network) to make more data but we did not make it in time.


This hackathon receive honorable mention prize.
