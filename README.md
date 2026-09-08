# 2026年秋季学期

## 2026.9.08
- 张文良 L3A: Label-Augmented Analytic Adaptation for Multi-Label Class Incremental Learning [[paper]([https://github.com/tiggers23/ALBM.git](https://github.com/scut-zx/L3A.git))][[slides](./assets/slides/20260908-zhangwl.pdf)]
> 本文提出L3A，将解析持续学习方法ACL扩展到多标签类增量学习场景，目标是在不保存历史样本的情况下持续学习新类别并减轻遗忘。针对多标签数据中历史类别标签缺失的问题，方法利用上一阶段分类器为当前样本生成历史类别伪标签，形成更完整的训练标签；同时设计加权解析分类器，根据类别出现频率为不同样本分配权重，减弱高频类别主导、低频类别被忽视的问题。模型采用冻结的TResNet-M提取图像特征，并通过随机投影和ReLU映射到高维空间，最终利用加权岭回归的闭式解以及递归更新的 \(R_t\) 和 \(W_t\) 完成持续学习。实验表明，L3A在COCO和VOC多种增量协议下取得了较好的无回放多标签持续学习性能。

# 过去的合集 
- [2026年春季学期](./2026-spring.md)
- [2025年秋季学期](./2025-autumn.md)
- [2025年春季学期](./2025-spring.md)
- [2024年秋季学期](./2024-autumn.md)
- [2024年春季学期](./2024-spring.md)
- [写作参考材料](./documents.md)
