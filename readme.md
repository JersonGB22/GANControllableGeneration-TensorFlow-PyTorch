# <h1 align="center">**Controllable Generation using GANs**</h1>

<p align="center">
<img src="https://mmlab.ie.cuhk.edu.hk/projects/CelebA/intro.png" width="700"> 
</p>

This repository presents an implement of controllability for [GANs (Generative Adversarial Networks)](https://papers.nips.cc/paper/5423-generative-adversarial-nets.pdf) utilizing gradients from a classifier. By training a classifier to recognize specific features, we can use it to adjust the inputs of the generator and generate images with more or less of those features.

## Implementations in TensorFlow and PyTorch
Implementations have been carried out in both TensorFlow and PyTorch, the two most widely used frameworks in Deep Learning, to explore the capabilities of controllable generation in GANs. Each implementation provides insights into the differences and similarities between these frameworks, offering practical perspectives for professionals in the field.

- [TensorFlow Notebook](GANControllableGeneration_CelebA_PyTorch.ipynb)

- [PyTorch Notebook](GANControllableGeneration_CelebA_TensorFlow.ipynb)

## Dataset Setup
The ``CelebA`` dataset was employed, consisting of over 200,000 images of celebrities, each with 40 binary facial attribute annotations. The complete dataset is available for download from the [official page](https://mmlab.ie.cuhk.edu.hk/projects/CelebA.html). In case of download inconveniences, loading and data preprocessing details are provided for TensorFlow and PyTorch in their respective notebooks.

## Key Components of Controllable Generation
- A classifier is trained to label each image with one or more of the 40 available attributes, alongside a generator and a discriminator to generate images of human faces. The architectures of these three components are based on DCGAN, a direct extension of GAN that utilizes convolutional and transposed convolutional layers.

- For controllable generation, stochastic gradient ascent is employed. This method, contrary to gradient descent, seeks to maximize rather than minimize. The classifier, along with stochastic gradient ascent, is used to generate noise that allows for adjusting the presence of specific characteristics in the generated images.

## Generated Examples
<p align="center">
<img src="images/celeba/celeba.gif"> 
</p>

*You can observe how face generation improves as epochs progress.*

## Examples of Controllable Generation

<div style="display: flex; justify-content: center;">
    <div style="display: flex; justify-content: space-between; max-width: 800px;">
        <img src="images/labels_celeba/Smiling/Smiling.gif" style="width: 150px;">
        <img src="images/labels_celeba/Eyeglasses/Eyeglasses.gif" style="width: 150px;">
        <img src="images/labels_celeba/Blond_Hair/Blond_Hair.gif" style="width: 150px;">
        <img src="images/labels_celeba/Mustache/Mustache.gif" style="width: 150px;">
    </div>
</div>

<div style="display: flex; justify-content: center;">
    <div style="display: flex; justify-content: space-between; max-width: 800px;">
        <img src="images/labels_celeba/Male/Male.gif" style="width: 150px;">
        <img src="images/labels_celeba/Wearing_Lipstick/Wearing_Lipstick.gif" style="width: 150px;">
        <img src="images/labels_celeba/Bald/Bald.gif" style="width: 150px;">
        <img src="images/labels_celeba/Young/Young.gif" style="width: 150px;">
    </div>
</div>

*With controllable generation, it is possible to add specific features to the generated face by using stochastic gradient ascent on the noise that forms the face. As the steps progress, the desired characteristic is successfully incorporated.*

## Technological Stack
[![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white&labelColor=101010)](https://docs.python.org/3/) 
[![TensorFlow](https://img.shields.io/badge/TensorFlow-FF6F00?style=for-the-badge&logo=tensorflow&logoColor=white&labelColor=101010)](https://www.tensorflow.org/api_docs)
[![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white&labelColor=101010)](https://pytorch.org/docs/stable/index.html)

## Contact
[![Gmail](https://img.shields.io/badge/Gmail-D14836?style=for-the-badge&logo=gmail&logoColor=white&labelColor=101010)](mailto:jerson.gimenesbeltran@gmail.com)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white&labelColor=101010)](https://www.linkedin.com/in/jerson-gimenes-beltran/)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white&labelColor=101010)](https://github.com/JersonGB22/)