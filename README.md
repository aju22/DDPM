# Diffusion Models

DDPM was the first paper demonstrating the use of diffusion models for generating high-quality images. The authors proved that a certain parameterization of diffusion models reveals an equivalence with denoising score matching over multiple noise levels during training and with annealed Langevin dynamics during sampling that generates the best quality results.

Access Colab File at: [DDPM.ipynb](https://colab.research.google.com/drive/1n0eqxWuFUupUEv3Seu2MC71DMVeT4t89)

*Diffusion Models are generative models, meaning that they are used to generate data similar to the data on which they are trained. Fundamentally, Diffusion Models work by destroying training data through the successive addition of Gaussian noise, and then learning to recover the data by reversing this noising process. After training, we can use the Diffusion Model to generate data by simply passing randomly sampled noise through the learned denoising process.*

![](https://www.assemblyai.com/blog/content/images/2022/05/image-10.png)

## *Advantages*

Beyond cutting-edge image quality, Diffusion Models come with a host of other benefits, including not requiring adversarial training. The difficulties of adversarial training are well-documented; and, in cases where non-adversarial alternatives exist with comparable performance and training efficiency, it is usually best to utilize them. On the topic of training efficiency, Diffusion Models also have the added benefits of scalability and parallelizability.

## *Forward Diffusion*

A Diffusion Model consists of a forward process (or diffusion process), in which a datum (generally an image) is progressively noised.
![image](https://user-images.githubusercontent.com/72931799/215066392-4b86e623-9410-4888-80eb-3763f2bf1715.png)

## *Reverse Process*

As mentioned previously, the "magic" of diffusion models comes in the reverse process. During training, the model learns to reverse this diffusion process in order to generate new data.

![](https://www.assemblyai.com/blog/content/images/size/w1000/2022/05/image-1.png)

## *Training and Sampling Algorithm*

![](https://www.assemblyai.com/blog/content/images/size/w1000/2022/05/image-20.png)

