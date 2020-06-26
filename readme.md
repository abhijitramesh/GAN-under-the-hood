# Generative Adversarial Networks


# Applications of GANs

---

## StackGan Model

This model takes in a description of a bird and generates a high-resolution image of a bird matching that description. These are images that have not been seen before which means the gan is not searching for an image in a set of images but generates a new image.

## IGAN

These Gan helps artist when a doodle is drawn using a mouse these GANs translate them to images

## Pix2Pix

The GANs take input of an image in one domain and convert them to images in other domains for examples blueprints of building can be changed to images of buildings or drawings of cat can be turned into images of cats.

## Cartoon GANs

These GANs generate cartoon face given a normal face, these GANs were trained on faces of people and cartoon faces but they were not told what image is mapped to what.

## Cycle GANS

These GANs also uses unsupervised learning they can do things like take in a video of a horse and convert it to a video of a zebra , since they are using unsupervised learning they not only convert the horse object but also some parts of the background since they are using unsupervised learning.

## Simulated Training

GANs can take in input of 3d or 2d models and create realistic datasets which can be used as training dataset for image recognition tools.

# How GAN's Work

As we know RNNs can be used for generating text data word by word at a time similarly image can also be generate by fully visible belief networks (what it was called in the 90's) by generating pixel by pixel at a time these are called Autoregressive models (renamed when they were rediscovered later). 

But if we need to generate an entire image as output we use GANs, They consist of two different neural networks called as generators and discriminator.

## Generator

---

The generator is a neural network which takes in a random noise and runs it to a neural network to generate an image this image is *realistic.* The choice of the random noice determine how *realistic* the image is. The generator learns to create these data looking at the data provided.

Unlike a supervised learning model Generative models doesn't have labels to tell what to learn from but they are asked to make more images that come from the same probability distribution.

How do we do this ?

Most generative models do this by adjusting the parameters of the generator but this is difficult to compute this. Most models do this by using some kind of approximations GANs uses some kind of approximations called as Discriminator.

## Discriminator

---

The discriminator is a normal classifier neural net which predicts if the image generated by the generator is real or fake, if it is real the generator will give a value close to one if not otherwise.

Overtime generator tries to make images which have probability close to one and discriminator gets better and better at determining which images are not real.
