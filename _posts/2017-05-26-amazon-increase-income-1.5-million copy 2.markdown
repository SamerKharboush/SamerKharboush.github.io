---
layout: post
title:  CAD prediction using CMRI DL on a Web App
date:   2022-05-26 15:05:55 +0300
image:  /assets/images/blog/cad.jpg
author: Samer
tags:   DL
---

What is coronary artery disease? Coronary artery disease (CAD) is the most common type of heart disease in the United States. It is sometimes called coronary heart disease or ischemic heart disease.

For some people, the first sign of CAD is a heart attack. You and your health care team may be able to help reduce your risk for CAD. What causes coronary artery disease? CAD is caused by plaque buildup in the walls of the arteries that supply blood to the heart (called coronary arteries) and other parts of the body.

Plaque is made up of deposits of cholesterol and other substances in the artery. Plaque buildup causes the inside of the arteries to narrow over time, which can partially or totally block the blood flow. This process is called atherosclerosis. Coronary artery disease (CAD) is known as a common cardiovascular disease. A standard clinical tool for diagnosing CAD is angiography.

The main challenges are dangerous side effects and high angiography costs. Today, the development of artificial intelligence-based methods is a valuable achievement for diagnosing disease., so I tried different Machine Learning methods such as (CNN),Pytorch, Tensorflow and Pre-trained model ResNet18 to detect CAD patient MRI also Autoencoder which will try to understand the underlying distribution of Data, and try to create CAD images using Models.

Custom Data Generator A lot of effort in solving any machine learning problem goes into preparing the data. PyTorch provides many tools to make data loading easy and preprocess/augment data from a non-trivial dataset. torch.utils.data.Dataset is an abstract class representing a dataset. Your custom dataset should inherit Dataset and override the following methods: len so that len(dataset) returns the size of the dataset. getitem to support the indexing such that dataset can be used to get ith sample. Learn More: Pytorch Data Loading Documentation Custom Neural Network Class This class will inherit the properties from torch.nn.Module and should have two functions init for defining neural network and forward for forward propogation. In General, forward function, will be dealing with output from each layer. I can apply MaxPool, Dropouts and other activation functions.

Convolutional Neural Network - Classification.

> Autoencoder notebook
Autoencoder is a type neural network where the output layer has the same dimensionality as the input layer. In simpler words, the number of output units in the output layer is equal to the number of input units in the input layer. An autoencoder replicates the data from the input to the output in an unsupervised manner and is therefore sometimes referred to as a replicator neural network. Architecture of autoencoders An autoencoder consists of three components: • Encoder: An encoder is a feedforward, fully connected neural network that compresses the input into a latent space representation and encodes the input image as a compressed representation in a reduced dimension. The compressed image is the distorted version of the original image. • Code: This part of the network contains the reduced representation of the input that is fed into the decoder. • Decoder: Decoder is also a feedforward network like the encoder and has a similar structure to the encoder. This network is responsible for reconstructing the input back to the original dimensions from the code.

an Autoencoder Implementation, which will try to understand the underlying distribution of Data, and try to create CAD images using Models, (noise denoise) concept Dataloading and preparation, then build a linear (NN), loss MSELoss and Adam optimizer, Show the result of the autoencoder using clear_output from IPython.display.

More can be accessed here: https://github.com/SamerKharboush/CAD