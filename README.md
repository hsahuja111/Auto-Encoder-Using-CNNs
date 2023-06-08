# Auto-Encoder-Using-MLP-CNN-and-KNN-On-Encoded-Image

This repository consists of a Jupyter notebook named Auto-Encoder.ipynb in which we have built Auto-Encoder using different models and played with
it by tweaking model structues

## What is AUTO ENCODER ??
An autoencoder is a type of artificial neural network that is commonly used for unsupervised learning and dimensionality reduction. 
It is composed of an encoder network and a decoder network, which work together to learn a compressed representation of input data.

The purpose of an autoencoder is to learn a lower-dimensional representation, or encoding, of the input data in such a way that the decoder can reconstruct the original input as closely as possible.
The encoder network maps the input data into a lower-dimensional latent space, and the decoder network attempts to reconstruct the original data from the latent representation.

### Dataset Used
We have used CIFAR-10 dataset which consists of 60000 32x32 colour images in 10 classes, with 6000 images per class. There are 50000 training images and 10000 test images

## CORE IDEA
![image](https://github.com/hsahuja111/Auto-Encoder-Using-MLP-CNN-and-KNN-On-Encoded-Image/assets/43888676/c33f813c-7774-47f4-88e4-d6984c398524)

Firsly we are encoding the image to get a encoded version of the image which has much reduced size. 
Now comes the Decoder which uses this encoded image generates the image of original size and tries to get the best quality.



## TASKS PERFORMED

### Part - 1

1. Training 3 different types of models for Auto Encoder
  *  MLP-only model --> MLPAutoEncoder()
  *  CNN-MLP combination model --> ComboAutoEncoder()
  *  CNN-only model -->  CNNAutoEncoder()

In all the models, encoder and decoder should be consisting of  3  layers each, and the encoder should be giving a flattened representation of size  32 .

I have tabulated Model Size , Model Parameters , Time Taken per epoch for each of these models 

2. Playing with the following representation sizes of the image
  * 10 --> CNNAutoEncoder10()
  * 32 --> CNNAutoEncoder32()
  * 100 --> CNNAutoEncoder100()
  * 1000 --> CNNAutoEncoder1000()

These are the size of the encoded images that is further used to decode the image and this size is flattened representation.

3. Playing with following layers of encoder and decoder each
  * 1 --> CNNAutoEncoderL1()
  * 3 --> CNNAutoEncoderL3()
  * 5 --> CNNAutoEncoderL5()
  * 10 --> CNNAutoEncoderL10()
  
### Part - 2

In this section , we have used KNN on the encoded image. Here, we have model which has representation size of 10 and then extracted the encoded images from the trained model
Now we have applied KNN on these encoded image which will reduce the computation cost when compared to images of large size.


## Comments for each step have been added in the jupyter notebook which will help to understand better.
 



