# TensorFlow.js: Training a variational autoencoder.

This example shows you how to train a [variational autoenconder](https://blog.keras.io/building-autoencoders-in-keras.html) using TensorFlow.js on Node.

The model will be trained on the [Fashion MNIST](https://github.com/zalandoresearch/fashion-mnist) dataset

## Prepare the node environment:
```sh
$ yarn
# Or
$ npm install
```

## Download the data

Download the [train-images-idx3-ubyte.gz](http://fashion-mnist.s3-website.eu-central-1.amazonaws.com/train-images-idx3-ubyte.gz) from [this page](https://github.com/zalandoresearch/fashion-mnist#get-the-data).

Uncompress the file and put the resulting `train-images-idx3-ubyte`. Into a folder called `dataset` within this example folder.

## Run the training script:
```sh
$ node main.js
```

It will display a preview image after every epoch and will save the model at the end of training.

If you are running on a Linux system that is [CUDA compatible](https://www.tensorflow.org/install/install_linux), try using the GPU
package. To do so, replace `require('@tensorflow/tfjs-node')` with `require('@tensorflow/tfjs-node-gpu');` in main.js