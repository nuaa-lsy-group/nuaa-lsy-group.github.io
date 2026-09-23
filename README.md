# 2026年秋季学期
## 2026.9.22
- 冯朝晨 SAGE: REINFORCEMENT LEARNING FOR SELF-IMPROVING AGENT WITH SKILL LIBRARY [[paper](https://github.com/amazon-science/SAGE.git)][[slides](./assets/slides/fzc0922.pdf)]
>  这篇 ACL 2026 的论文提出了 SAGE（Skill Augmented GRPO for self-Evolution），面向带有技能库的自改进智能体，通过强化学习同时优化 Skill 的生成、复用与任务执行。其核心是 Sequential Rollout：让智能体连续执行一组相似任务，并把前序任务生成的 Skill 保存到技能库中供后续任务调用；同时设计 Skill-integrated Reward，不仅奖励当前任务成功，还额外奖励“生成的 Skill 能帮助后续任务成功”以及“成功复用已有 Skill”的行为。实验在 AppWorld 上表明，SAGE 相比普通 GRPO 在 Test Normal 上将 SGC 从 51.8% 提升到 60.7%，同时减少约 26% 的交互步数和 59% 的生成 Token。论文说明，相比只优化单任务结果的传统 Agent RL，SAGE 更关注经验能否被沉淀为可复用技能，从而提升智能体的持续自改进能力与执行效率。

- 林鑫科 Concept Bottleneck Models [[paper](https://arxiv.org/abs/2007.04612)][[slides](./assets/slides/20260922林鑫科.pdf)]
>  大家好，本周将和大家分享文章《Concept Bottleneck Models》。本文认为，传统端到端模型直接从输入预测结果，虽然能够获得较好的任务性能，但缺乏基于人类可理解概念进行解释和干预的能力。为此，文章在输入与最终预测之间引入概念瓶颈，构建 \(X\rightarrow C\rightarrow Y\) 的模型结构，并重点研究了不同训练方式下模型的任务准确率、概念准确率以及测试时概念干预的效果。


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
