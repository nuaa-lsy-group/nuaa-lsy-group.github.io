# 2024年春季学期
## 7.4
- 万文海：Data Augmentation-Based Long-tailed Learning[[slide](./assets/slides/2024.7.4组会%20万文海)][[paper1](https://openreview.net/forum?id=RgUPdudkWlN)][[paper2](https://openreview.net/forum?id=RzY9qQHUXy)]
> 介绍了long-tailed learning中关于数据增强的两个工作。第一篇发现class-wise augmentation 可以提高 non-augmented classes 的性能，而 augmented classes 的性能可能不会显著提高，基于这一点，分别计算每个类别的 level-of-learning score，并利用该得分来确定增强强度，第二篇提出一种自适应的动态可选数据增强，以解决固有的数据层面的不平衡和外在的增强层面的不平衡，使每个类别在训练期间可以选择适当的增强方法。

## 6.20
- 郑金鹏：Out-of-Distribution Detection in Long-Tailed Recognition with Calibrated Outlier Class Learning[[slide](./assets/slides/2024.6.20组会%20郑金鹏.pdf)][[paper](./assets/papers/Out-of-Distribution%20Detection%20in%20Long-Tailed%20Recog.pdf)]

## 6.13
- 万文海：Online Knowledge Distillation[[slide](./assets/slides/2024.6.13组会%20万文海.pdf)][[paper1](https://arxiv.org/pdf/1912.00350)][[paper2](https://openaccess.thecvf.com/content_CVPR_2020/papers/Guo_Online_Knowledge_Distillation_via_Collaborative_Learning_CVPR_2020_paper.pdf)]
> 介绍了 Online Knowledge Distillation 的两个工作，一篇使用self-attention机制生成target引导学生网络的输出，另一篇提出了四种基于协作学习的target生成方案。此外，讨论了：1）不平衡场景下训练的模型应用于TTA的合理性、可行性；2）将OOD检测应用于长尾多专家的方案尝试

## 6.6
- 郑宇翔：Loss Decoupling for Task-Agnostic Continual Learning[[slide](./assets/slides/2024.6.6组会%20郑宇祥.pdf)][[paper](./assets/papers/Loss%20Decoupling%20for%20Task-Agnostic%20Continual%20Learning.pdf)]
- 郑金鹏：Open-Sampling: Exploring Out-of-Distribution Data for Re-balancing Long-tailed Datasets[[slide](./assets/slides/2024.3.14组会%20郑金鹏.pdf)][[paper](./assets/papers/Open-Sampling%20Exploring%20Out-of-Distribution%20data%20.pdf)]
> 相似论文：[采样高斯噪声处理长尾](./assets/papers/Pure%20Noise%20to%20the%20Rescue%20of%20Insufficient%20Data%20Imp.pdf)；[采样OOD处理噪声](./assets/papers/Open-set%20Label%20Noise%20Can%20Improve%20Robustness%20Agains.pdf)，也许可以把OOD样本引入到长尾噪声数据集。

## 5.30
- 陶子健：General Multi-label Image Classification with Transformers[[slide](./assets/slides/2024.5.30组会%20陶子健.pdf)][[paper](./assets/papers/General%20Multi-label%20Image%20Classification%20with%20Transformers.pdf)]
> 采用了随机掩码策略，将label embedding添加state embedding，包括positive、negative、unknown，将label embedding和feature embedding同时放入transformer中
> 相似论文：[Language-Guided Transformer for Federated Multi-Label Classification](./assets/papers/Language-Guided%20Transformer%20for%20Federated%20Multi-Label%20Classification.pdf)，
它将随机掩码替换成将global modal在local model上预测的不自信的label进行掩码，加强对不确定的label的学习。


## 5.16
- 万文海：Exploring and Utilizing Pattern Imbalance[[slide](./assets/slides/2024.5.16组会%20万文海.pdf)][[paper](./assets/papers/Exploring_and_Utilizing_Pattern_Imbalance.pdf)]

>相似论文：[Subclass-balancing Contrastive Learning for Long-tailed Recognition](./assets/papers/Hou_Subclass-balancing_Contrastive_Learning_for_Long-tailed_Recognition_ICCV_2023_paper.pdf)
共性：从子类角度出发
简介：介绍了用于长尾识别的子类平衡对比学习（SBCL）。它通过子类平衡自适应聚类将头部类分解为多个语义一致的子类，并结合了一种双粒度对比损失，以促进子类和实例的平衡。在多个数据集上的大量实验表明，SBCL在长尾识别的基准数据集上实现了最先进的单模型性能。

## 5.11

- 赵世佶：Towards Real-World Test-Time Adaptation: Tri-Net Self-Training with Balanced Normalization[[slide](./assets/slides/2024.5.11组会%20赵世佶.pdf)][[paper](./assets/papers/Towards%20Real-World%20Test-Time%20Adaptation%20Tri-Net%20Self-Training%20with%20Balanced%20Normalization.pdf)]

## 4.25

- 陶子健：No Fear of Classifier Biases: Neural Collapse Inspired Federated Learning with Synthetic and Fixed Classifier[[slide](./assets/slides/2024.4.25组会%20陶子健.pdf)][[paper](./assets/papers/No%20Fear%20of%20Classifier%20Biases-Neural%20Collapse%20Inspired%20Federated%20Learning%20with%20Synthetic%20and%20Fixed%20Classifier-iccv2023.pdf)]
- 郑金鹏：ProMix: Combating Label Noise via Maximizing Clean Sample Utility[[slide](./assets/slides/2024.4.25组会%20郑金鹏.pdf)][[paper](./assets/papers/ProMix%20Combating%20Label%20Noise%20via%20Maximizing%20Clean.pdf)]

## 4.21

- 郑宇祥：Understanding and Mitigating the Label Noise in Pre-training on Downstream Tasks[[slide](./assets/slides/2024.4.21组会%20郑宇祥.pdf)][[paper](./assets/papers/Understanding%20and%20Mitigating%20the%20Label%20Noise%20in%20Pre-training%20on%20Downstream%20Tasks.pdf)]
- 赵世佶：PromptStyler: Prompt-driven Style Generation for Source-free Domain Generalization[[slide](./assets/slides/2024.4.21组会%20赵世佶.pdf)][[paper](./assets/papers/PromptStyler%20Prompt-driven%20Style%20Generation%20for%20S.pdf)]

## 3.22

- 万文海：Long-Tailed Recognition via Weight Balancing[[slide](./assets/slides/2024.3.22组会%20万文海.pdf)][[paper](./assets/papers/Long-Tailed_Recognition_via_Weight_Balancing_CVPR_2022_paper.pdf)]

## 3.14

- 陶子健：Model-Contrastive Federated Learning [[slide](./assets/slides/2024.3.14组会%20陶子健.pdf)][[paper](./assets/papers/Li_Model-Contrastive_Federated_Learning_CVPR_2021_paper.pdf)]
- 郑金鹏：When Noisy Labels Meet Long Tail Dilemmas: A Representation Calibration Method [[slide](./assets/slides/2024.3.14组会%20郑金鹏.pdf)][[paper](./assets/papers/When%20Noisy%20Labels%20Meet%20Long%20Tail%20Dilemmas%20A%20Repre.pdf)]
