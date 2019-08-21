---
layout: post
title:      "(Pre)Training Your Network"
date:       2019-08-21 00:22:25 +0000
permalink:  pre_training_your_network
---


Creating a Neural Network is much like solving a puzzle. When you start, there are an infinite amount of possibilities in direction and vision. As your network progresses, you can focus on obvious choices to improve the model. Each factor implemented can take a toll on efficiency, there’s a real-world toll in the form of time and sheer computational power that limits whats feasible when creating your own network.

It’s at this point I was introduced to Transfer Learning. Transfer learning using a pre-trained model allows you to significantly improve your results while also maintaining the time needed to effectively train your model. A pre-trained model is one that is previously trained on a much larger dataset. The pretrained network can be helpful in two big ways. One is feature extraction. When a model is pretrained, it is trained over a large variety of different images to the point that it can recognize patterns that are generalizable to a greater number of data sets. Adding a new classifier, this model can now be trained on top of the pretrained model. The other way a pretrained model can help is the process of fine-tuning. Because the pretrained model is considered a base layer to a multilayer neural network for your specific dataset, certain layers can be frozen and unfrozen to be modified. This allows the last layers to be “fine-tuned” to make them more relevant for the task at hand.

A final note to be made is the different networks shipped with the library Keras. These networks, which are previously pretrained off the ImageNet dataset, a collection of 1.4 million images and 1,000 classes, are integral in the network creation puzzle. These networks include VGG19, ResNet50, Xception, and more. Each network has their pros and cons which can benefit you in different ways. For example, VGG19 was considered simple to train but can be slow and demanding on storage in terms of weights. ResNet50 can reduce the storage required for the model significantly. All these factors change the efficiency of your model. 

Each decision made when it comes to perfecting your neural network needs to be trained and tested, iterated and reiterated on. And using transfer learning techniques can be a powerful tool in creating your perfect model. By having a well trained CNN able to generalize visual patterns, you extract new value when applying these patterns to different domains

