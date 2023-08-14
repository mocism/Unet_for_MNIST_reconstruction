# Unet_for_MNIST_reconstruction

Don't know why but i try to use [U-net](https://arxiv.org/abs/1505.04597) archetecture to change handwrithing images form MNIST to be the image of that number.

**From this**

![from this](https://imgur.com/VZmm3M3.png)

**To this**

![to this](https://imgur.com/k0YcxSw.png)


## Architecture

Referencing from U-net original paper of u-shape network where it has encoding path, decoding path and skip connection connecting the two side. The model were adjusted to be used with 28X28 2D images. (by keras, tensorflow)

![unet](https://imgur.com/0YKKLWI.png)


## Results

The result indicate the posibilities of using the network to transform handwrithing image into the image of that number. The accuracy is around 0.88 with 5% loss.

But there are some flaws in the MNIST dataset that need to be consider. One main issue is that the image quality is so poor (there are some handwriting that are very bad).

Like in this image, 

![7minst](https://imgur.com/m6BrsQb.png)

it is labeled as 7, but as human, I can't see it as 7 at all. So, the model give,

![7model](https://imgur.com/ybh0iUT.png)

which can read as 5.

Nevertheless, the model still work in most normal cases.


