---
title: Caffe tutorial
layout: post
---


**声明：创建本文档的目的是出于个人学习。**

**参考：[Caffe 官方文档][CaffeOfficial]**

[CaffeOfficial]: http://caffe.berkeleyvision.org "caffe yangqing jia"

#Installation

[Link to caffe installation doc](http://caffe.berkeleyvision.org/installation.html)

[Caffe + Ubuntu 14.04 64bit + CUDA 6.5 配置说明](caffeinstall_ubuntu14.04.html)

[Caffe + Ubuntu 12.04 64bit + CUDA 6.5 配置说明](caffeinstall_ubuntu12.04.html)

[Our caffe server log file](log.html)

[Our caffe makefile.config file](Makefile.config.html)

#Training LeNet on MNIST with Caffe

[How to run example: Training LeNet on MNIST with Caffe](http://caffe.berkeleyvision.org/gathered/examples/mnist.html)

The LeNet network for example is a slightly different version from the original LeNet, replacing the sigmoid activations with Rectified Linear Unit (ReLU) activations for the neurons.

The design of LeNet contains the essence of CNNs that are still used in larger models such as the ones in ImageNet. In general, it consists of a convolutional layer followed by a pooling layer, another convolution layer followed by a pooling layer, and then two fully connected layers similar to the conventional multilayer perceptrons.

Get the dataset:

    cd $CAFFE_ROOT
    ./data/mnist/get_mnist.sh
    ./examples/mnist/create_mnist.sh

If it complains that wget or gunzip are not installed, you need to install them respectively. After running the script there should be two datasets, mnist\_train\_lmdb, and mnist\_test\_lmdb.

Train the model:

    cd $CAFFE_ROOT
    ./examples/mnist/train_lenet.sh

Some understanding about the example:


    $ cat CAFFE_ROOT/examples/mnist/train_lenet.sh 
    
    #!/usr/bin/env sh

    ./build/tools/caffe train --solver=examples/mnist/lenet_solver.prototxt

Then:
    
    $ cat CAFFE_ROOT/examples/mnist/lenet_solver.prototxt

    # The train/test net protocol buffer definition
    net: "examples/mnist/lenet_train_test.prototxt"
    # test_iter specifies how many forward passes the test should carry out.
    # In the case of MNIST, we have test batch size 100 and 100 test iterations,
    # covering the full 10,000 testing images.
    test_iter: 100
    # Carry out testing every 500 training iterations.
    test_interval: 500
    # The base learning rate, momentum and the weight decay of the network.
    base_lr: 0.01
    momentum: 0.9
    weight_decay: 0.0005
    # The learning rate policy
    lr_policy: "inv"
    gamma: 0.0001
    power: 0.75
    # Display every 100 iterations
    display: 100
    # The maximum number of iterations
    max_iter: 10000
    # snapshot intermediate results
    snapshot: 5000
    snapshot_prefix: "examples/mnist/lenet"
    # solver mode: CPU or GPU
    solver_mode: GPU

From file *lenet_solver.prototxt*, it's easy to see that the network is defined in *lenet_train_test.prototxt*
    
[Explanation, LeNet: the MNIST Classification Model](http://caffe.berkeleyvision.org/gathered/examples/mnist.html)

#RCNN

**需要matlab**

[Code ( Including fast-cnn cnn )][Ross Girshick' s github]

[Ross Girshick' s github]: https://github.com/rbgirshick



