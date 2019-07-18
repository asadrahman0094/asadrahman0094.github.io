---
layout: post
title:      "Build Your Own Network"
date:       2019-07-18 23:40:43 +0000
permalink:  build_your_own_network
---


For my module 4 project, I was faced with the dilemma of creating a pattern recognizing network that could take in chest xray and distinguish a healthy body from that infected with pneumonia. Pattern recognition, especially for images, is the forte of convolution neural networks. As opposed to the vectorization that occurs in a regular keras model, introducing convolution layers that recognize both local and global patterns throughout each layer of the network greatly increases the effectiveness of our model. But how do we know we’ve created the best model?

![](https://miro.medium.com/max/1200/1*DW0Ccmj1hZ0OvSXi7Kz5MQ.jpeg)

Our first model is a baseline line framework of our final product, a neural network using dense layers which will vectorize the patterns in our xrays and feed the information through our model. This first iteration is able to give us a rough understanding of how effective our model is with no modification. Moving forward, we can increase or decrease the number of layers and epochs. A single epoch is a complete pass through the dataset that is run through our model.
Each iteration of our model will effect the results differently, small changes can result in exponential increase in accuracy and loss. This measure of information change is recorded in both training and validation loss. Our accuracy is simply that, how accurately can our model fit the training data and the validation data. Considering training data are the images the model actually trained off of, we expect this number to raise constantly through each increased iteration of our model regardless of ow many times that is. Our validation accuracy though levels out, limiting the number of effective epochs to render an output to a reasonable amount of time. But even if our data is able to achieve 99% accuracy, there is always the chance that this instance of the model is catering specifically to the dataset fed at that moment. This is known as overfitting. A good gauge of this is if your training loss is much lower or not similar to your validation loss. Making sure you don’t overfit your model helps generalize the use of the model beyond the data it is fed.

The last step for perfecting your model is optimizing it. By introducing weight regularization (L1 and L2), you add a cost associated with having larger weights. Another way to optimize your model is introducing dropout layers. A dropout rate is a fraction of features that randomly zero out, increasing the variability of the model during training. Dropout layers are very effective in combating overfitting. Through tweaks and iterations, increasing training data, altering network capacity, and employing different optimization techniques – a neural network is a powerful patter recognizing tool that can process information quickly and effectively.

