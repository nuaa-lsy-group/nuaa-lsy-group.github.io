# 2024年秋季学期
## 2024.3.19
- 郑腾鑫陵：AMU-Tuning Effective Logit Bias for CLIP-based Few-shot Learning [[paper](./assets/papers/AMU-Tuning%20Effective%20Logit%20Bias%20for%20CLIP-based%20Few-shot%20Learning.pdf)][[slides](./assets/slides/2025.3.19组会%20郑腾鑫陵.pdf)]
## 2024.12.17
- 郑金鹏：CLIPCleaner Cleaning Noisy Labels with CLIP[[paper](https://dl.acm.org/doi/10.1145/3664647.3680664)][[slides](./assets/slides/20241217-zjp.pdf)]

## 2024.12.10
- 郑腾鑫陵：Efficient Test-Time Adaptation of Vision-Language Models & WATT: Weight Average Test-Time Adaptation of CLIP[[paper1](./assets/papers/Efficient%20Test-Time%20Adaptation%20of%20Vision-Language%20Models.pdf)[[paper2](./assets/papers/WATT%20Weight%20Average%20Test-Time%20Adaptation%20of%20CLIP.pdf)][[slide](./assets/slides/2024.12.10组会&郑腾鑫陵.pdf)]
>第一篇文章使用CLIP为backbone，不调节CLIP参数，设计positive和negative队列作为缓存模型，减少时间开销。第二篇使用CLIP为backbone，根据text template 调整CLIP参数，验证不同text template的影响。

- 卢昕怡：Class Balanced Adaptive Pseudo Labeling for Federated Semi-Supervised Learning [[paper](./assets/papers/Class_Balanced_Adaptive_Pseudo_Labeling_for_Federated_Semi-Supervised_Learning_CVPR_2023_paper.pdf)][[slides](./assets/slides/2024.12.10组会%20卢昕怡%20.pdf)]

## 2024.12.3

- 赵世佶：Decorate the Newcomers: Visual Domain Prompt for Continual Test Time Adaptation & Dataset Condensation with Gradient Matching [[paper1](./assets/papers/Decorate%20the%20Newcomers%20Visual%20Domain%20Prompt%20for%20C.pdf)] [[paper2](./assets/papers/Dataset%20Condensation%20with%20Gradient%20Matching.pdf)] [[slide](./assets/slides/20241203-zhaosj.pdf)]

> 第一篇文章做的是持续TTA的设定。文章通过直接在图像像素层面构造矩形prompt作为可变参数，并和输入图像聚合送入冻结的模型中得到输出。作者设计了两种prompt，一个用教师-学生网络，通过交叉熵更新学习域知识；另一个多了一项正则限制域敏感参数的更新以保证域泛化知识保留。第二篇是数据集蒸馏的经典论文，通过课程梯度匹配的方式实现数据集蒸馏。

## 2024.11.26

- 陶子健： Towards Calibrated Multi-label Deep Neural Networks[[paper](./assets/papers/Towards_Calibrated_Multi-Label_Deep_Neural_Networks.pdf)][[slides](./assets/slides/2024.11.25组会%20陶子健.pdf)]

- 郑金鹏：GLAD: Towards Better Reconstruction with  Global and Local Adaptive Diffusion Models for  Unsupervised Anomaly Detection[[paper](./assets/papers/GLAD%20Towards%20Better%20Reconstruction%20with%20Global%20and%20Local%20Adaptive%20Diffusion%20Models%20for%20Unsupervised.pdf)][[slides](./assets/slides/2024.11.26-郑金鹏.pdf)]

## 2024.11.19

- 卢昕怡：Towards Unbiased Training in Federated Open-world Semi-supervised Learning [[paper](./assets/papers/Towards%20Unbiased%20Training%20in%20Federated%20Open-world%20Semi-supervised%20Learning.pdf)] [[slide](./assets/slides/2024.11.19组会%20卢昕怡.pdf)]
- 郑腾鑫陵：A Versatile Framework for Continual Test-Time Domain Adaptation: Balancing  Discriminability and Generalizability
[[paper](./assets/papers/A%20Versatile%20Framework%20for%20Continual%20Test-Time%20Domain%20Adaptation%20Balancing%20Discriminability%20and%20Gene.pdf)][[silde](./assets/slides/2024.11.19组会%20郑腾鑫陵.pdf)]

## 2024.11.12

- 赵世佶：Self-supervised Learning for Large-scale Item Recommendations & Deep Interest Network for Click-Through Rate Prediction [[paper1](./assets/papers/Deep%20Interest%20Network%20for%20Click-Through%20Rate%20Predion.pdf)] [[paper2](./assets/papers/Self-supervised%20Learning%20for%20Large-scale%20Item%20Recommendations.pdf)] [[slide](./assets/slides/20241112-zhaosj.pdf)]

> 简要介绍了推荐系统的基础架构：召回->粗排->精排->重排，然后分别展示了召回和精排的两个经典模型。谷歌在召回双塔模型的基础上引入对比学习扩充了样本量，解决了长尾表征的问题。阿里利用attention对用户序列建模，设计了DIN。

- 郑宇祥：Learning Equi-angular Representations for Online Continual Learning[[paper](https://arxiv.org/abs/2404.01628)][[slides](./assets/slides/20241112-zyx.pdf)]

## 2024.11.6

- 郑金鹏：AnomalyGPT: Detecting Industrial Anomalies Using Large Vision-Language Models[[paper](https://arxiv.org/abs/2308.15366)][[slides](./assets/slides/2024.11.7郑金鹏.pdf)]

## 2024.10.29

- 卢昕怡：Robust Semi-supervised Learning by wisely leveraging open-set data [[paper](./assets/papers/Robust%20Semi-supervised%20Learning%20by%20wisely%20leveraging%20open-set%20data.pdf)] [[slide](./assets/slides/2024.10.29%20组会%20卢昕怡.pdf)]
- 郑宇祥：Breaking the Memory Barrier: Near Infinite Batch Size Scaling for Contrastive Loss[[paper](https://arxiv.org/abs/2410.17243)][[slides](./assets/slides20241029-zyx.pdf)]

## 2024.10.21

- 赵世佶：EcoTTA: Memory-Efficient Continual Test-time Adaptation via Self distilled Regularization [[paper](./assets/papers/EcoTTA_Memory-Efficient_Continual_Test-time_Adapt.pdf)] [[slide](./assets/slides/20241021-zhaosj.pdf)]

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
