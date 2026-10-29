# 2026年秋季学期
## 2026.10.27
- 卢昕怡 Handling Spatial-Temporal Data Heterogeneity for Federated Continual Learning via Tail Anchor [[paper](./assets/papers/Yu_Handling_Spatial-Temporal_Data_Heterogeneity_for_Federated_Continual_Learning_via_Tail_CVPR_2025_paper.pdf)][[slides](./assets/slides/20261027-lxy.pdf)]
> 第一篇FedTA 面向联邦持续学习（FCL）中空间-时间数据异质性引发的灾难性遗忘问题，将遗忘解耦为参数遗忘与输出遗忘。方法上冻结所有客户端共享的预训练 ViT 以消除参数遗忘，并首次引入可学习的尾部锚点与冻结特征混合，通过对比损失将特征锚定到服务器选定的固定全局原型，从而抑制输出遗忘；同时设计输入增强、选择性输入知识融合和最佳全局原型选择来提升下游性能与跨客户端知识共享。
> 第二篇FedMGP则更关注个性化联邦持续学习（PFCL）下的时空灾难性遗忘与本地个性化挑战。该方法首次显式构建多粒度知识空间，通过使用粗粒度全局提示作用于输入嵌入层，以负责时空不变的粗粒度知识，便于服务器聚合，以对抗空间遗忘；同时使用细粒度局部提示作用于MSA层，以负责类级别的个性化知识，用于对抗时间遗忘并实现本地个性化。
> 第三和第四篇是以往的FCL方法（MFCL和TARGET），主要思路都是无数据下的旧样本生成，与当前新样本一起混合训练，以缓解遗忘。MFCL主要提出把生成式回放从客户端上移到服务器，且生成器训练完全不接触原始数据，以无数据的方式进行生成器训练，合成旧任务样本并下发给客户端；客户端训练时混合真实数据与合成数据，通过拆分分类头学新类、冻结骨干只调分类头、重要性加权特征蒸馏来兼顾塑性与稳定性。TARGET也是相似的思想，基于持续学习的方法往往需要额外数据集或存储旧任务真实数据，在联邦的隐私敏感场景下不可行，因此服务器利用旧全局模型无示例地生成模拟全局数据分布的合成数据，客户端再用这些合成旧数据与当前真实新数据联合全局教师模型进行知识蒸馏，以实现缓解遗忘和保护隐私。

## 2026.10.20
- 孙佳家 pFedMMA:Personalized Federated Fine-Tuning with Multi-Modal Adapter for Vision-Language Models [[paper](./assets/papers/pFedMMA%20-Personalized%20Federated%20Fine-Tuning%20with%20Multi-Modal%20Adapter%20for%20Vision-Language%20Models.pdf)][[slides](./assets/slides/2026.10.20%E7%BB%84%E4%BC%9A%E5%AD%99%E4%BD%B3%E5%AE%B6.pptx)]
>  针对个性化联邦视觉语言学习中客户端数据高度异构、传统联邦提示学习方法难以兼顾本地个性化与跨客户端泛化能力，尤其是在未见类别和跨域场景下容易出现泛化性能下降的问题，提出了一种基于多模态适配器的个性化联邦微调框架pFedMMA。该方法以预训练的 CLIP 视觉语言模型为基础，在冻结视觉和文本编码器原有参数的前提下，在两个编码器的高层 Transformer 模块中引入轻量级多模态适配器。每个适配器由模态特定的降维投影层、跨模态共享投影层和模态特定的升维投影层组成，通过共享投影实现图像与文本特征的协同对齐，同时保留不同模态的特征表达能力。在联邦训练方面，作者设计了一种局部个性化与全局共享相结合的非对称优化策略：各客户端利用本地数据更新完整的多模态适配器，但仅将共享投影层参数上传至服务器进行全局聚合，而模态特定的升维和降维投影层始终保留在本地，从而在适应客户端特有数据分布的同时促进跨客户端知识迁移，并降低通信开销。实验方面，作者在涵盖类别分布偏移和特征分布偏移的11个数据集上开展评估，通过 Local、Base、Novel 准确率及其HM综合衡量模型的个性化与泛化能力。在7个视觉分类数据集的16-shot实验中，该方法取得了84.15%的平均HM准确率，并在多种非IID场景下表现出较强的适应能力。
## 2026.10.13
- 蒋明忠 ZoomEarth: Active Perception for Ultra-High-Resolution Geospatial  Vision-Language Tasks [[paper](./assets/papers/Liu%20%E7%AD%89%20-%202026%20-%20ZoomEarth%20Active%20Perception%20for%20Ultra-High-Resolution%20Geospatial%20Vision-Language%20Tasks.pdf)][[slides](./assets/slides/%E8%92%8B%E6%98%8E%E5%BF%A0-2026.10.pdf)]
>  针对超高分辨率遥感图像中传统视觉语言模型存在的细节信息丢失、视觉冗余严重以及缺乏主动感知能力等问题，提出了一种基于主动感知（Active Perception）的遥感视觉语言框架 ZoomEarth。该方法模仿人类“先整体观察、再局部放大”的视觉认知过程：首先将超高分辨率遥感图像下采样，利用多模态大模型获取全局场景信息；随后根据用户问题自主判断是否需要进一步观察，并预测感兴趣区域（ROI）的边界框，从原始高分辨率图像中裁剪对应区域，重新输入模型进行精细感知与推理。在训练方面，作者构建了包含17类视觉语言任务的 LRS-GRO 数据集，并以 Qwen2.5-VL-3B 为基础模型，采用监督微调（SFT）与 GRPO 强化学习的两阶段训练策略，同时设计区域引导奖励（Region-Guided Reward），缓解传统 IoU 奖励在目标定位偏差较大时反馈稀疏的问题。实验表明，该方法能够有效提升超高分辨率遥感图像的视觉问答、目标定位和细粒度理解能力，并可通过工具调用扩展至图像分割、去云和图像编辑等下游任务。其核心贡献是将传统的被动式遥感图像理解转变为由模型自主决定“看哪里、是否放大、如何进一步观察”的主动感知范式。
## 2026.10.6
- 郑腾鑫陵 
> Jev 是 TypeSafe AI 推出的一种“决策模型”，由前 OpenAI 研究人员开发，它不生成自由文本，而是从预设选项中直接输出带置信度的结构化判断（如“是/否”、选项或评分）。它主要面向分类、路由、评分等高频、有限选项的场景，速度比传统大模型快得多，成本也低得多，常被用作 Agent 系统中的“快判断”组件，与负责复杂推理的大模型形成“快慢分工”。
> 
> DeepSeek Harness（简称 dsh）是 DeepSeek 开源的 Agent 运行时框架，核心公式是“Model + Harness = Agent”。基座模型负责推理，Harness 则是环绕模型的“执行神经系统”，负责调度工具、管理状态和执行闭环。
它的核心设计原则是 “一切皆插件”，底层基于 Cordis 插件内核构建。模型、工具、技能、会话、沙箱、存储、Agent Loop、调度、UI 等所有能力都是独立插件，可自由替换和重组，无需改动框架源码。这意味着可替换范围从单个工具一直延伸到整个 Agent 循环本身。
DeepSeek Harness 提供四种运行模式：标准模式（完整工具组合）、PTC 模式（程序化工具调用，模型生成代码组合多轮调用）、极简模式（仅保留 shell 和文件编辑，用于基准测试）、创造模式（允许 Agent 在内存中试验和组合插件）。
会话系统采用仅追加的事件日志，模型看到的系统提示词、思维链、工具调用与结果、子 Agent 调度等全部被记录，支持恢复、分叉、检索与回放。多 Agent 采用 Supervisor-Worker 模式，父 Agent 可通过 Spawn 或 Fork 启动子 Agent。

## 2026.9.22
- 冯朝晨 SAGE: REINFORCEMENT LEARNING FOR SELF-IMPROVING AGENT WITH SKILL LIBRARY [[paper](https://github.com/amazon-science/SAGE.git)][[slides](./assets/slides/fzc0922.pdf)]
>  这篇 ACL 2026 的论文提出了 SAGE（Skill Augmented GRPO for self-Evolution），面向带有技能库的自改进智能体，通过强化学习同时优化 Skill 的生成、复用与任务执行。其核心是 Sequential Rollout：让智能体连续执行一组相似任务，并把前序任务生成的 Skill 保存到技能库中供后续任务调用；同时设计 Skill-integrated Reward，不仅奖励当前任务成功，还额外奖励“生成的 Skill 能帮助后续任务成功”以及“成功复用已有 Skill”的行为。实验在 AppWorld 上表明，SAGE 相比普通 GRPO 在 Test Normal 上将 SGC 从 51.8% 提升到 60.7%，同时减少约 26% 的交互步数和 59% 的生成 Token。论文说明，相比只优化单任务结果的传统 Agent RL，SAGE 更关注经验能否被沉淀为可复用技能，从而提升智能体的持续自改进能力与执行效率。

- 林鑫科 Concept Bottleneck Models [[paper](https://arxiv.org/abs/2007.04612)][[slides](./assets/slides/20260922林鑫科.pdf)]
>  大家好，本周将和大家分享文章《Concept Bottleneck Models》。本文认为，传统端到端模型直接从输入预测结果，虽然能够获得较好的任务性能，但缺乏基于人类可理解概念进行解释和干预的能力。为此，文章在输入与最终预测之间引入概念瓶颈，构建 \(X\rightarrow C\rightarrow Y\) 的模型结构，并重点研究了不同训练方式下模型的任务准确率、概念准确率以及测试时概念干预的效果。


- 王必广 Abductive multi-instance multi-label learning for periodontal disease [[paper](https://www.sciencedirect.com/science/article/pii/S1361841524003797)][[slides](./assets/slides/2026_0922wbg.pdf)]
>  大家好，本周和大家分享一篇关于神经符号学习与医学图像分类的论文《Abductive Multi-Instance Multi-Label Learning for Periodontal Disease Classification with Prior Domain Knowledge》，发表于 Medical Image Analysis。论文针对传统牙周疾病分类方法难以刻画局部病变与疾病类别之间复杂关系、且难以有效利用医生先验知识的问题，提出了 AB-MIML 方法。该方法将整张口腔图像作为 Bag、局部图像块作为 Instance，利用多实例多标签学习建模局部区域与疾病属性之间的关系，并进一步将医生经验和图像结构信息表示为知识库，通过溯因推理（Abductive Reasoning）对模型产生的伪标签进行校验和修正，使神经网络的感知能力与符号知识的推理能力相结合。汇报中将重点介绍 MIML 建模、知识库构建、溯因学习机制以及实验结果。欢迎大家批评指正，谢谢！


## 2026.9.15
- 白楚榆 EIA: ENVIRONMENTAL INJECTION ATTACK ON GENERALIST WEB AGENTS FOR PRIVACY LEAKAGE [[paper](https://arxiv.org/pdf/2409.11295)][[slides](./assets/slides/2026.9.15组会%20白楚榆.pdf)]
> 这篇 ICLR 2025 的论文提出了“环境注入攻击”（EIA），揭示了网页智能体的一种新型隐私泄露风险。攻击者通过在网页 HTML 中植入隐藏恶意元素，诱导智能体在执行任务时，将用户的个人信息（PII）泄露出去。实验显示，针对特定 PII 的窃取成功率最高可达 70%。由于攻击后原任务仍能正常完成，用户难以察觉。论文强调，简单的提示词防御无效，需构建多层次的防御体系。

- 蒋塾英 DeepTutor: Towards Agentic Personalized Tutoring [[paper](https://github.com/HKUDS/DeepTutor.git)][[slides](./assets/slides/20260915-jiangsy.pdf)]
> 该论文提出 DeepTutor，一个以共享个性化引擎为核心的个性化学习框架，旨在解决大模型教育系统中问题辅导与问题生成相互割裂、缺乏持续学习者模型的问题。系统由静态知识基础（SKG）和动态个性化记忆（DPM）组成：SKG 提供课程知识依据，DPM 通过轨迹森林和学习者画像持续记录学习过程与薄弱点。DeepTutor 将辅导拆为“调查—引导—迭代生成”，将出题拆为“想法生成—题目/答案/解析生成”，并用独立 Validator 校验，使辅导与练习形成闭环。论文还提出 TutorBench 基准，实验显示其相比最佳基线整体提升 10.76%，验证了 SKG 与 DPM 对个性化教学的关键作用。


## 2026.9.08
- 张文良 L3A: Label-Augmented Analytic Adaptation for Multi-Label Class Incremental Learning [[paper](https://github.com/scut-zx/L3A.git)][[slides](./assets/slides/20260908-zhangwl.pdf)]
> 本文提出L3A，将解析持续学习方法ACL扩展到多标签类增量学习场景，目标是在不保存历史样本的情况下持续学习新类别并减轻遗忘。针对多标签数据中历史类别标签缺失的问题，方法利用上一阶段分类器为当前样本生成历史类别伪标签，形成更完整的训练标签；同时设计加权解析分类器，根据类别出现频率为不同样本分配权重，减弱高频类别主导、低频类别被忽视的问题。模型采用冻结的 TResNet-M 提取图像特征，并通过随机投影和ReLU映射到高维空间，最终利用加权岭回归的闭式解以及递归更新的 $R_t$ 和 $W_t$ 完成持续学习。实验表明，L3A在COCO和VOC多种增量协议下取得了较好的无回放多标签持续学习性能。

# 过去的合集 
- [2026年春季学期](./2026-spring.md)
- [2025年秋季学期](./2025-autumn.md)
- [2025年春季学期](./2025-spring.md)
- [2024年秋季学期](./2024-autumn.md)
- [2024年春季学期](./2024-spring.md)
- [写作参考材料](./documents.md)
- [2026年戏曲讨论班](./opera.md)
