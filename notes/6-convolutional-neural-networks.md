*These notes are based on slides by [François Pitié](https://francois.pitie.net/) that can be found [here](https://github.com/frcs/EE4C16/blob/master/handouts/handout-05-deep-feedforward-networks.pdf)*

# Convolutional Neural Networks

[This](https://www.youtube.com/watch?v=FmpDIaiMIeA) is a good explanation of some of the concepts from this topic.

A **Convolutional Layer** is a layer where units are only connected to a few of the nearest neighbours in the input layer.

A **Convolutional Neural Network** (or *convnet*) is a neural network that has convolutional layers.

In a **Dense Layer**, every unit in the layer is connected to every unit in the adjacent layers.

In a **Convolutional Layer**, the units in the next layer are connected to only a few of the nearest neighbours in the previous layer.

There are two ways (at least in Keras) to deal with the fact that at picture boundaries, not all neighbours are defined:  
* **Padding Same** means that values outside of the image domain are set to zero.
* **Padding Valid** means that pixels that have neighbours outside the domain are not computed. This means that the image will be slightly cropped.

In image processing, **Stride** is the distance that separates every processed pixel. A stride of 1 means that all pixels are processed and kept. A stride of 2 means that only every second pixel in the x and y direction are kept.

**Pooling** is a way of subsampling the inputs.

In **Max Pooling**, the maximum of each block is kept.

In **Average Pooling**, the average of each block is kept.

In **Stochastic Pooling**, a random sample of each block is kept.

**A typical convnet architecture for classification:**
* Is based on interleaving convolutional layers with pooling layers.
* Its conv layers usually have a kernel size of 5x5 or 3x3.
* Once the pictures are so small that they no longer look like picture (e.g. 7x7 pixels) they can be connected to fully connected layers and terminate by a last softmax for classification.

|Architecture|History|
|---|---|
|LaNet|Pioneered the use of convolutional layers in NNs in 1998|
|AlexNet|Won the [ImageNet challenge](https://en.wikipedia.org/wiki/ImageNet_Large_Scale_Visual_Recognition_Challenge) in 2012, kickstarting the deep learning revolution.|
|VGG|Popular for object recognition|

Convolutional Neural Netorks offer a very effective simplification over Dense Nets when dealing with images. By interleaving Conv Layers & Pooling Layers, the number of weights and units can be reduces.

