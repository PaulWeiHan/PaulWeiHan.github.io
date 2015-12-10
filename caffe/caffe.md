---
title: Caffe tutorial
layout: post
---


**声明：创建本文档的目的是出于个人学习。**

**参考：[Caffe 官方文档][CaffeOfficial]**

[CaffeOfficial]: http://caffe.berkeleyvision.org "caffe yangqing jia"

#Installation

[Link to caffe installation doc](http://caffe.berkeleyvision.org/installation.html)

#Training LeNet on MNIST with Caffe

[How to run example: Training LeNet on MNIST with Caffe](http://caffe.berkeleyvision.org/gathered/examples/mnist.html)

The LeNet network for example is a slightly different version from the original LeNet, replacing the sigmoid activations with Rectified Linear Unit (ReLU) activations for the neurons.

The design of LeNet contains the essence of CNNs that are still used in larger models such as the ones in ImageNet. In general, it consists of a convolutional layer followed by a pooling layer, another convolution layer followed by a pooling layer, and then two fully connected layers similar to the conventional multilayer perceptrons. We have defined the layers in $CAFFE\_ROOT/examples/mnist/lenet\_train\_test.prototxt.
