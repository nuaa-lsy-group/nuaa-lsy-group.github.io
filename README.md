# 2026春季学期
## 2026.3.25
- 王远见 Concepts from Representations Post-hoc Concept Bottleneck Models via Sparse Decomposition of Visual Representations [[paper](./assets/papers/Concepts%20from%20Representations%20Post-hoc%20Concept%20Bottleneck%20Models%20via%20Sparse%20Decomposition%20of%20Visual%20Representations.pdf)][[slides](./assets/slides/2026.03.25%E7%BB%84%E4%BC%9A%20%E7%8E%8B%E8%BF%9C%E8%A7%81.pdf)]
> 本文提出了一种名为PCBM-ReD的新型事后概念瓶颈模型（CBM），为预训练的黑盒视觉模型自动赋予高保真可解释性。该方法利用稀疏自编码器从预训练图像编码器的潜在表示中挖掘特征概念，并借助多模态大语言模型（MLLM）根据视觉可识别性与任务相关性进行标注与过滤；提出一种基于重建引导的无监督贪心算法，筛选出线性独立且能高效重构原始视觉表征的核心概念子集；利用CLIP的图文对齐特性，将图像表征稀疏分解为概念文本嵌入的线性组合，并在此基础上拟合线性分类器。PCBM-ReD缩小了与端到端黑盒模型的性能差距、达到同类可解释模型的最优精度，还完整保留了零样本与少样本泛化能力，并通过人工评估验证了其在概念直观性、表征忠实度及预测因果关联性上的显著优势。


## 2026.3.18
- 张文良 Hybrid Concept Bottleneck Models [[paper](https://github.com/ly1998117/HybridCBM)][[slides](./assets/slides/2026.3.18-zhangwl.pdf)]
> 这篇文章针对传统 CBM 需要昂贵概念标注且概念库不完整导致性能受限的问题，提出了HybridCBM——用 CLIP 共享空间免去除人工概念标注，用"静态概念（LLM 生成）+ 动态概念（可学习向量）"的混合概念库突破预定义限制，再用 GPT-2 翻译器将动态向量转为文本保持可解释性，最终在性能接近黑盒模型的同时保持高可解释性。
- 孙佳家 FedMGP: Personalized Federated Learning with Multi-Group Text-Visual Prompts [[paper](./assets/papers/FedMGP.pdf)][[slides](./assets/slides/2026.3.18%E7%BB%84%E4%BC%9A%20%E5%AD%99%E4%BD%B3%E5%AE%B6.pptx)]
> 这篇文章针对传统联邦提示学习仅依赖单一文本提示、易产生客户端过拟合和聚合不稳定，且难以兼顾个性化与泛化性的问题，提出了FedMGP——为每个客户端配置多组文本-视觉配对提示，搭配多样性损失驱动各提示组专攻不同互补语义维度，再设计基于相似度引导概率采样的动态提示聚合策略，在优先聚合语义对齐知识的同时探索少表征模式，还通过在多组间重新分配固定提示容量保持参数高效性，最终以最低的通信参数（5.1k）在各类联邦视觉-语言基准任务中，实现了个性化和域泛化性能的双优，同时平衡了全局公共知识保留与客户端特定特征挖掘。


## 2026.3.11
- 蒋明忠  SAM 3: Segment Anything with Concepts[[paper](./assets/papers/sam3.pdf)][[slides](./assets/slides/2026.3.11%E7%BB%84%E4%BC%9A-%E8%92%8B%E6%98%8E%E5%BF%A0%20.pdf)]
>这篇论文提出了 SAM 3 (Segment Anything Model 3)，这是一个统一的视觉模型，旨在基于概念提示（Concept Prompts，如简短的名词短语“黄色校车”、图像示例或两者结合）在图像和视频中检测、分割并跟踪所有匹配的对象实例。
其核心贡献包括：
新任务定义：正式提出了可提示概念分割 (PCS) 任务，超越了前代仅针对单个对象进行几何提示（点、框）的局限，实现了开放词汇下的全图/全视频实例查找与分割。
模型架构创新：采用共享骨干网络的检测器与基于记忆的视频跟踪器架构，并创新性地引入存在头 (Presence Head) 将“识别”（概念是否存在）与“定位”（对象在哪里）解耦，显著提升了检测精度和抗干扰能力。
数据引擎突破：构建了一个高效的人机协同数据引擎，利用多模态大语言模型（MLLM）作为“AI标注员”生成名词短语和困难负样本，并结合人工验证，构建了包含400万独特概念标签的高质量数据集 SA-Co。
性能表现：SAM 3 在图像和视频的 PCS 任务上将现有系统的准确率提高了一倍，同时在传统的视觉提示分割任务上也优于 SAM 2，并开源了模型代码及全新的 SA-Co 基准测试集。





# 过去的合集 

- [2025年秋季学期](./2025-autumn.md)
- [2025年春季学期](./2025-spring.md)
- [2024年秋季学期](./2024-autumn.md)
- [2024年春季学期](./2024-spring.md)
- [写作参考材料](./documents.md)
