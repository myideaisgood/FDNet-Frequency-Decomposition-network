Implementation of "FDNet : Frequency Decomposition for Learned Lossless Image Compression"

Hochang Rhee, Yeong Il Jang, Seyun Kim, and Nam Ik Cho

## Environments
- Ubuntu 18.04
- [Tensorflow 1.13.1](http://www.tensorflow.org/)
- CUDA 10.0.130 & cuDNN 7.6.5
- Python 3.7.7

You can type the following command to easily build the environment.
Download 'lcic_duplex.yml' and type the following command.

```
conda env create -f fdnet_env.yml
```

## Abstract


Recent learning-based lossless image compression methods encode an image in the unit of subimages and achieve better or comparable performances to conventional 
non-learning algorithms, along with reasonable inference time. However, these methods do not consider the performance drop in the high-frequency region, giving equal 
consideration to the low and high-frequency regions. In this paper, we propose a new lossless image compression method that proceeds the encoding in a coarse-to-fine manner 
to deal with low and high-frequency regions differently. We first compress the low-frequency components and then use them as additional input for encoding the remaining 
high-frequency region. The low-frequency components act as strong prior in this case, which leads to improved estimation in the high-frequency area. To classify the pixels 
as low or high-frequency regions, we also design a discriminating network that finds adaptive thresholds depending on the color channel, spatial location, and image 
characteristics. The network derives the image-specific optimal ratio of low/high-frequency components as a result. Experiments show that the proposed method achieves 
state-of-the-art performance for benchmark high-resolution datasets, outperforming both conventional learning-based and non-learning approaches.
