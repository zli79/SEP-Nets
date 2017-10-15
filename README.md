# SEP-NETs
This repository contains instroduction, instruction, models, prototxt and logs file along experiments for SEP-Nets introduced in the paper  ["SEP-Nets: Small and Effective Pattern Networks"](https://arxiv.org/pdf/1706.03912.pdf) by Zhe Li, Xiaoyu Wang, Xutao Lv, Tianbao Yang.

### Citting SEP-Nets
If you are using SEP-Nets, please cite as folowing:

        @article{li2017sep,
          title={SEP-Nets: Small and Effective Pattern Networks},
          author={Li, Zhe and Wang, Xiaoyu and Lv, Xutao and Yang, Tianbao},
          journal={arXiv preprint arXiv:1706.03912},
          year={2017}
        }

## Contents:
1. [Introduction](#Introduction)
2. [Instruction](#Instruction)
3. [Experiments on CIFAR10 with ResNet](#Experiments-on-CIFAR10-with-ResNet)
4. [Experiments on ImageNet with GoogleNet](#Experiments-on-ImageNet-with-GoogleNet)
5. [Experiments on ImageNet with Customized-InceptionNet](#Experiments-on-ImageNet-with-Customized-InceptionNet)
6. [Summary](#Summary)

## Introduction
We propose a simple yet powerful method for compressing the size of deep CNNs based on parameter binarization. The striking difference from most previous work on parameter binarization/quantization lies at different treatments of $1\times 1$ convolutions and $k\times k$ convolutions ($k>1$), where we only binarize $k\times k$ convolutions into binary patterns.  The resulting networks are referred to as pattern networks. By doing this, we show that previous deep CNNs such as GoogLeNet and Inception-type Nets can be compressed dramatically with marginal drop in performance. Second, in light of the different functionalities of $1\times 1$ (data projection/transformation) and $k\times k$ convolutions (pattern extraction), we propose a new block structure codenamed the pattern residual block that adds transformed feature maps generated by $1\times 1$ convolutions to the pattern feature maps generated by $k\times k$ convolutions, based on which we design a small network with $\sim 1$ million parameters.  Combining with our parameter binarization, we achieve better performance on ImageNet than using similar sized networks including recently released Google MobileNets.
## Instruction
## Experiments on CIFAR10 with ResNet
## Experiments on ImageNet with GoogleNet
## Experiments on ImageNet with Customized-InceptionNet
## Summary



