# 2024年秋季学期

## 2024.10.21

- 赵世佶：EcoTTA: Memory-Efficient Continual Test-time Adaptation via Self distilled Regularization [[paper](./assets/papers/EcoTTA_Memory-Efficient_Continual_Test-time_Adapt.pdf)] [[slide](./assets/slides/20241021zhaosj.pdf)]

> 介绍了EcoTTA，一篇研究持续TTA过程中如何减少内存消耗，从而能在端侧设备上实现持续适应。文章借鉴了TinyTL、EATA等一系列工作，通过将源模型的encoder分块，并在每一块之间插入专属的元网络(包括一层BN和一个Conv的残差连接)，实现模型激活值内存占用大幅缩减。设计的损失函数包括经典的熵最小化，以及一个子蒸馏的正则项用于防止模型遗忘。

- 陶子健：Pi-DUAL: Using privileged information to distinguish clean from noisy labels [[paper](./assets/papers/Pi-DUAL%20Using%20privileged%20information%20to%20distinguish%20clean%20from%20noisy%20labels.pdf)] [[slide](./assets/slides/2024.10.21组会%20陶子健.pdf)]

## 2024.10.14

- 郑腾鑫陵：Continual test-time domain Adaption [[paper](./assets/papers/Continual_test-time_domain_Adaption.pdf)] [[slide](./assets/slides/2024.10.14组会%20郑腾鑫陵.pdf)]

## 2024.9.23

- 郑金鹏：DeiT-LT: Distillation Strikes Back for Vision Transformer Training on Long-Tailed Datasets [[paper](https://openaccess.thecvf.com/content/CVPR2024/papers/Rangwani_DeiT-LT_Distillation_Strikes_Back_for_Vision_Transformer_Training_on_Long-Tailed_CVPR_2024_paper.pdf)] [[slide](./assets/slides/2024.9.23组会%20郑金鹏.pdf)]
- 陶子健：Category-Prompt Refined Feature Learning for Long-Tailed Multi-Label Image Classification [[paper](./assets/papers/Category-Prompt%20Refined%20Feature%20Learning%20for%20Long-Tailed%20Multi-Label%20Image%20Classification-acmmm2024.pdf)] [[slide](./assets/slides/2024.9.23组会%20陶子健.pdf)]

## 2024.9.9

- 卢昕怡： FedCorr Multi-Stage Federated Learning for Label Noise Correction [[paper](./assets/papers/FedCorr_Multi-Stage_Federated_Learning_for_Label_Noise_Correction.pdf)] [[slide](./assets/slides/2024.9.9%20卢昕怡.pdf)]
- 郑腾鑫陵：Continual-MAE Adaptive Distribution Masked Autoencoders for Continual Test-Time Adaptation [[paper](./assets/papers/Continual-MAE_Adaptive_Distribution_Masked_Autoencoders_for_Continual_Test-Time_Adaptation.pdf)] [[slide](./assets/slides/2024.9.9%20郑腾鑫陵.pdf)]

---

[2024年春季学期](./2024-spring.md)

[写作参考材料](./documents.md)
