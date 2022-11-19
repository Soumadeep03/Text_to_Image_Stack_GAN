# Implementing StackGAN Architecture to generate images from text using Keras
## Overview
StackGAN(Stacked Generative Adversarial Networks) is an extension of GAN(Generative Adversarial Networks) algorithm which uses two stages of GAN algorithm which solves an important problem of creating realistic high resoluton photos. The two stages- Stage-1 GAN sketches the primary colours and shapes based on the text description, and the Stage-2 GAN takes these low resolution images as inputs and turns these images ito realistic high resolutoin images. This model uses the CUB birds dataset for training and testing the model which contains 11,788 texts with 200 categories of birds images. 
## StackGAN architecture
<div>
   <img src="https://github.com/Soumadeep03/Text_to_Image_Stack_GAN/blob/main/architecture_stackGAN.PNG" title="StackGAN" alt="StackGAN" height="300" width="550">
</div>
<br>

* The architecture contains a embedding which is a pre-trained character level embedding turning input text into a fixed vector
* The Conditioning Augmentation(CA) which processes the input text and the this is passed to the, 
* Stage-1 GAN Generator which generates images based on the processed text. The images is sent to the Stage-1 Discriminator. This process continues for several epochs with backpropagation and then the generated low resolution images is passed to the Stage-2 GAN. 
* The Stage-2 GAN generates images from noise and this is passed to the Stage-2 Discriminator which enables
backpropagation, thus after a number of epochs high resolution images are generated from the Stage-2 Generator. 
* After this is fully trained text description can be given as input and will get high resolution images based on the text as output
## 
