# Seeing in the Dark with Smartphones

## Abstract

Taking photos in low light scenarios with a mobile device such as a smartphone is challenging.
Mainly due to the added noise that comes with high ISO settings and the blur introduced by the above-average exposures necessary.
Several proprietary black-box strategies have been developed and deployed to the flagship smartphones.
We propose an extension of the See-in-the-Dark dataset **cite LSID section 3** with images taken by smartphones.
While we use the same U-net archictecture proposed by **cite LSID section 4**, we propose the use of perceptual similarity metrics as a loss function instead of the traditional pixel-wise MAE loss.

## Background and Related Work

* LSID advantages over traditional pipelines.
* LSID experiments with GAN losses
* MAE loss shortcomings for this task.
* SSIM advantages and disadvantages.
* MS-SSIM 

## Mobile Cameras: See-in-the-Dark dataset

MCSID, pronounced McSeed, is a new dataset we collected inspired by the original SID dataset.
We photographed 600 hundred distinct settings, with as many different sensors as we can get our hands own (as long as they all output a Bayer matrix **footnote explaining**).

### Images

It contains several RAW short exposure images (usually very dark, noisy, and color inaccurate renditions), each paired with a reference RAW long exposure image.
All frames are aligned with each other, as the cameras used were on tripodds.
In order to maximize the usefulness of our dataset, we took photos using several different exposures and, instead of a single taking singles, we took bursts.
That will enable us to better evaluate LSID's strategy against traditional burst-based denoising algorithms.
Furthermore, it will enable us and future researchers to create different approaches to the low-light imaging problem (e.g., composing N images in a single frame).

### Devices

We used a Xiaomi Mi Mix S3, a Redmii ??? and a Cannon DSLR...

* Specs, which sensor they use, supported resolution, ISO, exposures.

### Methodology

We took our photographs in controlled environments.
The devices were kept stable on a tripod.
We created a small Android application to take the photos automatically, so we would not need to touch our devices to set them up in between shots.


## Experiments



## References

[LSID, CVPR](https://arxiv.org/pdf/1805.01934.pdf)

[Loss Functions for Image Restoration with NeuralNetworks, IEEE](https://arxiv.org/pdf/1511.08861.pdf)


[ms-ssim vs pl losses, bubble?](http://www.cs.toronto.edu/~jsnell/assets/perceptual_similarity_metrics_icip_2017.pdf)


[SSIM, IEEE](https://ieeexplore.ieee.org/document/1284395) // over 13k citations
