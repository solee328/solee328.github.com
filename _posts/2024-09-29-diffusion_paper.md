---
layout: post
title: DDPM - 논문 리뷰
# subtitle:
categories: diffusion
tags: [diffusion, ddpm, 논문 리뷰]
# sidebar: []
use_math: true
---

안녕하세요:lemon: 오랜만에 들고 온 논문은 DDPM으로 불리는 <a href="https://arxiv.org/abs/2006.11239" target="_blank">Denoising Diffusion Probabilistic Models</a>입니다!

DDPM은 Diffusion Model이라 불리는 Diffusion Probabilistic Model[53]을 개선한 모델로 Variational Autoencoders(VAEs), Generative Adversarial Networks(GANs)와 같은 Generative model로서 널리 사용되고 있습니다. 지금부터 하나하나 살펴보겠습니다 :eyes:
<br>

---

## Generative Model
Generative adversarial networks(GANs), AutoRegressive models, Variational Autoencoders(VAE)로 고품질의 이미지를 생성하는 연구들이 나왔으며 energy-based modeling 및 score matching에서도 GAN과 필적하는 이미지를 생성했습니다.

이 논문에서는 Diffusion Probabilistic model[53]를 기반으로 diffusion model의 sampling이 autoregressive decoding과 유사하며 diffusion model의 특정 parameterization은 denoising score matching과 sampling 중 annealed Langevin dynamics와 동등하다는 것(Section 3.2)을 증명합니다.

또한 Section 4에서 diffusion model이 고품질의 샘플을 생성할 수 있음을 함께 보여주며 생성 모델로서 Diffusion model의 이미지 생성 능력을 증명합니다. DDPM 이전의 다양한 생성 모델들에 대해서 간단하게 정리하고 DDPM의 세계로 가보겠습니다!

### GANs

### AutoRegressive Model

### Variational Autoencoders(VAEs)


### Energy-based Model & Score Matching


### Diffusion Probabilistic Model
[53]은 데이터에 해당하는 샘플을 생성하기 위해 variational inference를 사용해 학습된 parameterized Markov chain입니다.

Markov chain은 ~~~를 의미하며 여기서 diffusion process는 샘플에 noise를 점진적으로 추가하는 것이 됩니다. 모델은 이 diffusion process를 역전시키는 방법을 학습합니다.


<br>

---

## Dataset
LSUN, CelebA-HQ, CIFAR10 등


<br>


## Limitation
likelihood-based model에 비해 log-likelihoods를 가지고 있지는 않다고 합니다. 하지만 energy based model과 score matching 기반으로 생성된 large estimates annealed importance sampling 보다는 log likelihoods가 더 높았으며[11, 55], ---- 이유에서 일 것으로 생각됩니다.

---

<br>
