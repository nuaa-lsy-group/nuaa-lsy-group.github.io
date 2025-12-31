# 音频语音处理
## 1、文字转语音（Text-to-Speech, TTS）
基于数据驱动的语音生成任务，核心是利用深度学习模型建立**文本序列**到**音频波形序列**的映射关系，实现从书面文字到自然、流畅语音的智能合成。

- FastSpeech 2: Fast and High-Quality End-to-End Text to Speech[[paper](https://arxiv.org/pdf/2006.04558)][[code](https://speechresearch.github.io/fastspeech2/)]
> (2006年) 针对非自回归 TTS 模型 FastSpeech 依赖自回归教师模型导致训练流程复杂耗时、时长预测精度不足、蒸馏所得梅尔频谱存在信息损失等问题，提出 FastSpeech 2 模型，该模型摒弃教师 - 学生蒸馏范式，直接采用真实标注数据训练以规避信息丢失，同时引入时长、基频、能量等语音变异信息作为条件输入，训练时从语音波形提取真实特征，推理时使用预测值，更好地解决了 TTS 中的一对多映射问题。

- Tacotron: Towards End-to-End Speech Synthesis[[paper](https://arxiv.org/pdf/1703.10135)]
> (2017年) 第一批真正 end-to-end 的语音合成模型，不再依赖传统复杂的声码器流程。

- Montreal Forced Aligner: trainable text-speech alignment using Kaldi[[paper](http://prosodylab.org/~chael/papers/mcauliffe_etal_2017_MFA.pdf)][[code](https://montrealcorpustools.github.io/Montreal-Forced-Aligner/)]
> (2017年) 提出基于Kaldi的可训练语音-文本强制对齐工具MFA，支持多语言、多格式输入，具备三音素模型和说话人自适应能力，提升对齐精度与效率。

- Conditional Variational Autoencoder with Adversarial Learning for TTS[[paper](https://arxiv.org/pdf/2106.06103)]
> (2021年) 针对现有端到端并行 TTS 模型音质不及两阶段模型的问题，提出一种新型并行端到端 TTS 方法：该方法结合归一化流增强的变分推理与对抗训练提升生成模型表现力，引入随机时长预测器实现文本到多韵律语音的合成，通过隐变量不确定性建模与时长预测器刻画语音的一对多映射关系。

- DiffSinger: Singing Voice Synthesis via Shallow Diffusion Mechanism[[paper](https://arxiv.org/pdf/2105.02446)][[code](https://github.com/MoonInTheRiver/DiffSinger)]
> (2021年) 对现有歌声合成声学模型过平滑或训练不稳定的问题，提出DiffSinger扩散模型：以乐谱为条件迭代生成梅尔频谱，通过浅层扩散机制与自适应边界预测提升音质、加速推理，性能优于主流方案且泛化至 TTS 任务。

- ExpressiveSinger: Multilingual and Multi-Style Score-based Singing Voice Synthesis with Expressive Performance Control[[paper](https://dl.acm.org/doi/10.1145/3664647.3681642)][[demo](https://shuqid.net/expressive-singing-synthesis)]
>（2023年）针对深度生成模型驱动的歌声合成（SVS）存在音乐性不足、多语言多风格适配难的问题，提出ExpressiveSinger框架：基于级联扩散模型，通过整合构建多语言多风格歌唱数据集、生成音素时长 / 基频等表现力控制信号、融合风格与音色嵌入生成音频，实现高可控性、高音乐性的跨语言跨风格歌声合成，性能优于现有方案。

- WavTokenizer: An efficient acoustic discrete codec tokenizer for audio language modeling[[paper](https://arxiv.org/pdf/2408.16532)][[code](https://github.com/jishengpeng/WavTokenizer)]
> (2024年) 提出高效的音频离散编码器，支持语音、音乐和通用音频的高质量重建，增强编码中的语义信息

- Neural Codec Language Models are Zero-Shot Text to Speech Synthesizers[[paper](https://arxiv.org/pdf/2301.02111)][[code](https://github.com/microsoft/unilm)]
> (2023年) 首个基于神经编解码语言模型的零样本语音合成系统，将TTS视为条件语言建模任务，通过大规模语音数据预训练实现高质量的零样本语音合成。

- OmniChat: Enhancing Spoken Dialogue Systems with Scalable Synthetic Data for Diverse Scenarios[[paper](https://arxiv.org/pdf/2501.01384)]
> (2025年) 大语言模型驱动的口语对话系统受限于现有数据集规模与场景多样性，难以处理含音频、音乐、情感的复杂真实对话；构建首个大规模多场景口语对话数据集ShareChatX，提出融合异构特征的多轮对话系统OmniChat，探索合成数据训练策略并平衡其与真实数据配比，最终在真实对话数据集 DailyTalk 上取得 SOTA 效果。

- CosyVoice 3: Towards In-the-wild Speech Generation via Scaling-up and Post-training[[paper](https://arxiv.org/pdf/2505.17589)][[code](https://github.com/FunAudioLLM/CosyVoice)]
> (2025年) 专注于零样本野生场景;支持双向流式、超多语言、情感控制、后训练。该模型通过大规模扩展和后训练策略，在内容一致性、说话者相似度和韵律自然度上达到新高度，支持 9 种主流语言（中文、英语、日语、韩语、德语、西班牙语、法语、意大利语、俄语）和 18+ 种汉语方言/口音（如粤语、四川话、上海话）

- SoulX-Podcast: Towards Realistic Long-form Podcasts with Dialectal and Paralinguistic Diversity[[papaer](https://arxiv.org/pdf/2510.23541)][[code](https://github.com/Soul-AILab/SoulX-Podcast)]
> (2025年) 支持零样本声音克隆、多轮多说话者交互、超长时序生成（>90 分钟）和副语言多样性控制。它针对现有 TTS 系统在多说话者连贯性和方言/副语言建模上的局限进行优化，支持中文（普通话）、英语及多种方言（四川话、河南话、粤语）。

- VIBEVOICE Technical Report[[paper](https://arxiv.org/pdf/2508.19205)] [[code](https://github.com/microsoft/VibeVoice)]
> (2025年) 解决传统 TTS 在长形式对话生成上的痛点：现有模型难以维持多说话人一致性、情感表达和上下文连贯，导致播客式输出不自然。该框架通过 next-token 扩散机制实现高效合成，填补了开源 TTS 在多模态对话（语音 + 音乐 + 效果）上的空白。亮点：长形式对话、零-shot 克隆、实时流式、隐式多模态、开源扩展

- HPSU: A Benchmark for Human-Level Perception in Real-World Spoken Speech Understanding[[paper](https://arxiv.org/pdf/2511.23178)][[code](https://github.com/Ichen12/HPSU-Benchmark)]
> (2025年) 语音大语言模型（Speech LLMs）的进展推动了自动语音识别等任务发展，但其在真实口语潜在意图与隐性情感理解上的人类级感知能力尚未被充分探索。为此，研究提出人类级口语理解感知基准（HPSU），其包含 2 万余个中英双语专家验证样本，构建了覆盖基础说话人属性识别至复杂情感意图推理的全面评估框架；同时设计了融合音视频与文本信息的半自动标注流程，解决了数据稀缺与标注成本高的问题。

- ParaS2S: Benchmarking and Aligning Spoken Language Models for Paralinguistic-aware Speech-to-Speech Interaction[[paper](https://arxiv.org/pdf/2511.08723)]
> (2025年) 语音到语音（S2S）模型虽具备一定对话能力，但在处理情感、语气等副语言线索及实现内容与风格适配回应方面仍待探索，高质量示范数据稀缺进一步制约进展。为此，研究提出副语言感知强化学习框架 ParaS2S，可在波形层面优化内容与风格；同步构建 ParaS2SBench 基准，能自动评估模型输出适配性且与人类判断契合。借助该基准的评分反馈，模型通过 GRPO 算法从海量未标注语音中学习。

- SpeakerLM: End-to-End Versatile Speaker Diarization and Recognition with Multimodal Large Language Models[[paper](https://arxiv.org/pdf/2508.06372)]
> (2025年) 说话人区分识别（SDR）任务旨在预测音频片段中 **“何人、何时、说了什么”，是会议转写、对话系统等多说话人真实场景的关键任务。现有 SDR 系统多采用级联框架，整合说话人分轨（SD）与自动语音识别（ASR）模块，但存在误差传播、难以处理重叠语音、无法联合优化两任务协同效应等局限。** 为此，提出统一多模态大语言模型SpeakerLM，以端到端方式联合完成 SD 与 ASR 任务，并嵌入灵活的说话人注册机制以适配多样场景。该模型基于大规模真实数据，采用多阶段训练策略优化。
> 
## 2、语音转文字（**Speech-to-Text, STT**）
基于数据驱动的语音识别任务，核心是利用深度学习模型建立**音频信号序列**到**文本符号序列**的映射关系，实现将连续的语音波形转化为可读的文字内容。

- Natural Language Supervision for General-Purpose Audio Representations[[paper](https://arxiv.org/pdf/2309.05767)][[code](https://github.com/microsoft/CLAP)]
> (2023年) 提出对比学习音频-语言预训练模型，使用在多任务上预训练的音频编码器和自回归文本编码器，在26个下游任务上实现零样本SOTA。

- NaturalSpeech 2: Latent Diffusion Models are Natural and Zero-Shot Speech and Singing Synthesizers[[paper](https://arxiv.org/pdf/2304.09116)][[code](https://speechresearch.github.io/naturalspeech2)]
> (2023年) 针对主流大规模多说话人 TTS 系统韵律不稳、音质差等问题，提出NaturalSpeech 2模型：采用神经音频编解码器与扩散模型生成语音隐向量，结合语音提示机制强化零样本能力；模型基于 4.4 万小时语音和歌唱数据训练，在零样本场景下的韵律、音质等指标大幅超越现有方案，还可实现零样本歌声合成。

# 功能
## 1、语音合成


## 2、语音识别


## 3、语音对话


# 特色
## 1、情感/风格


## 2、副语言
