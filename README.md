WebGPU Image Super Resolution
======================

**University of Pennsylvania, CIS 565: GPU Programming and Architecture, Final Proejct**

* Paul (San) Jewell
  * [LinkedIn](https://www.linkedin.com/in/paul-jewell-2aba7379), [work website](
    https://www.biociphers.org/paul-jewell-lab-member), [personal website](https://gitlab.com/inklabapp), [twitter](https://twitter.com/inklabapp), etc.
* Tested on: Linux pop-os 5.11.0-7614-generic, i7-9750H CPU @ 2.60GHz 32GB, GeForce GTX 1650 Mobile / Max-Q 4GB

* Yuxuan Zhu
  * [LinkedIn](https://www.linkedin.com/in/andrewyxzhu/)
* Tested on: Windows 10, i7-7700HQ @ 2.80GHz 16GB, GTX 1050 4096MB (Personal Laptop)

## Live Online

[![](img/Demo.gif)](https://sona1111.github.io/webgpu-super-resolution/)

## Introduction

We created a WebGPU based image super resolution program. Under the hood, it runs a neural netork based on [ESRGAN](https://github.com/xinntao/ESRGAN). The input to the program is any RGB image. The output of the program is the same image with 4x the resolution. The program runs in Chrome Canary with the flag `--enable-unsafe-webgpu`. All the computation is done on the client side, so the images uploaded by clients will remain on the client side. No privacy concerns! We currently support up-sizing images of medium size. For example, a typical GPU with 4GB RAM can upsize image of size 400px by 400px. The size limit and run time varies depending on different client hardwares.

## Usage Instruction
1. Download and install Chrome Canary/Chrome Dev/Firefox Nightly
2. Go to chrome://flags/#enable-unsafe-webgpu to enable WebGPU
3. Visit https://sona1111.github.io/webgpu-super-resolution/
4. Voilà, now you can increase the resolution of any image that you upload!

## Performance Analysis

![](benchmark/runtime.png)
![](benchmark/ramuse.png)
![](benchmark/numpx.png)

## Roadmap
- Support for larger images
- Further improve runtime

## Credits

* [WebGPU Compute](https://web.dev/gpu-compute/) 
* [WebGPU Samples](https://github.com/austinEng/webgpu-samples)
* [ESRGAN](https://arxiv.org/abs/1809.00219)
* [ESRGAN Weights](https://github.com/xinntao/ESRGAN)
* [More ESRGAN Weights](https://github.com/xinntao/Real-ESRGAN)
