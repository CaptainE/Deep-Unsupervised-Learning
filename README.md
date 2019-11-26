# Deep-Unsupervised-Learning
Pytorch implementatiions of the Homeworks in course CS294-158

Here you can find PyTorch implementations of a Masked Autoencoder for Distribution Estimation, PixelCNN, RealNVP and other architectures
that are used in course.

# Homework 1
For the first homework there is a PyTorch implementation of PixelCNN-MADE

That is a auto-regressive model, which mixes ideas from the two papers [Pixel Recurrent Neural Networks](https://arxiv.org/abs/1601.06759) (2016) and [MADE: Masked Autoencoder for Distribution Estimation](https://arxiv.org/abs/1502.03509) (2015) to produce colored 28x28 MNIST digits. Pixel intensities have been quantized to 2 bits (i.e. four intensities for each color channel). The dataset can be downloaded from [here](https://drive.google.com/open?id=1hm077GxmIBP-foHxiPtTxSNy371yowk2).

## Training data

I have used 60,000 quantized 28x28 images from the colored MNIST dataset. Here's a few samples from the training set:

![TrainingSet](https://i.imgur.com/5YqSFBl.png)


## Examples

After 50 epochs of training, a network consisting of 12 residual blocks - see [Deep Residual Learning for Image Recognition](https://arxiv.org/abs/1512.03385) (2015) - followed by a 3-layer MADE generates samples like the following:

![Example](https://i.imgur.com/amfxoUy.png)

You are very welcome to extend the code however you like. If you produce anything cool, be sure to let me know!

# Homework 2
For the second homework we implement RealNVP coupling layers for modelling flows

## Training data

Here I have used 5000 datapoints sampled from this distribution:

![TrainingSet](https://i.imgur.com/stOm8dK.png)

## Example
After 500 epochs we can sample the following face

![Example](https://imgur.com/72Kbd2J.png)

with this fancy latent space

![Latent space face](https://imgur.com/e8pkrcA.png)

and density plot
![density plot](https://imgur.com/2TDhRG4.png)

We also implement RealNVP(https://arxiv.org/abs/1605.08803) to achive these results:

![realnvp](https://imgur.com/jOiG4KP.png)

# Homework 3

We implement a VAE with a gated shortcur connection(https://arxiv.org/pdf/1612.08083) 
and train it on the SVHN dataset.

The final results look like this:
![done_training](https://imgur.com/utnCudE.png)


# Homework 4

In the 4th homework we implement the Wasserstein GAN(https://arxiv.org/abs/1704.00028) and draw inspiration from the architecture used in SN-GAN(https://arxiv.org/abs/1802.05957)


This we for 80 K iteration and the training curves and mean inception score look like the following:
![Training curve](https://imgur.com/HX55Qtl.png)
![Inception_Score](https://imgur.com/XLzzanG.png)

And the resulting samples:

![Samples](https://imgur.com/BApYcle.png)
