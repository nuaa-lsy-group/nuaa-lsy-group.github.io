# 2026春季学期
## 2026.6.3
- 王子晨 Prototypes as Anchors: Tackling Unseen Noise for online continual learning 
[[paper](./assets/papers/Prototypes%20as%20Anchors%20Tackling%20Unseen%20Noise%20for%20online%20continual%20learning.pdf)][[slides](./assets/slides/20260603-wzc_20260603130707.pdf)]
> 本文首次正式定义并分析闭集噪声与开集噪声，指出两类噪声都会向当前训练分类器引入未知类别样本。为有效处理噪声标签与未知类别，本文提出一种基于回放的创新方法：原型锚定（PAA）。该方法为每一类学习具有代表性且强判别性的原型，并在表征空间中采用基于相似度的去噪机制，以识别并消除未知类别带来的负面影响。同时，PAA 采用双分类器架构，通过分类器间的一致性校验进一步提升模型鲁棒性。
## 2026.5.27
- 白楚榆 EMERGING SAFETY ATTACK AND DEFENSE IN FED ERATED INSTRUCTION TUNING OF LARGE LANGUAGE MODELS [[paper](./assets/papers/EMERGING%20SAFETY%20ATTACK%20AND%20DEFENSE%20IN%20FED-%20ERATED%20.pdf)][[slides](./assets/slides/2026.5.27%E7%BB%84%E4%BC%9A%20%E7%99%BD%E6%A5%9A%E6%A6%86.pdf)]
> 本文首次揭示了联邦指令微调（FedIT）场景下大语言模型安全对齐的脆弱性。研究发现，恶意客户端只需将本地训练数据替换为未对齐数据，即可在不被察觉的情况下显著破坏全局模型的安全性，且现有6种联邦防御方法对此基本失效，最多仅能恢复4%的安全性。针对这一问题，论文提出了一种事后防御方法：在每轮聚合完成后，服务器自动生成安全对齐数据对全局模型进行微调修复，最多可恢复69%的安全性，甚至超过无攻击时的水平，且该方法即插即用，无需改动现有联邦训练流程。
- 刘天泽 Seg2Change Adapting Open-Vocabulary Semantic Segmentation Model for Remote Sensing Change Detection [[paper](./assets/papers/Seg2Change%20Adapting%20Open-Vocabulary%20Semantic%20Segmentation%20Model%20for%20Remote%20Sensing%20Change%20Detection.pdf)][[slides](./assets/slides/20260527-liutz.pdf)]
> 本文首先构建了类别无关变化检测数据集 CA-CDD；同时设计了类别无关变化检测头（CACH），能够捕捉任意地物类别间的转换关系，并映射到具体语义类别。在此基础上，本文提出Seg2Change适配模块，用以将现有开放词汇语义分割模型高效适配到变化检测任务中。该框架结构简洁、无需额外冗余设计，在多项基准测试上取得了当前最优的开放词汇变化检测性能。

## 2026.5.20
- 冯朝晨 PersonaVLM-Long-Term Personalized Multimodal LLMs [[paper](./assets/papers/PersonaVLM-Long-Term%20Personalized%20Multimodal%20LLMs.pdf)][[slides](./assets/slides/PersonaVLM.pdf)]
> 这篇论文提出PersonaVLM，一个面向长期个性化交互的多模态大语言模型智能体框架。该框架通过集成记忆（主动提取并总结多模态交互历史）、推理（检索相关记忆进行多轮个性化推理）和响应对齐（动态推断用户演变个性并调整输出）三项关键能力，将通用MLLM转化为能持续适应用户偏好变化的个性化助理。为评估长期个性化能力，构建了Persona-MME基准，涵盖超过2,000个交互案例、7个关键维度和14个细粒度任务。
- 蒋塾英 Backpropagation-Free Test-Time Adaptation via Probabilistic Gaussian Alignment [[paper](./assets/papers/Backpropagation-Free%20Test-Time%20Adaptation%20via%20Probabilistic%20Gaussian%20Alignment.pdf)][[slides](./assets/slides/2026.5.20%E7%BB%84%E4%BC%9A%E8%92%8B%E5%A1%BE%E8%8B%B1.pdf)]
> 该论文的核心在于将模型在测试阶段的优化过程从复杂的梯度下降重构为高效的概率统计推理。在不进行任何反向传播的情况下，该方法将测试输入特征建模为高斯分布，通过对比观测数据与预定义的类原型分布，利用闭式解直接更新类均值。这种方法不仅彻底规避了反向传播带来的高显存开销与推理延迟，还通过引入历史知识库与 CLIP 先验的正则化机制，显著提升了模型在应对分布偏移时的决策稳定性，使其成为极低算力设备实现高精度实时自适应的理想方案。

## 2026.5.13
- 林鑫科 BACK TO BASICS REVISITING ASR IN THE AGE OF VOICE AGENTS [[paper](./assets/papers/BACK%20TO%20BASICS%20REVISITING%20ASR%20IN%20THE%20AGE%20OF%20VOICE%20AGENTS.pdf)][[slides](./assets/slides/2026_5_13lxk.pdf)]
> 这篇论文提出了WildASR，一个基于真实人类语音的多语言诊断基准(benchmark)，系统评估ASR系统在环境退化、人口统计变化和语言多样性三大维度下的鲁棒性，揭示当前ASR模型在真实世界复杂条件下的严重性能下降和幻觉问题，并提供实用的分析工具，推动更可靠的语音识别系统研发。

## 2026.5.7
- 郑腾鑫陵 多模态大模型发展历程[[slides](./assets/slides/2026.5.6组会%20郑腾鑫陵.pdf)]
> 内容分为三部分。第一部分关于Transformer架构及相应拓展（旋转位置编码 ROPE、注意力机制 MHA、MQA、GQA、MLA）。第二部分关GPT 1-3系列、ViT、CLIP、BLIP 1-3系列、LLaVA 1 1.5 1.5HD系列、Qwen-VL、Qwen2-VL、Qwen2.5-VL系列。第三部分关于后训练（监督微调，强化对齐 PPO、DPO、GRPO）。

## 2026.4.29
- 刘天泽 MM-OVSeg: Multimodal Optical–SAR Fusion for Open-Vocabulary Segmentation in Remote Sensing [[paper](./assets/papers/MM-OVSeg%20Multimodal%20Optical%E2%80%93SAR%20Fusion%20for%20Open-Vocabulary.pdf)][[slides](./assets/slides/20260429-liutz(1).pdf)]
> 开放词汇分割能够从开放文本类别中实现像素级识别，可超越固定类别实现泛化。尽管在遥感中极具潜力，但该领域的研究仍高度依赖晴空光学数据，在多云、雾霾等恶劣条件下表现极差。本文提出 MM-OVSeg，一种用于恶劣天气下鲁棒开放词汇分割的光学–SAR 多模态融合框架。MM-OVSeg 充分利用两种模态的互补优势：光学图像提供丰富的光谱语义，而合成孔径雷达（SAR）具备穿透云层的结构信息。为解决跨模态域差异与当前视觉–语言模型稠密预测能力不足的问题，我们提出两项关键设计：用于多传感器特征对齐的跨模态统一流程，以及双编码器融合模块，该模块整合多个视觉基础模型的分层特征，实现文本对齐的多模态分割。大量实验表明，MM-OVSeg 在各类云覆盖条件下均具备优异的鲁棒性与泛化能力。
- 张文良 HGLTR: Hierarchical Knowledge Injection for Calibrating Pre-trained Models in  Long-Tail Recognition [[paper](https://github.com/z7d1/hgltr.git)][[slides](./assets/slides/20260429-zhangwl.pdf)]
> 这篇文章针对长尾分布下预训练视觉‑语言模型在尾类别表现不足的问题，提出 HGLTR——通过将类别层次知识作为先验注入模型，实现特征层面对齐和分类器正则化，使模型在提升尾类别识别准确率的同时保持整体语义一致性。
## 2026.4.22
- 王远见 Discovering Fine-Grained Visual-Concept Relations by Disentangled Optimal Transport Concept Bottleneck Models [[paper](./assets/papers/Discovering%20Fine-Grained%20Visual-Concept%20Relations%20by%20Disentangled%20Optimal%20Transport%20Concept%20Bottleneck%20Models.pdf)][[slides](./assets/slides/2026.04.22%E7%BB%84%E4%BC%9A%20%E7%8E%8B%E8%BF%9C%E8%A7%81.pdf)]
> 本文提出了解耦最优传输概念瓶颈模型（DOT-CBM），旨在同步实现局部图像块与文本概念的细粒度显式对齐，并消除数据偏差导致的捷径学习。该框架包含三个核心设计：模态内特征解耦，通过正交投影损失强制拉开不同局部区域与概念的特征距离，提升细粒度判别力；基于最优传输的细粒度对齐，将概念预测建模为图像块与概念分布间的传输问题，利用Sinkhorn算法求解显式分配矩阵，实现前向概念预测与反向空间定位掩码的双向输出；双先验分布建模抗偏，利用视觉显著性图与概念共现统计构造先验分布注入传输约束，从底层抑制背景干扰与概念混淆。
- 蒋明忠 LoRA: Low-Rank Adaptation of Large Language Models [[paper](./assets/papers/Hu%20%E7%AD%89%20-%202021%20-%20LoRA%20Low-Rank%20Adaptation%20of%20Large%20Language%20Models.pdf)][[slides](./assets/slides/2026.04.22%E7%BB%84%E4%BC%9A-%E8%92%8B%E6%98%8E%E5%BF%A0%20.pdf)]
> 自然语言处理的主流范式包括对一般领域数据的大规模预训练和对特定任务或领域 的适应。当我们预训练更大的模型时,重新训练所有模型参数的传统微调变得不太 可行。以GPT-3 175B为例,部署许多独立的微调模型实例(每个实例都有175B参数) 是非常昂贵的。我们提出了低秩自适应(Low-Rank Adaptation,或LoRA),它冻结了 预训练的模型权重,并将可训练的秩分解矩阵注入到Transformer体系结构的每一层, 从而大大减少了下游任务的可训练参数的数量。对于GPT-3,与完全微调相比, LoRA可以将可训练参数的数量减少10,000倍,计算硬件需求减少3倍。LoRA在GPT3和GPT-2上的模型质量表现与微调相当或更好,尽管具有更少的可训练参数,更高 的训练吞吐量,并且没有额外的推理延迟。我们还对语言模型适应中的等级缺陷进 行了实证研究,从而揭示了LoRA的有效性。


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
