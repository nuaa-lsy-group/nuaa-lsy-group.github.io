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
>（2025年）大语言模型驱动的口语对话系统受限于现有数据集规模与场景多样性，难以处理含音频、音乐、情感的复杂真实对话；构建首个大规模多场景口语对话数据集ShareChatX，提出融合异构特征的多轮对话系统OmniChat，探索合成数据训练策略并平衡其与真实数据配比，最终在真实对话数据集 DailyTalk 上取得 SOTA 效果。
## 2、语音转文字（**Speech-to-Text, STT**）
基于数据驱动的语音识别任务，核心是利用深度学习模型建立**音频信号序列**到**文本符号序列**的映射关系，实现将连续的语音波形转化为可读的文字内容。

- Natural Language Supervision for General-Purpose Audio Representations[[paper](https://arxiv.org/pdf/2309.05767)][[code](https://github.com/microsoft/CLAP)]
> (2023年) 提出对比学习音频-语言预训练模型，使用在多任务上预训练的音频编码器和自回归文本编码器，在26个下游任务上实现零样本SOTA。

- NaturalSpeech 2: Latent Diffusion Models are Natural and Zero-Shot Speech and Singing Synthesizers[[paper](https://arxiv.org/pdf/2304.09116)][[code](https://speechresearch.github.io/naturalspeech2)]
> (2023年) 针对主流大规模多说话人 TTS 系统韵律不稳、音质差等问题，提出NaturalSpeech 2模型：采用神经音频编解码器与扩散模型生成语音隐向量，结合语音提示机制强化零样本能力；模型基于 4.4 万小时语音和歌唱数据训练，在零样本场景下的韵律、音质等指标大幅超越现有方案，还可实现零样本歌声合成。

## 3、歌声合成（Singing Voice Synthesis, SVS）
面向音乐场景的语音合成延伸技术，核心是利用深度学习模型建立**音乐符号序列（如音符、歌词、节奏）** 到**人声歌唱音频波形**的映射关系，实现兼具**音高准确性、节奏匹配度和情感表现力**的拟人化歌声生成。
- Prompt-Singer: Controllable Singing-Voice-Synthesis with Natural Language Prompt[[paper](https://arxiv.org/pdf/2403.11780)][[code](https://github.com/cyanbx/Prompt-Singer)]
> (2024年) 首个能够用自然语言对歌手性别、音域和音量进行属性控制的SVS方法。

- Opencpop: A High-Quality Open Source Chinese Popular Song Corpus for Singing Voice Synthesis[paper(https://arxiv.org/pdf/2201.07429)][[code](https://wenet.org.cn/opencpop/)]
> (2022年) 提供精细的音素和音符边界标注，并建立基线SVS模型验证数据质量。

- WeSinger 2: Fully Parallel Singing Voice Synthesis via Multi-Singer Conditional Adversarial Training[[paper](https://arxiv.org/pdf/2207.01886)][[demo](https://zzw922cn.github.io/wesinger2)] 
> (2022年) 通过对抗训练策略，产生非常自然且逼真的歌唱声音。

- PERFORMSINGER: MULTIMODAL SINGING VOICE SYNTHESIS LEVERAGING SYNCHRONIZED LIP CUES FROM SINGING PERFORMANCE VIDEOS[[paper](https://arxiv.org/pdf/2509.22718)]
> (2025年) 现有的歌唱声音合成（SVS）模型在很大程度上依赖于细粒度的音素级持续时间，这限制了它们的实际应用。这些方法忽略了视觉信息在持续时间预测中的互补作用。为了解决这些问题，提出PerformSinger，首个多模态SVS框架，它将视频中的嘴唇线索作为一种视觉模态，实现了高质量的“无持续时间”歌唱声音合成并构建首个音频-视觉SVS数据集。

- SingNet: Towards a Large-Scale, Diverse, and In-the-Wild Singing Voice Dataset[[paper](https://arxiv.org/pdf/2505.09325)]
> (2025年) 针对歌声合成、转换等应用缺乏大规模多样化公开数据集的痛点，构建了SingNet野生歌声数据集：通过专用数据处理流程从网络样本库与歌曲中提取数据，形成涵盖多语言多风格的 3000 小时歌声数据；同时基于该数据集预训练并开源 Wav2vec2 等多款 SOTA 模型，开展歌词转录、声码器、歌声转换等任务的基准测试，验证了数据集的有效性。

- Neurodyne: Neural Pitch Manipulation with Representation Learning and Cycle-Consistency GAN[[paper](https://arxiv.org/pdf/2505.15368)]
> (2025年) 针对基于神经网络的音频音调调整系统，因源 - 滤波器模型特征解缠不准确、缺乏配对调谐 / 失调训练数据导致性能受限的问题，提出Neurodyne方案：采用对抗表示学习获取与音调无关的隐表示，解决特征解缠难题；通过循环一致性训练隐式构建配对训练数据。实验表明，该系统在全局调式与模板基音调调整任务中，可提升合成音质，同时有效保留原歌手音色特征。

- LeVo: High-Quality Song Generation with Multi-Preference Alignment[[paper](https://arxiv.org/pdf/2506.07520)][[code](https://github.com/tencent-ailab/songgeneration)]
> (2025年) 针对歌词谱曲生成在音质、音乐性及人声伴奏协调性等方面的不足，提出基于语言模型的LeVo框架：通过双令牌并行建模、双解码器 Transformer 架构及模块化训练保障音轨质量与协调性，结合 DPO 多偏好对齐方法提升指令依从性，实验验证其性能显著优于开源方案，与工业级系统相当。
## 4、戏曲合成
戏曲合成是歌声合成（SVS）技术针对传统戏曲艺术的**定向优化分支**，核心是利用深度学习模型建立**戏曲文本唱词** + **曲谱韵律**到**戏曲唱腔音频波形**的映射关系，生成兼具戏曲腔调、板式韵律和表演风格的拟人化演唱音频。
- FT-GAN: Fine-Grained Tune Modeling for Chinese Opera Synthesis[[paper](https://ojs.aaai.org/index.php/AAAI/article/view/29943)][[code](https://zhengmidon.github.io/FTGAN.github.io/)]
> (2024年) 针对中国戏曲歌声合成（SVS）因缺乏训练数据、难以实现高表现力而研究不足的问题，构建了高质量歌仔戏音文对齐数据集并制定适配中国戏曲的标注方法；基于戏曲与流行歌曲的差异分析，提出用于戏曲精细唱腔建模的声学模型FT-GAN，同时引入语音预训练策略注入额外知识；实验证明该模型在歌仔戏合成任务上优于主流基线模型，且在京剧等其他戏曲合成任务中表现良好。
- Generating Gezi Opera Scores with a Large Language Model and a High-Quality Dataset[[paper](https://ieeexplore.ieee.org/abstract/document/10889420)][[code](https://github.com/ZhenLEI96/GeziOperaDataset)]

> (2025年) 构建142首歌词-旋律对齐的歌仔戏乐谱数据集，提出“三元组数据格式”（歌词、音符、音长）以统一输入长度，使用LLaMA-8B+LoRA进行歌词到旋律生成任务。
- (2025年)HuangmeiSinger: A Dataset and A Branchformer-Diffusion Model for Huangmei Opera Synthesis[[paper](https://dl.acm.org/doi/full/10.1145/3727648.3727752)][[code](https://walkinginthelight.github.io/HuangmeiSinger.github.io/opera/)]

> 针对黄梅戏等传统戏曲歌声合成因缺乏高质量标注数据集与适配模型而受限的问题，开展两项核心工作：一是提出针对性数据标注方法，解决黄梅戏多唱腔标注难题，构建含精细乐谱信息、44.1kHz 高采样率的黄梅戏歌声数据集；二是设计融合 Branchformer 编码器与基频扩散模块的声学模型，适配黄梅戏复杂多样的旋律特征。实验验证了该数据集与模型的有效性。
