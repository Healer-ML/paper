# Healer-ML 研究论文索引

跨模态检索 · 果实计数 · 微表情识别

## 研究方向导航

### 01 · 跨模态检索

图文与多模态检索、遥感图文检索、文本行人检索、组合图像检索及视频文本检索。论文条目包含原题、摘要中文释义、期刊/会议简称、年份和公开代码链接。

**导航：** [专题目录](#cross-modal) · [2021（22篇）](#year-2021) · [2022（27篇）](#year-2022) · [2023（26篇）](#year-2023) · [2024（72篇）](#year-2024) · [2025（93篇）](#year-2025) · [2026（92篇）](#year-2026)

---

### 02 · 果实计数

覆盖开放计数、果园与田间果实计数、浆果计数、遥感/无人机计数、跨帧去重及计数驱动的估产；正式论文与预印本分别标注。

**导航：** [专题首页与年度目录（2021–2026）](papers/fruit-counting.md) · [2021](papers/fruit-counting.md#2021) · [2022](papers/fruit-counting.md#2022) · [2023](papers/fruit-counting.md#2023) · [2024](papers/fruit-counting.md#2024) · [2025](papers/fruit-counting.md#2025)

---

### 03 · 微表情识别

聚焦微表情识别、时空建模、跨数据库泛化，以及数据集、采集设备与帧率信息。

**导航：** [论文目录](papers/micro-expression-recognition.md#论文目录) · [数据集与采集信息](papers/micro-expression-recognition.md#数据集与采集信息) · [专题首页](papers/micro-expression-recognition.md)

---

<a id="cross-modal"></a>

## 跨模态检索 · 年度论文目录

图文、多模态、遥感图文、文本行人、组合图像与视频文本检索。正式出版信息以出版方记录为准，并区分预印本与正式发表版本。最近核对：2026-10-02。

**按年跳转：** [2021 · 22篇](#year-2021) · [2022 · 27篇](#year-2022) · [2023 · 26篇](#year-2023) · [2024 · 72篇](#year-2024) · [2025 · 93篇](#year-2025) · [2026 · 92篇](#year-2026)

---

<details id="year-2021">
<summary>2021 · 22 篇</summary>

### 通用图文检索与匹配 · 9 篇

| 论文题目 | 摘要（中文释义） | 刊会简称 | 代码 |
|---|---|---|---|
| Similarity Reasoning and Filtration for Image-Text Matching | 通过相似度推理和过滤模块建模图文整体关系，抑制不可靠的局部匹配并学习判别性跨模态表示。 | AAAI | [Code](https://github.com/Paranioar/SGRAF) |
| Learning the Best Pooling Strategy for Visual Semantic Embedding | 提出广义池化算子，依据模态和特征自动学习合适的聚合策略，以较低额外开销提升视觉语义检索表示。 | CVPR | [Code](https://github.com/woodfrog/vse_infty) |
| Discrete-continuous Action Space Policy Gradient-based Attention for Image-Text Matching | 将注意力权重直接作为可优化的跨模态投影，通过离散-连续策略梯度学习更适合检索指标的对齐权重。 | CVPR | [Code](https://github.com/Shiyang-Yan/Discrete-continous-PG-for-Retrieval) |
| CoSMo: Content-Style Modulation for Image Retrieval With Text Feedback | 将文本反馈拆解为内容与风格调制信号，联合参考图像和修改文本形成查询，用于迭代式图像检索。 | CVPR | [Code](https://github.com/postBG/CoSMo.pytorch) |
| Cross-Modal Center Loss for 3D Cross-Modal Retrieval | 以跨模态中心损失缩小三维对象不同模态的类内距离、扩大类间间隔，支持大规模三维跨模态检索。 | CVPR | [Code](https://github.com/LongLong-Jing/Cross-Modal-Center-Loss) |
| Deep Adversarial Quantization Network for Cross-Modal Retrieval | 将对抗式表示学习与量化结合，把不同模态映射为紧凑哈希码以支持低存储和快速检索。 | ICASSP | [Code](https://github.com/zhouyu1996/DAQN) |
| Ask&Confirm: Active Detail Enriching for Cross-Modal Retrieval With Partial Query | 面向信息不完整的查询，主动询问并补足具有区分度的细节，再逐步更新跨模态检索结果。 | ICCV | [Code](https://github.com/CuthbertCai/Ask-Confirm) |
| Probabilistic Embeddings for Cross-Modal Retrieval | 用概率分布而非单点向量表示图像和文本，使相似度能够反映表示不确定性和语义歧义。 | CVPR | [Code](https://github.com/naver-ai/pcme) |
| StacMR: Scene-Text Aware Cross-Modal Retrieval | 构建包含场景文字的检索基准，将图像、描述文本与图中文字共同编码，利用 OCR 线索消解视觉相似结果。 | WACV | [Code](https://github.com/AndresPMD/StacMR) |

### 组合图像检索 · 2 篇

| 论文题目 | 摘要（中文释义） | 刊会简称 | 代码 |
|---|---|---|---|
| Compositional Learning of Image-Text Query for Image Retrieval | 提出自编码式组合网络，将参考图像和修改文本组合成查询表示，检索符合用户反馈的目标图像。 | WACV | [Code](https://github.com/ecom-research/ComposeAE) |
| Image Retrieval on Real-Life Images With Pre-Trained Vision-and-Language Models | 提出真实场景组合图像检索任务与 CIRR 基准，使用预训练视觉语言模型融合参考图像和自然语言修改。 | ICCV | [Code](https://github.com/Cuberick-Orion/CIRPLANT) |

### 文本行人检索 · 3 篇

| 论文题目 | 摘要（中文释义） | 刊会简称 | 代码 |
|---|---|---|---|
| Text-Based Person Search with Limited Data | 通过跨模态动量对比扩充小批次监督，并迁移大规模图文数据知识，缓解文本行人检索训练数据有限的问题。 | BMVC | [Code](https://github.com/BrandonHanx/TextReID) |
| Contextual Non-Local Alignment over Full-Scale Representation for Text-Based Person Search | 在多个尺度上联合对齐行人图像区域与文本片段，利用上下文非局部关系增强细粒度文本行人搜索。 | arXiv | [Code](https://github.com/TencentYoutuResearch/PersonReID-NAFS) |
| Semantically Self-Aligned Network for Text-to-Image Part-aware Person Re-identification | 自动提取图像部位与文本短语的语义对应，并用多视角关系和排序损失提升文本行人检索。 | arXiv | [Code](https://github.com/zifyloo/SSAN) |

### 遥感图文检索 · 2 篇

| 论文题目 | 摘要（中文释义） | 刊会简称 | 代码 |
|---|---|---|---|
| Exploring a Fine-Grained Multiscale Method for Cross-Modal Remote Sensing Image Retrieval | 提取遥感影像多尺度显著特征并指导文本表示，缓解空间目标尺度与文本语义粒度不一致。 | TGRS | [Code](https://github.com/xiaoyuan1996/AMFMN) |
| A Lightweight Multi-scale Crossmodal Text-Image Retrieval Method in Remote Sensing | 以轻量多尺度特征交互建模遥感影像与文本的局部语义对应，提升跨模态检索效率和细粒度匹配能力。 | TGRS | [Code](https://github.com/xiaoyuan1996/retrievalSystem) |

### 视频文本检索 · 4 篇

| 论文题目 | 摘要（中文释义） | 刊会简称 | 代码 |
|---|---|---|---|
| Frozen in Time: A Joint Video and Image Encoder for End-to-End Retrieval | 统一图像与视频编码器，并利用图像和视频描述进行联合对比训练，使静态图文预训练知识迁移到端到端视频文本检索。 | ICCV | [Code](https://github.com/m-bain/frozen-in-time) |
| HANet: Hierarchical Alignment Networks for Video-Text Retrieval | 从实体、动作到事件建立层次化视频—文本对齐，兼顾细粒度片段关联与整体语义匹配。 | ACM MM | [Code](https://github.com/Roc-Ng/HANet) |
| TeachText: Cross-Modal Generalized Distillation for Text-Video Retrieval | 集成多个预训练文本编码器作为教师，以跨模态广义蒸馏提升视频与文本嵌入的迁移和检索效果。 | ICCV | [Code](https://www.robots.ox.ac.uk/~vgg/research/teachtext/) |
| Dual Encoding for Video Retrieval by Text | 采用双编码器和混合语义空间进行视频—文本粗到细匹配，在保持检索效率的同时学习互补表示。 | TPAMI | [Code](https://github.com/danieljf24/hybrid_space) |

### 跨模态哈希检索 · 2 篇

| 论文题目 | 摘要（中文释义） | 刊会简称 | 代码 |
|---|---|---|---|
| Deep Graph-neighbor Coherence Preserving Network for Unsupervised Cross-modal Hashing | 以图邻居一致性约束无监督哈希空间，建模跨模态特征之外的潜在语义关系，提升二值检索排序。 | AAAI | [Code](https://github.com/Atmegal/DGCPN) |
| Local Graph Convolutional Networks for Cross-Modal Hashing | 通过局部图卷积保留模态内邻域结构，并将图像与文本映射到紧凑哈希空间以进行跨模态搜索。 | ACM MM | [Code](https://github.com/chenyd7/LGCNH) |

</details>

<details id="year-2022">
<summary>2022 · 27 篇</summary>

### 通用图文检索与匹配 · 2 篇

| 论文题目 | 摘要（中文释义） | 刊会简称 | 代码 |
|---|---|---|---|
| Negative-Aware Attention Framework for Image-Text Matching | 显式利用负样本信息调节区域-词语注意力，减少错误局部关联对图文匹配的干扰。 | CVPR | [Code](https://github.com/CrossmodalGroup/NAAF) |
| Show Your Faith: Cross-Modal Confidence-Aware Network for Image-Text Matching | 为区域-词语匹配估计跨模态置信度，并降低全局语义不一致的局部匹配对最终相似度的影响。 | AAAI | [Code](https://github.com/CrossmodalGroup/CMCAN) |

### 噪声对应鲁棒检索 · 1 篇

| 论文题目 | 摘要（中文释义） | 刊会简称 | 代码 |
|---|---|---|---|
| Deep Evidential Learning with Noisy Correspondence for Cross-Modal Retrieval | 用证据学习估计图文配对可信度，在特征与标签层面建模不确定性，降低错误配对监督的影响。 | ACM MM | [Code](https://github.com/QinYang79/DECL) |

### 组合图像检索 · 2 篇

| 论文题目 | 摘要（中文释义） | 刊会简称 | 代码 |
|---|---|---|---|
| ARTEMIS: Attention-based Retrieval with Text-Explicit Matching and Implicit Similarity | 将组合查询拆分为文本显式匹配和图像隐式相似两路信号，联合排序候选图像。 | ICLR | [Code](https://github.com/naver/artemis) |
| Composed Image Retrieval Using Contrastive Language-Image Pretraining | 利用 CLIP 预训练视觉语言知识，将参考图像与修改文本融合为组合查询，覆盖自然图像及服饰检索。 | CVPR | [Code](https://github.com/ABaldrati/CLIP4Cir) |

### 文本行人检索 · 3 篇

| 论文题目 | 摘要（中文释义） | 刊会简称 | 代码 |
|---|---|---|---|
| See Finer, See More: Implicit Modality Alignment for Text-based Person Retrieval | 以隐式模态对齐和细粒度特征交互缩小行人图像与自然语言描述的差距。 | ECCV Workshop | [Code](https://github.com/TencentYoutuResearch/PersonRetrieval-IVT) |
| A Simple and Robust Correlation Filtering Method for Text-Based Person Search | 通过相关性过滤提取关键线索，并以互斥约束分离身体部位响应，强化文本行人搜索的鲁棒性。 | ECCV | [Code](https://github.com/Suo-Wei/SRCF) |
| Learning Granularity-Unified Representations for Text-to-Image Person Re-identification | 用共享字典和可学习原型统一图像局部特征与文本语义粒度，在共同表示空间检索行人。 | ACM MM | [Code](https://github.com/ZhiyinShao-H/LGUR) |

### 遥感图像与图文检索 · 6 篇

| 论文题目 | 摘要（中文释义） | 刊会简称 | 代码 |
|---|---|---|---|
| Remote Sensing Cross-Modal Text-Image Retrieval Based on Global and Local Information | 联合遥感图像全局和局部多尺度特征，并结合显著性与重排序改善图文双向检索。 | TGRS | [Code](https://github.com/xiaoyuan1996/GaLR) |
| MCRN: A Multi-source Cross-modal Retrieval Network for Remote Sensing | 提出统一多来源遥感检索网络，通过共享模式迁移处理不同数据源之间的语义异质性。 | IJAEOG | [Code](https://github.com/xiaoyuan1996/MCRN) |
| Multisource Data Reconstruction-Based Deep Unsupervised Hashing for Unisource Remote Sensing Image Retrieval | 重构多源数据以学习跨来源共享语义，再生成哈希码服务于单源遥感图像检索。 | TGRS | [Code](https://github.com/sunyuxi/MrHash) |
| Asymmetric Hash Code Learning for Remote Sensing Image Retrieval | 通过非对称哈希学习将查询和图库映射到紧凑编码空间，降低遥感图像大规模检索成本。 | TGRS | [Code](https://github.com/weiweisong415/Demo_AHCL_for_TGRS2022) |
| Meta-hashing for Remote Sensing Image Retrieval | 用元学习适配不同遥感数据分布，并以多哈希码匹配提升跨场景图像检索能力。 | TGRS | [Code](https://github.com/TangXu-Group/Meta-hashing) |
| Unsupervised Contrastive Hashing for Cross-Modal Retrieval in Remote Sensing | 以无监督对比目标学习遥感文本和图像的二值表示，在缺少配对标签时执行跨模态检索。 | arXiv | [Code](https://git.tu-berlin.de/rsim/duch) |

### 视频文本检索 · 10 篇

| 论文题目 | 摘要（中文释义） | 刊会简称 | 代码 |
|---|---|---|---|
| X-CLIP: End-to-End Multi-grained Contrastive Learning for Video-Text Retrieval | 通过跨粒度对比目标连接视频片段与文本，并利用跨帧注意力建模视频内部时序关系。 | ACM MM | [Code](https://github.com/xuguohai/X-CLIP) |
| X-Pool: Cross-Modal Language-Video Attention for Text-Video Retrieval | 以文本条件化的视频注意力池化突出与查询相关的帧信息，形成适用于双向检索的视频表示。 | CVPR | [Code](https://github.com/layer6ai-labs/xpool) |
| TS2-Net: Token Shift and Selection Transformer for Text-Video Retrieval | 通过时序 token 移位和选择压缩视频序列，在降低冗余计算的同时保留有助于图文匹配的动态线索。 | ECCV | [Code](https://github.com/LiuRicky/ts2_net) |
| Lightweight Attentional Feature Fusion: A New Baseline for Text-to-Video Retrieval | 使用轻量注意力融合聚合多层视频和文本特征，为文本搜视频提供高效的跨模态检索基线。 | ECCV | [Code](https://github.com/ruc-aimc-lab/laff) |
| Everything at Once—Multi-modal Fusion Transformer for Video Retrieval | 以统一多模态融合 Transformer 同时利用视频帧、音频及文本上下文，增强复杂视频检索的整体表征。 | CVPR | [Code](https://github.com/ninatu/everything_at_once) |
| Bridging Video-Text Retrieval with Multiple Choice Questions | 将视频—文本匹配改写为多选问答式判别任务，以候选文本对比增强视频检索模型的语义辨别能力。 | CVPR | [Code](https://github.com/TencentARC/MCQ) |
| Visual Consensus Modeling for Video-Text Retrieval | 建模多个视觉片段间的共识信息，并将其用于视频与文本的跨模态相似度估计。 | AAAI | [Code](https://github.com/sqiangcao99/VCM) |
| Improving Video-Text Retrieval by Multi-Stream Corpus Alignment and Dual Softmax Loss | 通过多流语料对齐利用视频帧与文本片段信息，并用双 Softmax 损失校准跨模态匹配分数。 | arXiv | [Code](https://github.com/starmemda/CAMoE) |
| Cross-Lingual Cross-Modal Retrieval with Noise-Robust Learning | 从机器翻译生成的跨语言伪配对中学习，并以多视图自蒸馏缓解翻译噪声对跨语言图文和视频检索的影响。 | ACM MM | [Code](https://github.com/HuiGuanLab/nrccr) |
| A Feature-space Multimodal Data Augmentation Technique for Text-video Retrieval | 在特征空间混合语义相近的视频及描述，扩展训练分布并改善文本—视频检索的泛化能力。 | ACM MM | [Code](https://github.com/aranciokov/FSMMDA_VideoRetrieval) |

### 跨模态哈希检索 · 3 篇

| 论文题目 | 摘要（中文释义） | 刊会简称 | 代码 |
|---|---|---|---|
| Bi-CMR: Bidirectional Reinforcement Guided Hashing for Effective Cross-Modal Retrieval | 以双向强化学习更新跨模态语义关系，减少独立学习标签哈希码带来的偏差，提升图文检索相关性。 | AAAI | [Code](https://github.com/lty4869/Bi-CMR) |
| Differentiable Cross-modal Hashing via Multimodal Transformers | 使用多模态 Transformer 建模图文语义交互，并通过可微哈希学习紧凑二值表示。 | ACM MM | [Code](https://github.com/kalenforn/DCHMT) |
| Deep Adaptively-Enhanced Hashing with Discriminative Similarity Guidance for Unsupervised Cross-modal Retrieval | 以判别性相似度指导无监督哈希表征，并自适应增强跨模态邻域结构以改善检索。 | TCSVT | [Code](https://github.com/reresearcher/DAEH) |

</details>

<details id="year-2023">
<summary>2023 · 26 篇</summary>

### 通用图文检索与匹配 · 5 篇

| 论文题目 | 摘要（中文释义） | 刊会简称 | 代码 |
|---|---|---|---|
| Learning Semantic Relationship among Instances for Image-Text Matching | 以层次关系建模同时捕获片段级和样本级联系，区分语义相近的困难负例并改善图文嵌入。 | CVPR | [Code](https://github.com/CrossmodalGroup/HREM) |
| Fine-Grained Image-text Matching by Cross-modal Hard Aligning Network | 通过跨模态困难对齐网络强化图像区域和文本词语之间的细粒度匹配。 | CVPR | [Code](https://github.com/ppanzx/CHAN) |
| Plug-and-Play Regulators for Image-Text Matching | 以循环对应调节器和聚合调节器反复修正局部对齐与相似度聚合，可插拔地提升图文匹配。 | TIP | [Code](https://github.com/Paranioar/RCAR) |
| Rethinking Benchmarks for Cross-modal Image-text Retrieval | 指出现有基准对细粒度语义区分的评测不足，并构建更细粒度的 MSCOCO-FG 与 Flickr30K-FG 数据集。 | SIGIR | [Code](https://github.com/cwj1412/MSCOCO-Flikcr30K_FG) |
| Image-text Retrieval via Preserving Main Semantics of Vision | 以视觉语义损失突出图像主体语义，减少次要共现内容对图文相似度的干扰，并在标准图文检索基准上验证。 | ICME | [Code](https://github.com/ZhangXu0963/VSL) |

### 噪声对应鲁棒检索 · 4 篇

| 论文题目 | 摘要（中文释义） | 刊会简称 | 代码 |
|---|---|---|---|
| Cross-Modal Active Complementary Learning with Self-refining Correspondence | 挖掘模态互补信息并持续自校正图文对应关系，减少噪声配对导致的过拟合。 | NeurIPS | [Code](https://github.com/QinYang79/CRCL) |
| Cross-Modal Retrieval with Partially Mismatched Pairs | 对部分不匹配图文对建模软对应和可靠关系，减轻错配监督对检索表示的损害。 | TPAMI | [Code](https://github.com/penghu-cs/RCL) |
| BiCro: Noisy Correspondence Rectification for Multi-modality Data via Bi-directional Cross-modal Similarity Consistency | 用双向跨模态相似度一致性发现并校正错误配对，避免单向相似度估计的偏差。 | CVPR | [Code](https://github.com/xu5zhao/BiCro) |
| MSCN: Noisy Correspondence Learning with Meta Similarity Correction | 通过元学习校准跨模态相似度，识别错误图文对应并稳定噪声监督下的匹配学习。 | CVPR | [Code](https://github.com/hhc1997/MSCN) |

### 文本行人检索 · 5 篇

| 论文题目 | 摘要（中文释义） | 刊会简称 | 代码 |
|---|---|---|---|
| Cross-Modal Implicit Relation Reasoning and Aligning for Text-to-Image Person Retrieval | 推理文本属性与行人局部区域的隐式关系，增强全局检索表示而不增加推理开销。 | CVPR | [Code](https://github.com/anosorae/IRRA) |
| RaSa: Relation and Sensitivity Aware Representation Learning for Text-based Person Search | 通过关系感知区分强弱正样本，并检测描述中被替换的词语，提升文本行人搜索鲁棒性。 | IJCAI | [Code](https://github.com/Flame-Chasers/RaSa) |
| CLIP-Driven Fine-grained Text-Image Person Re-identification | 在 CLIP 表示空间中挖掘行人局部身份线索，以跨粒度细化和细粒度对应发现改善图文匹配。 | TIP | [Code](https://github.com/shuanglinyan/CFine) |
| Dual Pseudo-Labels Interactive Self-Training for Semi-Supervised Visible-Infrared Person Re-Identification | 以双伪标签交互自训练利用未标注可见光和红外行人数据，改善跨模态身份检索。 | ICCV | [Code](https://github.com/XiangboYin/DPIS_SSVI-ReID) |
| Towards Unified Text-based Person Retrieval: A Large-scale Multi-Attribute and Language Search Benchmark | 构建 MALS 大规模多属性、自然语言行人检索基准，并以属性—文本联合预训练改善跨数据集文本行人检索。 | ACM MM | [Code](https://github.com/Shuyu-XJTU/APTM) |

### 遥感图文检索 · 6 篇

| 论文题目 | 摘要（中文释义） | 刊会简称 | 代码 |
|---|---|---|---|
| A Prior Instruction Representation Framework for Remote Sensing Image-text Retrieval | 将先验指令表示融入遥感图文检索，以指令语义引导专业描述与影像对齐。 | ACM MM | [Code](https://github.com/Zjut-MultimediaPlus/PIR-pytorch) |
| Parameter-Efficient Transfer Learning for Remote Sensing Image-Text Retrieval | 在预训练 CLIP 中引入轻量遥感多模态适配器和混合对比目标，以较少参数适配领域检索。 | TGRS | [Code](https://github.com/ZhanYang-nwpu/PE-RSITR) |
| Hypersphere-Based Remote Sensing Cross-Modal Text–Image Retrieval via Curriculum Learning | 在超球面空间学习遥感图文特征，并用课程策略逐步安排训练样本难度。 | TGRS | [Code](https://github.com/ZhangWeihang99/HVSA) |
| Reducing Semantic Confusion: Scene-aware Aggregation Network for Remote Sensing Cross-modal Retrieval | 以场景感知聚合组织影像区域和文本语义，减少遥感场景中相近类别造成的混淆。 | ICMR | [Code](https://github.com/jaychempan/SWAN) |
| Knowledge-Aided Momentum Contrastive Learning for Remote-Sensing Image Text Retrieval | 将遥感先验知识融入动量对比学习，改善影像与描述之间的语义匹配。 | TGRS | [Code](https://github.com/mcx-mcx/KAMCL) |
| Interacting-Enhancing Feature Transformer for Cross-Modal Remote-Sensing Image and Text Retrieval | 以特征交互增强 Transformer 建模遥感影像和文本的全局语义与局部关系。 | TGRS | [Code](https://github.com/TangXu-Group/Cross-modal-remote-sensing-image-and-text-retrieval-models/tree/main/IEFT) |

### 组合图像检索 · 1 篇

| 论文题目 | 摘要（中文释义） | 刊会简称 | 代码 |
|---|---|---|---|
| Pic2Word: Mapping Pictures to Words for Zero-shot Composed Image Retrieval | 将参考图像投影为伪词并与修改文本组合，使预训练图文模型无需组合检索三元组也能完成零样本检索。 | CVPR | [Code](https://github.com/google-research/composed_image_retrieval) |

### 视频文本检索 · 1 篇

| 论文题目 | 摘要（中文释义） | 刊会简称 | 代码 |
|---|---|---|---|
| Cap4Video: What Can Auxiliary Captions Do for Text-Video Retrieval? | 利用视频生成的辅助描述扩增训练数据、交互视频与描述特征，并融合文本—视频和文本—描述匹配分数。 | CVPR | [Code](https://github.com/whwu95/Cap4Video) |

### 跨模态哈希检索 · 4 篇

| 论文题目 | 摘要（中文释义） | 刊会简称 | 代码 |
|---|---|---|---|
| Adaptive Marginalized Semantic Hashing for Unpaired Cross-Modal Retrieval | 为非配对跨模态样本自适应学习语义边界与哈希位，支持配对和非配对数据上的检索。 | TMM | [Code](https://github.com/LKYLKYZ/AMSH) |
| Partial Multi-Modal Hashing via Neighbor-aware Completion Learning | 面向模态缺失数据，联合补全缺失内容和邻域语义，再学习适用于跨模态搜索的哈希码。 | TMM | [Code](https://github.com/FutureTwT/NCH) |
| Targeted Adversarial Attack against Deep Cross-modal Hashing Retrieval | 研究针对深度跨模态哈希检索的定向对抗攻击，分析小幅输入扰动对二值编码和检索排序的影响。 | TCSVT | [Code](https://github.com/tswang0116/TA-DCH) |
| Multi-granularity Interactive Transformer Hashing for Cross-modal Retrieval | 以 Transformer 联合建模跨模态粗粒度和细粒度相似性，并通过跨模态交互学习判别哈希码。 | ACM MM | [Code](https://github.com/QinLab-WFU/CLIP-based-Cross-Modal-Hashing) |

</details>

<details id="year-2024">
<summary>2024 · 72 篇</summary>

### 通用图文与混合模态检索 · 4 篇

| 论文题目 | 摘要（中文释义） | 刊会简称 | 代码 |
|---|---|---|---|
| UniIR: Training and Benchmarking Universal Multimodal Information Retrievers | 提出统一多模态检索器和 M-BEIR 基准，使同一模型处理异构图文查询及多种目标模态。 | ECCV | [Code](https://github.com/TIGER-AI-Lab/UniIR) |
| Dynamic Weighted Combiner for Mixed-Modal Image Retrieval | 自适应估计图像与文本在混合查询中的贡献，并用软相似度监督缓解网络文本标签噪声。 | AAAI | [Code](https://github.com/fuxianghuang1/DWC) |
| Composing Object Relations and Attributes for Image-Text Matching | 将目标、属性和关系组合成场景图式语义表示，改善复杂场景中的图文匹配与 Flickr30K/MSCOCO 双向检索。 | CVPR | [Code](https://github.com/vkhoi/cora_cvpr24) |
| Cross-Modal and Uni-Modal Soft-Label Alignment for Image-Text Retrieval | 同时利用跨模态与模态内软标签建模样本关系，缓解漏标正例和假负例对图文检索训练的影响。 | AAAI | [Code](https://github.com/lerogo/aaai24_itr_cusa) |

### 通用多模态检索 · 5 篇

| 论文题目 | 摘要（中文释义） | 刊会简称 | 代码 |
|---|---|---|---|
| VISTA: Visualized Text Embedding For Universal Multi-Modal Retrieval | 将图像信息转化为可与文本编码器交互的视觉 token，并以合成组合数据和分阶段训练构造通用多模态检索表示。 | ACL | [Code](https://github.com/FlagOpen/FlagEmbedding) |
| PreFLMR: Scaling Up Fine-Grained Late-Interaction Multi-modal Retrievers | 构建 M2KR 多模态检索训练与评测套件，并以细粒度 late-interaction 检索器支持图文、图文问答等知识型检索任务。 | ACL | [Code](https://github.com/LinWeizheDragon/Retrieval-Augmented-Visual-Question-Answering) |
| E5-V: Universal Embeddings with Multimodal Large Language Models | 将多模态大语言模型训练为通用嵌入器，通过多任务指令微调和对比学习支持图文及多模态检索。 | arXiv | [Code](https://github.com/kongds/E5-V) |
| MM-Embed: Universal Multimodal Retrieval with Multimodal LLMs | 基于多模态大语言模型构建统一检索嵌入，并用困难负例挖掘提升跨模态及多模态检索能力。 | arXiv | [Code](https://huggingface.co/nvidia/MM-Embed) |
| INQUIRE: A Benchmark for Expert-Level Image Retrieval | 构建面向科学专家的文本搜图基准和大规模相关性标注，评估模型在专业、知识密集型图像检索中的能力。 | NeurIPS D&B | [Code](https://github.com/inquire-benchmark/INQUIRE) |

### 多模态文档检索 · 1 篇

| 论文题目 | 摘要（中文释义） | 刊会简称 | 代码 |
|---|---|---|---|
| Unifying Multimodal Retrieval via Document Screenshot Embedding | 将文档页面截图直接编码为稠密向量，保留页面中的文字、图像和布局信息，避免解析/OCR流程造成的信息损失。 | EMNLP | [Code](https://github.com/texttron/tevatron/tree/main/examples/dse) |

### 视频文本检索 · 9 篇

| 论文题目 | 摘要（中文释义） | 刊会简称 | 代码 |
|---|---|---|---|
| Holistic Features are almost Sufficient for Text-to-Video Retrieval | 通过教师模型蒸馏把多粒度视频—文本知识迁移到整体特征中，以更低的交互成本执行文本搜视频。 | CVPR | [Code](https://github.com/ruc-aimc-lab/TeachCLIP) |
| MV-Adapter: Multimodal Video Transfer Learning for Video Text Retrieval | 在预训练 CLIP 中插入时序适配器，并结合跨模态信息传递，将图像—文本预训练高效迁移到视频文本检索。 | CVPR | [Code](https://github.com/zhangbw17/MV-Adapter) |
| DGL: Dynamic Global-Local Prompt Tuning for Text-Video Retrieval | 动态调整全局与局部提示，联合捕获视频整体语义和片段细节，以适配文本—视频跨模态检索。 | AAAI | [Code](https://github.com/knightyxp/DGL) |
| M2-RAAP: A Multi-Modal Recipe for Advancing Adaptation-based Pre-training towards Effective and Efficient Zero-shot Video-text Retrieval | 通过多模态适配式预训练配方提升零样本文本—视频检索效果，并兼顾参数与推理效率。 | SIGIR | [Code](https://github.com/alipay/Ant-Multi-Modal-Framework/tree/main/prj/M2_RAAP) |
| MPT: Multi-grained Prompt Tuning for Text-Video Retrieval | 在多个语义粒度上学习可训练提示，增强文本与视频整体及局部内容之间的匹配。 | ACM MM | [Code](https://github.com/zchoi/MPT) |
| UMP: Unified Modality-aware Prompt Tuning for Text-Video Retrieval | 以统一且具模态感知能力的提示适配视觉和语言特征，减少模态差异并提升视频文本检索。 | TCSVT | [Code](https://github.com/zchoi/UMP_TVR) |
| Composed Video Retrieval via Enriched Context and Discriminative Embeddings | 将文本修改上下文融入参考视频表示，并学习判别性嵌入以检索符合组合意图的目标视频。 | CVPR | [Code](https://github.com/OmkarThawakar/composed-video-retrieval) |
| Reversed in Time: A Novel Temporal-Emphasized Benchmark for Cross-Modal Video-Text Retrieval | 提出强调时间顺序理解的视频—文本检索基准，评测模型区分时间反转语义的能力并提供相应方法。 | ACM MM | [Code](https://github.com/qyr0403/Reversed-in-Time) |
| WAVER: Writing-Style Agnostic Text-Video Retrieval via Distilling Vision-Language Models through Open-Vocabulary Knowledge | 通过开放词汇视觉语言教师向视频检索学生蒸馏知识，减轻描述写作风格和标注视角差异造成的检索偏差。 | ICASSP | [Code](https://github.com/Fsoft-AIC/WAVER) |

### 部分相关视频文本检索 · 4 篇

| 论文题目 | 摘要（中文释义） | 刊会简称 | 代码 |
|---|---|---|---|
| GMMFormer: Gaussian-Mixture-Model Based Transformer for Efficient Partially Relevant Video Retrieval | 以高斯混合模型表示文本查询与视频片段的相关性分布，并通过 Transformer 高效定位部分相关内容。 | AAAI | [Code](https://github.com/huangmozhi9527/GMMFormer) |
| GMMFormer v2: An Uncertainty-aware Framework for Partially Relevant Video Retrieval | 在部分相关视频检索中显式建模相关性不确定性，以更稳健地聚合相关片段并抑制无关内容。 | arXiv | [Code](https://github.com/huangmozhi9527/GMMFormer_v2) |
| PREM: Improving Video Corpus Moment Retrieval with Partial Relevance Enhancement | 面向视频语料库时刻检索利用部分相关监督，增强文本查询与相关视频片段的定位和排序。 | ICMR | [Code](https://github.com/hdy007007/PREM) |
| BGM-Net: Exploiting Instance-level Relationships in Weakly Supervised Text-to-Video Retrieval | 在弱监督文本搜视频中利用实例级关系传播跨样本信息，缓解视频—文本对应标签不足。 | TOMM | [Code](https://github.com/xjtupanda/BGM-Net) |

### 跨模态哈希检索 · 7 篇

| 论文题目 | 摘要（中文释义） | 刊会简称 | 代码 |
|---|---|---|---|
| Deep Lifelong Cross-modal Hashing | 以持续学习方式逐批更新跨模态哈希模型，在学习新数据时保持旧类别检索能力并减少重复训练。 | TCSVT | [Code](https://github.com/HqiLi/DLCH) |
| Cross-Modal Hashing Method With Properties of Hamming Space: A New Perspective | 从汉明空间性质出发设计语义通道和差异化约束，缓解连续特征到离散码的空间鸿沟。 | TPAMI | [Code](https://github.com/hutt94/SCH) |
| Contrastive Incomplete Cross-Modal Hashing | 针对部分模态缺失的样本，以对比式补全学习恢复跨模态语义并生成可检索哈希码。 | TKDE | [Code](https://github.com/DarrenZZhang/CICH) |
| Deep Neighborhood-Preserving Hashing With Quadratic Spherical Mutual Information for Cross-Modal Retrieval | 以二次球面互信息刻画邻居与非邻居差异，并用深度编码器学习保留局部语义结构的跨模态哈希码。 | TMM | [Code](https://github.com/QinLab-WFU/DNpH) |
| Robust Contrastive Cross-modal Hashing with Noisy Labels | 用动态噪声分离器筛选可信跨模态关系，并以鲁棒对比目标学习噪声标签下稳定的哈希表示。 | ACM MM | [Code](https://github.com/LonganWANG-cs/NRCH) |
| Deep Semantic-Aware Proxy Hashing for Multi-Label Cross-Modal Retrieval | 以语义代理和多标签监督构造紧凑哈希表示，联合利用实例关系与类别级信息进行跨模态检索。 | TCSVT | [Code](https://github.com/QinLab-WFU/DSPH) |
| Deep Class-guided Hashing for Multi-label Cross-modal Retrieval | 联合建模样本关系、类别关系及类间结构，减少多标签语义分散并生成更具判别性的跨模态哈希码。 | arXiv | [Code](https://github.com/donnotnormal/DCGH) |

### 噪声对应鲁棒检索 · 8 篇

| 论文题目 | 摘要（中文释义） | 刊会简称 | 代码 |
|---|---|---|---|
| Cross-modal Retrieval with Noisy Correspondence via Consistency Refining and Mining | 通过一致性细化与可靠关系挖掘识别错误图文对应，并利用模态内和跨模态结构降低噪声影响。 | TIP | [Code](https://github.com/XLearning-SCU/2024-TIP-CREAM) |
| One-step Noisy Label Mitigation | 以一步式机制缓解噪声标签对跨模态检索训练的累积影响。 | arXiv | [Code](https://github.com/leolee99/OSA) |
| PC²: Pseudo-Classification Based Pseudo-Captioning for Noisy Correspondence Learning in Cross-Modal Retrieval | 先预测伪类别再生成伪描述，为可疑图文配对提供更稳定的语义监督。 | ACM MM | [Code](https://github.com/alipay/PC2-NoiseofWeb) |
| UGNCL: Uncertainty-Guided Noisy Correspondence Learning for Efficient Cross-Modal Matching | 估计图文配对不确定性并据此选择训练样本，降低噪声匹配学习的计算开销。 | SIGIR | [Code](https://github.com/qxzha/UGNCL) |
| Mitigating Noisy Correspondence by Geometrical Structure Consistency Learning | 联合利用图像空间、文本空间和跨模态几何结构的一致性识别并缓解错误对应。 | CVPR | [Code](https://github.com/MediaBrain-SJTU/GSC) |
| Learning to Rematch Mismatched Pairs for Robust Cross-Modal Retrieval | 为疑似错配图文对重新寻找语义伴侣，恢复训练监督中的匹配关系并提升检索鲁棒性。 | CVPR | [Code](https://github.com/hhc1997/L2RM) |
| Negative Pre-aware for Noisy Cross-modal Matching | 在对比学习前识别不可靠负样本，减少潜在正例被错误当作负例的训练偏差。 | AAAI | [Code](https://github.com/ZhangXu0963/NPC) |
| Integrating Language Guidance into Image-Text Matching for Correcting False Negatives | 利用语言指导发现被标注为负例的潜在相关图文对，缓解基准标注不完整造成的假负例问题。 | TMM | [Code](https://github.com/AAA-Zheng/LG_ITM) |

### 文本行人检索 · 8 篇

| 论文题目 | 摘要（中文释义） | 刊会简称 | 代码 |
|---|---|---|---|
| Noisy-Correspondence Learning for Text-to-Image Person Re-identification | 以多方置信共识筛选可靠文本-行人图像对，并通过对齐损失降低噪声配对影响。 | CVPR | [Code](https://github.com/QinYang79/RDE) |
| Diverse Person: Customize Your Own Dataset for Text-Based Person Search | 提出可定制的文本行人搜索数据生成流程，以生成式方法降低真实行人数据采集和标注成本。 | AAAI | [Code](https://github.com/Vill-Lab/2024-AAAI-DP) |
| UFineBench: Towards Text-based Person Retrieval with Ultra-fine Granularity | 构建超细粒度文本行人检索基准，强调属性级描述与视觉局部证据的精确匹配。 | CVPR | [Code](https://github.com/Zplusdragon/UFineBench) |
| Adaptive Uncertainty-Based Learning for Text-Based Person Retrieval | 以不确定性过滤低置信匹配，并联合粗细粒度对齐与跨模态掩码建模，增强文本行人检索的噪声鲁棒性。 | AAAI | [Code](https://github.com/CFM-MSG/Code-AUL) |
| PLIP: Language-Image Pre-training for Person Representation Learning | 面向行人表示学习开展语言-图像预训练，利用大规模图文语义提升检索和重识别迁移能力。 | NeurIPS | [Code](https://github.com/Zplusdragon/PLIP) |
| MACA: Memory-aided Coarse-to-fine Alignment for Text-based Person Search | 通过记忆辅助的由粗到细对齐，逐步建模文本描述与行人候选之间的匹配关系。 | SIGIR | [Code](https://github.com/suliangxu/MACA) |
| Harnessing the Power of MLLMs for Transferable Text-to-Image Person ReID | 利用多模态大模型为大规模行人图像生成描述，以语言-图像预训练提升文本行人检索的迁移能力。 | CVPR | [Code](https://github.com/MPI-Lab/MLLM4Text-ReID) |
| Adaptive Uncertainty-Based Learning for Text-Based Person Retrieval | 根据样本不确定性调整文本行人检索训练权重，减少歧义描述和困难配对导致的不稳定优化。 | AAAI | [Code](https://github.com/CFM-MSG/Code-AUL) |

### 遥感图文与遥感图像检索 · 10 篇

| 论文题目 | 摘要（中文释义） | 刊会简称 | 代码 |
|---|---|---|---|
| Toward Efficient and Accurate Remote Sensing Image–Text Retrieval With a Coarse-to-Fine Approach | 先粗筛再精排遥感图文候选，兼顾大规模检索效率与细粒度语义匹配。 | GRSL | [Code](https://github.com/ZhWenQian/CFITR) |
| Prior-Experience-based Vision-Language Model for Remote Sensing Image-Text Retrieval | 将视觉语言模型的先验经验适配遥感领域，增强遥感影像与专业描述之间的检索匹配。 | TGRS | [Code](https://github.com/TangXu-Group/Cross-modal-remote-sensing-image-and-text-retrieval-models/tree/main/PERSVL) |
| Transcending Fusion: A Multiscale Alignment Method for Remote Sensing Image–Text Retrieval | 通过多尺度对齐建立不同空间尺度目标与文本语义的对应关系，避免依赖单层特征融合。 | TGRS | [Code](https://github.com/TangXu-Group/Cross-modal-remote-sensing-image-and-text-retrieval-models/tree/main/MSA) |
| Cross-Modal Prealigned Method With Global and Local Information for Remote Sensing Image and Text Retrieval | 联合预对齐和全局-局部信息建模，减轻遥感影像与描述之间的特征错位。 | TGRS | [Code](https://github.com/TangXu-Group/Cross-modal-remote-sensing-image-and-text-retrieval-models/tree/main/CMPAGL) |
| Cross-Modal Remote Sensing Image–Text Retrieval via Context and Uncertainty-Aware Prompt | 以上下文与不确定性感知提示适配遥感图文语义差异和样本可信度变化。 | TNNLS | [Code](https://github.com/TangXu-Group/Cross-modal-remote-sensing-image-and-text-retrieval-models/tree/main/CUP) |
| PriorCLIP: Visual Prior Guided Vision-Language Model for Remote Sensing Image-Text Retrieval | 通过空间和语义视觉先验筛选关键区域并渐进适配视觉语言表示，提升封闭域及开放域遥感图文检索。 | arXiv | [Code](https://github.com/jaychempan/PriorCLIP) |
| RemoteCLIP: A Vision Language Foundation Model for Remote Sensing | 以大规模遥感图文预训练构建领域视觉语言模型，并评估其在检索、分类和定位任务上的迁移能力。 | TGRS | [Code](https://github.com/ChenDelong1999/RemoteCLIP) |
| SIRS: Multi-task Joint Learning for Remote Sensing Foreground-Entity Image–Text Retrieval | 联合学习语义分割和图文检索，以前景实体区域削弱背景干扰并开展多尺度匹配。 | TGRS | [Code](https://github.com/StarBurstStream0/SIRS) |
| Composed Image Retrieval for Remote Sensing | 将组合图像检索扩展到遥感场景，以遥感图像和文本修改共同表达目标检索意图。 | IGARSS | [Code](https://github.com/billpsomas/rscir) |
| Multi-Spectral Remote Sensing Image Retrieval using Geospatial Foundation Models | 利用地理空间基础模型表征多光谱影像，探索其在遥感图像检索中的迁移能力。 | IGARSS | [Code](https://github.com/IBM/remote-sensing-image-retrieval) |

### 组合图像检索 · 16 篇

| 论文题目 | 摘要（中文释义） | 刊会简称 | 代码 |
|---|---|---|---|
| LinCIR: Language-only Training of Zero-shot Composed Image Retrieval | 仅以语言数据训练组合查询投影模块，不依赖带标注的图像-修改文本-目标图三元组。 | CVPR | [Code](https://github.com/naver/lincir) |
| Fine-grained Textual Inversion Network for Zero-Shot Composed Image Retrieval | 将参考图像映射为主体与属性伪词，再与修改文本形成零样本组合查询。 | SIGIR | [Code](https://github.com/iLearn-Lab/SIGIR24-FTI4CIR) |
| MagicLens: Self-Supervised Image Retrieval with Open-Ended Instructions | 自动构造开放式检索指令训练图像检索器，使模型响应多样化自然语言搜索意图。 | ICML | [Code](https://github.com/google-deepmind/magiclens) |
| CompoDiff: Versatile Composed Image Retrieval With Latent Diffusion | 利用潜扩散模型生成组合查询的视觉表示，并将文本修改意图注入参考图像特征。 | TMLR | [Code](https://github.com/navervision/CompoDiff) |
| Bi-directional Training for Composed Image Retrieval via Text Prompt Learning | 通过文本提示学习和双向训练强化组合查询与目标图像的对应关系。 | WACV | [Code](https://github.com/Cuberick-Orion/Bi-Blip4CIR) |
| Candidate Set Re-ranking for Composed Image Retrieval | 利用候选图像间关系对初始召回结果再排序，提升组合图像检索最终排序质量。 | TMLR | [Code](https://github.com/Cuberick-Orion/Candidate-Reranking-CIR) |
| Knowledge-Enhanced Dual-stream Zero-shot Composed Image Retrieval | 通过外部图文数据库补充参考图像属性，并以额外分支将伪词与细粒度文本概念对齐。 | CVPR | [Code](https://github.com/suoych/KEDs) |
| Sentence-level Prompts Benefit Composed Image Retrieval | 学习针对修改描述的句子级提示，将提示与相对文本拼接后复用文本图像检索模型完成组合检索。 | ICLR | [Code](https://github.com/chunmeifeng/SPRC) |
| Visual Delta Generator with Large Multi-modal Models for Semi-supervised Composed Image Retrieval | 在辅助数据中寻找关联图像对，并用多模态大模型生成视觉差异描述，以扩充半监督组合检索训练数据。 | CVPR | [Code](https://github.com/youngkyunJang/VDG) |
| FashionERN: Enhance-and-Refine Network for Composed Fashion Image Retrieval | 先增强组合查询表征，再用修改文本引导局部细化，提升服饰组合检索表现。 | AAAI | [Code](https://github.com/ChenAnno/FashionERN_AAAI2024) |
| Decomposing Semantic Shifts for Composed Image Retrieval | 将修改指令拆分为视觉原型退化和目标语义升级两个步骤，减少模型忽略参考图像的捷径。 | AAAI | [Code](https://github.com/starxing-yuu/SSN) |
| Data Roaming and Quality Assessment for Composed Image Retrieval | 提出大规模 LaSCo 组合检索数据集，并分析查询中图像与文本模态的必要性及冗余性。 | AAAI | [Code](https://github.com/levymsn/LaSCo) |
| Vision-by-Language for Training-Free Compositional Image Retrieval | 用视觉语言模型生成参考图像描述，再借助语言模型按修改意图重写描述，实现免训练组合检索。 | ICLR | [Code](https://github.com/ExplainableML/Vision_by_Language) |
| Context-I2W: Mapping Images to Context-dependent Words for Accurate Zero-Shot Composed Image Retrieval | 根据修改描述选择参考图像中相关视觉信息并映射为上下文伪词，增强零样本组合查询表示。 | AAAI | [Code](https://github.com/Pter61/context-i2w) |
| Improving Composed Image Retrieval via Contrastive Learning with Scaling Positives and Negatives | 通过多模态大模型扩充正样本，并在第二阶段引入静态困难负例以改善组合检索表征空间。 | ACM MM | [Code](https://github.com/BUAADreamer/SPN4CIR) |
| Simple but Effective Raw-Data Level Multimodal Fusion for Composed Image Retrieval | 从原始输入分别构造文本型和视觉型统一查询，再融合两路检索结果以适应不同搜索意图。 | SIGIR | [Code](https://github.com/iLearn-Lab/SIGIR24-DQU-CIR) |

</details>

<details id="year-2025">
<summary>2025 · 93 篇</summary>

### 通用图文检索与匹配 · 9 篇

| 论文题目 | 摘要（中文释义） | 刊会简称 | 代码 |
|---|---|---|---|
| FLAIR: VLM with Fine-grained Language-informed Image Representations | 利用细粒度文本生成局部语言感知视觉表示，支持全图及局部语义驱动的文本搜图和图文检索。 | CVPR | [Code](https://github.com/ExplainableML/flair) |
| Aligning Information Capacity Between Vision and Language via Dense-to-Sparse Feature Distillation for Image-Text Matching | 以密集描述向稀疏文本特征蒸馏信息，提升图文嵌入的信息容量及多视角描述检索能力。 | ICCV | [Code](https://github.com/liuyyy111/d2s-vse) |
| FG-CLIP: Fine-Grained Visual and Textual Alignment | 通过区域级视觉特征和细粒度文本描述增强局部语义对齐，并评测包括图文检索在内的下游任务。 | ICML | [Code](https://github.com/360CVGroup/FG-CLIP) |
| Visual Semantic Description Generation with MLLMs for Image-Text Matching | 利用多模态大模型生成视觉语义描述，联合实例级图文对齐与类别原型约束改善跨域图文匹配和检索。 | arXiv | [Code](https://github.com/Image-Text-Matching/VSD) |
| Compositional Image-Text Matching and Retrieval by Grounding Entities | 将实体和关系区域嵌入融合进图像表示，免训练增强组合式图文匹配，并在 Flickr30K、MSCOCO 检索上验证。 | CVPRW | [Code](https://github.com/madhukarreddyvongala/GroundingCLIP) |
| Beyond General Alignment: Fine-Grained Entity-Centric Image-Text Matching with Multimodal Attentive Experts | 以多模态注意力专家强化实体级视觉—语言交互，提升新闻图文等跨域数据上的细粒度匹配和检索。 | SIGIR | [Code](https://github.com/wangyxxjtu/ETE) |
| FiRE: Enhancing MLLMs with Fine-Grained Context Learning for Complex Image Retrieval | 以细粒度上下文学习和分阶段微调增强多模态大模型，在长文本搜图、对话检索及组合图像检索中提升复杂查询理解。 | SIGIR | [Code](https://github.com/iLearn-Lab/SIGIR25-FIRE) |
| Revolutionizing Text-to-Image Retrieval as Autoregressive Token-to-Voken Generation | 将图像编码为语义化视觉 token，并把文本搜图改写为自回归 token-to-voken 生成，兼顾检索准确率与推理效率。 | SIGIR | [Code](https://github.com/HongruCai/AVG) |
| Diffusion Augmented Retrieval: A Training-Free Approach to Interactive Text-to-Image Retrieval | 以扩散生成的图像补充交互式查询，再联合对话意图与图像语义执行免训练检索，适应逐轮细化的复杂需求。 | SIGIR | [Code](https://github.com/longkukuhi/Diffusion-Agumented-Retrieval) |

### 通用多模态检索 · 6 篇

| 论文题目 | 摘要（中文释义） | 刊会简称 | 代码 |
|---|---|---|---|
| GENIUS: A Generative Framework for Universal Multimodal Search | 将图像和文本编码为模态解耦的离散语义 ID，再由生成式解码器预测目标 ID，统一多种模态检索。 | CVPR | [Code](https://github.com/sung-yeon-kim/GENIUS-CVPR25) |
| MegaPairs: Massive Data Synthesis for Universal Multimodal Retrieval | 自动合成大规模异构多模态检索样本并训练检索模型，扩展通用检索任务覆盖范围。 | ACL | [Code](https://github.com/VectorSpaceLab/MegaPairs) |
| A Combination-based Framework for Generative Text-Image Retrieval: Dual Identifiers and Hybrid Retrieval Strategies | 以顺序与集合式双重图像标识训练生成检索器，并结合稠密重排，在生成式文本搜图中兼顾效率与排序质量。 | SIGIR-AP | [Code](https://github.com/KaipengLi/ComGTIR) |
| VLM2Vec: Training Vision-Language Models for Massive Multimodal Embedding Tasks | 提出 MMEB 基准并用指令化对比训练将视觉语言模型转为通用嵌入器，统一处理图像、文本组合及多种多模态检索任务。 | ICLR | [Code](https://github.com/TIGER-AI-Lab/VLM2Vec) |
| mmE5: Improving Multimodal Multilingual Embeddings via High-quality Synthetic Data | 通过高质量合成多语言图文数据训练多模态嵌入模型，改善跨语言语义匹配与图文检索。 | arXiv | [Code](https://github.com/haon-chen/mmE5) |
| Bridging Modalities: Improving Universal Multimodal Retrieval by Multimodal Large Language Models | 以多模态大语言模型生成与组织跨模态监督，训练通用多模态嵌入器，覆盖图像、视频及视觉文档检索。 | CVPR | [Code](https://huggingface.co/Alibaba-NLP/gme-Qwen2-VL-2B-Instruct) |

### 多模态文档检索 · 5 篇

| 论文题目 | 摘要（中文释义） | 刊会简称 | 代码 |
|---|---|---|---|
| ColPali: Efficient Document Retrieval with Vision Language Models | 直接将文档页面图像编码为多向量表示并用 late interaction 匹配，跳过繁琐文本抽取，同时发布 ViDoRe 视觉文档检索基准。 | ICLR | [Code](https://github.com/illuin-tech/colpali) |
| Recurrence-Enhanced Vision-and-Language Transformers for Robust Multimodal Document Retrieval | 以循环融合单元逐层整合文档中的图像与文本，并利用查询和文档的多层表示开展多模态文档检索。 | CVPR | [Code](https://github.com/aimagelab/ReT) |
| Zero-shot Multimodal Document Retrieval via Cross-Modal Question Generation | 用多模态大模型为文档生成跨模态预问题，再以问题语义建立索引，实现免任务训练的文档检索。 | EMNLP | [Code](https://github.com/yejinc00/PREMIR) |
| PUMA: Layer-Pruned Language Model for Efficient Unified Multimodal Retrieval with Modality-Adaptive Learning | 通过层剪枝、自蒸馏和模态自适应对比学习构造更高效的统一多模态检索器。 | ACM MM | [Code](https://github.com/iLearn-Lab/ACM-MM25-PUMA) |
| ViDoRAG: Visual Document Retrieval-Augmented Generation via Dynamic Iterative Reasoning Agents | 构建视觉文档检索与推理基准，并以混合多模态检索和探索、总结、反思式多代理流程处理复杂文档问题。 | EMNLP | [Code](https://github.com/Alibaba-NLP/ViDoRAG) |

### 视频文本检索 · 13 篇

| 论文题目 | 摘要（中文释义） | 刊会简称 | 代码 |
|---|---|---|---|
| DiscoVLA: Discrepancy Reduction in Vision, Language, and Alignment for Parameter-Efficient Video-Text Retrieval | 同时缩小视觉、语言和对齐三类图像到视频迁移差异，以伪图像描述和图像—视频蒸馏提升参数高效检索。 | CVPR | [Code](https://github.com/LunarShen/DsicoVLA) |
| Learning Audio-Guided Video Representation with Gated Attention for Video-Text Retrieval | 以门控注意力筛除无关音频并融合有用声学线索，同时采用自适应间隔对比损失改善视频—文本对齐。 | CVPR | [Code](https://github.com/BoseungJeong/AVIGATE-CVPR2025) |
| Narrating the Video: Boosting Text-Video Retrieval via Comprehensive Utilization of Frame-Level Captions | 利用帧级生成描述增强视频特征，以查询感知过滤去除错误叙述，并联合视频与叙述相似度进行检索。 | CVPR | [Code](https://github.com/invhun/NarVid) |
| TempMe: Video Temporal Token Merging for Efficient Text-Video Retrieval | 合并冗余视频时序 token，在保留检索相关信息的同时降低视频编码开销。 | ICLR | [Code](https://github.com/LunarShen/TempMe) |
| Learning Fine-Grained Representations through Textual Token Disentanglement in Composed Video Retrieval | 解耦文本 token 的不同语义作用并学习细粒度组合表示，以更好匹配参考视频、修改描述与目标视频。 | ICLR | [Code](https://github.com/May2333/FDCA) |
| Bidirectional Likelihood Estimation with Multi-Modal Large Language Models for Text-Video Retrieval | 利用多模态大语言模型进行双向似然估计，从视频生成文本和由文本匹配视频，增强跨模态相关性判断。 | ICCV | [Code](https://github.com/mvlab/BLiM) |
| T2VParser: Adaptive Decomposition Tokens for Partial Alignment in Text to Video Retrieval | 引入自适应分解 token，将句子和视频拆为可局部匹配的语义单元，以应对跨模态部分对齐。 | ACM MM | [Code](https://github.com/Lilidamowang/T2VParser) |
| HUD: Hierarchical Uncertainty-Aware Disambiguation Network for Composed Video Retrieval | 通过层次化不确定性估计消解组合视频查询歧义，逐步对齐修改意图与视频内容。 | ACM MM | [Code](https://github.com/iLearn-Lab/MM25-HUD) |
| HOVER: Hyperbolic Video-Text Retrieval | 在双曲空间组织视频与文本的层次语义关系，以更适合层级数据的几何表示执行跨模态检索。 | TIP | [Code](https://github.com/shi-rq/HOVER) |
| Text-Video Retrieval with Global-Local Semantic Consistent Learning | 联合约束全局和局部语义的一致性，增强视频片段与文本细节之间的互补对齐。 | TIP | [Code](https://github.com/zchoi/GLSCL) |
| Beyond Simple Edits: Composed Video Retrieval with Dense Modifications | 构建包含密集、多属性修改的组合视频检索任务与数据，并学习对复杂文本编辑敏感的检索表示。 | ICCV | [Code](https://github.com/OmkarThawakar/BSE-CoVR) |
| Q2E: Query-to-Event Decomposition for Zero-Shot Multilingual Text-to-Video Retrieval | 将多语言查询分解为事件级语义单元，借助跨语言对齐实现零样本文本—视频检索。 | IJCNLP-AACL | [Code](https://github.com/dipta007/Q2E) |
| Quantifying and Narrowing the Unknown: Interactive Text-to-Video Retrieval via Uncertainty Minimization | 通过不确定性量化识别查询中的未知信息，并以交互式反馈逐步缩小候选视频范围。 | ICCV | [Code](https://github.com/bingqingzhang/umivr) |

### 视频时刻检索 · 1 篇

| 论文题目 | 摘要（中文释义） | 刊会简称 | 代码 |
|---|---|---|---|
| RefCap: Zero-shot Video Corpus Moment Retrieval Based on Refined Dense Video Captioning | 先生成并细化视频中的密集事件描述，再根据文本相似度从大规模视频语料检索相关时刻，实现零样本视频时刻检索。 | ICASSP | [Code](https://github.com/BUAAPY/RefCap) |

### 部分相关视频文本检索 · 9 篇

| 论文题目 | 摘要（中文释义） | 刊会简称 | 代码 |
|---|---|---|---|
| Enhancing Partially Relevant Video Retrieval with Hyperbolic Learning | 以双曲空间刻画部分相关视频片段的层次语义，并改善文本查询与多片段相关性的匹配。 | ICCV | [Code](https://github.com/lijun2005/ICCV25-HLFormer) |
| Mitigating Semantic Collapse in Partially Relevant Video Retrieval | 分析部分相关视频检索中的语义坍塌现象，并通过结构化约束维持相关与非相关片段的区分。 | NeurIPS | [Code](https://github.com/admins97/MSC_PRVR) |
| ARL: Ambiguity-Restrained Text-Video Representation Learning for Partially Relevant Video Retrieval | 约束查询歧义带来的表示偏移，学习更可靠的文本—视频部分相关性表示。 | AAAI | [Code](https://github.com/gersys/ARL) |
| Towards Efficient Partially Relevant Video Retrieval with Active Moment Discovering | 主动发现与查询相关的视频时刻，避免对整段视频进行冗余计算以提升部分相关检索效率。 | TMM | [Code](https://github.com/songpipi/AMDNet) |
| Enhancing Partially Relevant Video Retrieval with Robust Alignment Learning | 以鲁棒对齐学习处理文本与局部视频片段之间的不完整或有噪对应，提升部分相关检索。 | EMNLP Findings | [Code](https://github.com/zhanglong-ustc/RAL-PRVR) |
| ProPy: Building Interactive Prompt Pyramids upon CLIP for Partially Relevant Video Retrieval | 在 CLIP 上构造交互式多层提示金字塔，以不同语义粒度定位部分相关视频内容。 | EMNLP Findings | [Code](https://github.com/BUAAPY/ProPy) |
| UEM: Uneven Event Modeling for Partially Relevant Video Retrieval | 建模视频中持续时间和语义密度不均的事件片段，提升文本查询对部分相关内容的定位能力。 | ICME | [Code](https://github.com/Sasa77777779/UEM) |
| MamFusion: Multi-Mamba with Temporal Fusion for Partially Relevant Video Retrieval | 结合多路 Mamba 序列建模与时序融合，捕获长视频中的局部事件及其文本相关性。 | ICME | [Code](https://github.com/Vision-Multimodal-Lab-HZCU/MamFusion) |
| Dual Learning with Dynamic Knowledge Distillation and Soft Alignment for Partially Relevant Video Retrieval | 通过双向学习、动态知识蒸馏和软对齐，兼顾全局匹配与局部相关片段检索。 | arXiv | [Code](https://github.com/HuiGuanLab/DL-DKD) |

### 实例级图像检索 · 1 篇

| 论文题目 | 摘要（中文释义） | 刊会简称 | 代码 |
|---|---|---|---|
| Referring Expression Instance Retrieval and A Strong End-to-End Baseline | 提出指代表达实例检索任务和基准，要求从图库中找出并定位文本所指的具体对象实例。 | ACM MM | [Code](https://github.com/haoxiangzhao12138/REIR) |

### 跨模态哈希检索 · 7 篇

| 论文题目 | 摘要（中文释义） | 刊会简称 | 代码 |
|---|---|---|---|
| Deep Probabilistic Binary Embedding via Learning Reliable Uncertainty for Cross-Modal Retrieval | 以贝叶斯编码器和拉普拉斯近似估计二值嵌入不确定性，处理语义歧义并提升跨模态哈希检索可靠性。 | ACM MM | [Code](https://github.com/QinLab-WFU/DPBE) |
| Deep Discriminative Boundary Hashing for Cross-modal Retrieval | 通过边界保持与类别级量化约束拉开语义类别的汉明距离，改善跨模态哈希码的区分性。 | TCSVT | [Code](https://github.com/QinLab-WFU/DDBH) |
| Deep Semantic-Consistent Penalizing Hashing for Cross-Modal Retrieval | 以语义一致性惩罚约束不同模态的二值表示，减少量化过程中的语义偏移。 | TMM | [Code](https://github.com/QinLab-WFU/DScPH) |
| Multi-scale Consistency Deep Lifelong Cross-modal Hashing | 面向连续到来的数据，通过多尺度跨模态一致性和持续学习机制兼顾新知识适应与旧知识保持。 | TOMM | [Code](https://github.com/HqiLi/MCDLCH) |
| Deep adaptive gradient-triplet hashing for cross-modal retrieval | 根据三元组难度自适应调整梯度，并分阶段优化语义相似性和正交量化以减轻哈希压缩损失。 | ESWA | [Code](https://github.com/QinLab-WFU/OUR-DAGtH) |
| Deep neighbor-coherence hashing with discriminative sample mining for supervised cross-modal retrieval | 联合样本、类别和邻域语义关系，并挖掘困难样本增强监督式跨模态哈希判别能力。 | ESWA | [Code](https://github.com/QinLab-WFU/DNcH) |
| Deep Semantic Tuplet-based Hashing by Hypergraph Modeling for Cross-modal Retrieval | 以超图构造多样本语义元组关系，学习更丰富的高阶标签结构并生成跨模态哈希码。 | TMM | [Code](https://github.com/QinLab-WFU/DSTH) |

### 噪声对应鲁棒检索 · 6 篇

| 论文题目 | 摘要（中文释义） | 刊会简称 | 代码 |
|---|---|---|---|
| Seeking Proxy Point via Stable Feature Space for Noisy Correspondence Learning | 在稳定特征空间寻找代理点，降低噪声图文对应引起的特征偏移。 | IJCAI | [Code](https://github.com/C-TeaRanger/SPS) |
| UCPM: Uncertainty-Guided Cross-Modal Retrieval With Partially Mismatched Pairs | 以不确定性估计定位部分错配样本，并自适应降低其对跨模态检索训练的影响。 | TIP | [Code](https://github.com/qxzha/UCPM) |
| ReCon: Enhancing True Correspondence Discrimination through Relation Consistency for Robust Noisy Correspondence Learning | 利用跨样本关系一致性区分真实匹配与噪声配对，弥补只看单对相似度的局限。 | CVPR | [Code](https://github.com/qxzha/ReCon) |
| Unlearning the Noisy Correspondence Makes CLIP More Robust | 遗忘由错误图文配对建立的有害关联，提升 CLIP 在噪声监督下的跨模态检索稳定性。 | ICCV | [Code](https://github.com/hhc1997/NCU) |
| Noise Self-Correction via Relation Propagation for Robust Cross-Modal Retrieval | 在样本邻域传播关系并自校正噪声对应，以结构信息补充单对匹配监督。 | ACM MM | [Code](https://github.com/njustkmg/MM25-GLP) |
| Learning with Noisy Triplet Correspondence for Composed Image Retrieval | 显式建模组合检索三元组中的语义错配，学习对噪声查询更稳健的组合表示。 | CVPR | [Code](https://github.com/li-shuxian/TME) |

### 组合图像检索 · 14 篇

| 论文题目 | 摘要（中文释义） | 刊会简称 | 代码 |
|---|---|---|---|
| MAI: A Multi-turn Aggregation-Iteration Model for Composed Image Retrieval | 通过多轮聚合和迭代细化组合查询，逐步融合参考图像与修改文本信息。 | ICLR | [Code](https://github.com/PKU-ICST-MIPL/MAI_ICLR2025) |
| Imagine and Seek: Improving Composed Image Retrieval with an Imagined Proxy | 生成与图文组合查询相符的代理图像，以代理表征补充组合检索中的细粒度视觉语义。 | CVPR | [Code](https://github.com/LeyRio/Imagine-and-Seek) |
| Missing Target-Relevant Information Prediction with World Model for Accurate Zero-Shot Composed Image Retrieval | 用潜在世界模型预测参考图像缺失的目标相关内容，再映射为伪词以改善零样本组合检索。 | CVPR | [Code](https://github.com/Pter61/predicir) |
| Composed Image Retrieval for Training-Free Domain Conversion | 以冻结视觉语言模型和离散文本反演执行免训练检索，将图像内容转换到文本指定的目标域。 | WACV | [Code](https://github.com/NikosEfth/freedom) |
| Reason-before-Retrieve: One-Stage Reflective Chain-of-Thoughts for Training-Free Zero-Shot Composed Image Retrieval | 在检索阶段显式推理参考图像和修改文本的组合意图，免除任务专属训练。 | CVPR | [Code](https://github.com/Pter61/osrcir) |
| Generative Zero-Shot Composed Image Retrieval | 先依据图像和修改文本生成组合目标的代理图像，再用代理图像执行零样本检索。 | CVPR | [Code](https://github.com/lan-lw/ComposedImageGen) |
| Slot Inversion for Asymmetric Composed Image Retrieval | 通过槽位反演建模参考图像与修改文本的非对称贡献，适配两种模态作用不均的组合检索。 | ICME | [Code](https://github.com/JThuge/Slot4ACir) |
| Fine-Grained Zero-Shot Composed Image Retrieval with Complementary Visual-Semantic Integration | 组合参考图像的伪 token、修改文本、候选新增物体及生成描述，整合互补视觉与语义证据完成零样本检索。 | ICDM | [Code](https://github.com/yyc6631/CVSI) |
| ConText-CIR: Learning from Concepts in Text for Composed Image Retrieval | 将修改文本中的概念短语与参考图像区域显式对应，减轻复杂编辑描述中的语义干扰并提升组合图像检索。 | CVPR | [Code](https://github.com/mvrl/ConText-CIR) |
| MA-CIR: A Multimodal Arithmetic Benchmark for Composed Image Retrieval | 构建覆盖属性添加、替换、否定和复杂组合操作的多模态算术基准，检验模型按文本编辑意图检索目标图像的能力。 | ICCV | [Code](https://github.com/jaeseokbyun/MACIR) |
| VQA4CIR: Boosting Composed Image Retrieval with Visual Question Answering | 以视觉问答一致性重排候选图像，检查候选结果是否满足修改文本表达的组合意图。 | AAAI | [Code](https://github.com/chunmeifeng/VQA4CIR) |
| Instance-Level Composed Image Retrieval | 提出实例级组合图像检索基准和免训练基线，要求系统结合参考实例图像与修改文本检索目标。 | NeurIPS | [Code](https://github.com/billpsomas/icir) |
| PAIR: Complementarity-guided Disentanglement for Composed Image Retrieval | 根据图像与修改文本的互补性解耦组合查询表征，缓解语义纠缠并提高目标图像匹配精度。 | ICASSP | [Code](https://github.com/iLearn-Lab/ICASSP25-PAIR) |
| good4cir: Generating Detailed Synthetic Captions for Composed Image Retrieval | 以视觉语言模型分阶段生成对象级描述和图像差异指令，构建更细致的组合检索训练数据与跨域基准。 | CVPRW | [Code](https://github.com/SLUVisLab/good4cir) |

### 文本行人与组合行人检索 · 13 篇

| 论文题目 | 摘要（中文释义） | 刊会简称 | 代码 |
|---|---|---|---|
| Chat-based Person Retrieval via Dialogue-Refined Cross-Modal Alignment | 利用多轮对话补充行人属性并细化文本意图，通过对话引导的跨模态对齐定位目标行人。 | CVPR | [Code](https://github.com/Flame-Chasers/DiaNA) |
| Gradient-Attention Guided Dual-Masking Synergetic Framework for Robust Text-based Person Retrieval | 依据梯度注意力实施双重掩码，抑制噪声描述并突出身份判别性图像和文本区域。 | EMNLP | [Code](https://github.com/Multimodal-Representation-Learning-MRL/GA-DMS) |
| Human-centered Interactive Learning via MLLMs for Text-to-Image Person Re-identification | 在测试时通过多模态大模型围绕行人属性进行交互式问答以细化查询，并用描述重组增强训练文本。 | CVPR | [Code](https://github.com/QinYang79/ICL) |
| Modeling Thousands of Human Annotators for Generalizable Text-to-Image Person Re-identification | 建模不同标注者的描述习惯，合成多样化行人文本并提升跨数据集文本行人检索泛化能力。 | CVPR | [Code](https://github.com/sssaury/HAM) |
| Beyond Walking: A Large-Scale Image-Text Benchmark for Text-based Person Anomaly Search | 构建图文行人异常搜索基准，研究利用文本描述从大规模图库检索异常或特定行人。 | ICCV | [Code](https://github.com/Shuyu-XJTU/CMP) |
| Automatic Synthetic Data and Fine-grained Adaptive Feature Alignment for Composed Person Retrieval | 提出自动合成组合行人检索数据和细粒度自适应对齐方法，并发布 ITCPR 评测基准。 | NeurIPS | [Code](https://github.com/Delong-liu-bupt/Composed_Person_Retrieval) |
| Multilingual Text-to-Image Person Retrieval via Bidirectional Relation Reasoning and Alignment | 通过双向关系推理对齐多语言行人描述与视觉区域，支持跨语言文本行人检索。 | TPAMI | [Code](https://github.com/Flame-Chasers/Bi-IRRA) |
| AEA-FIRM: Adaptive Elastic Alignment With Fine-Grained Representation Mining for Text-Based Aerial Pedestrian Retrieval | 以弹性对齐和细粒度表征挖掘处理航拍视角下行人与文本属性之间的差异。 | TCSVT | [Code](https://github.com/xbdxwyh/AEA-FIRM-main) |
| Visual Perturbation for Text-Based Person Search | 通过视觉扰动训练增强模型面对遮挡、外观变化和局部干扰时的鲁棒性，并执行文本到行人图像搜索。 | AAAI | [Code](https://github.com/PatrickZad/ViPer) |
| DM-Adapter: Domain-Aware Mixture-of-Adapters for Text-Based Person Retrieval | 以领域感知的适配器混合与路由实现参数高效迁移，增强细粒度文本行人检索的跨域能力。 | AAAI | [Code](https://github.com/Liu-Yating/DM-Adapter) |
| FRNS: A Dual-Strategy Framework for Fine-Grained Feature Refinement and Text Noise Suppression in Text-Based Person Retrieval | 通过前景细粒度特征细化和文本噪声抑制模块，降低背景及描述噪声对行人图文排序的影响。 | TBIOM | [Code](https://github.com/ShijuanHuang/FRNS) |
| UP-Person: Unified Parameter-Efficient Transfer Learning for Text-Based Person Retrieval | 统一组合 Prefix、LoRA 与 Adapter 参数高效迁移策略，以少量可训练参数适配文本行人检索。 | TCSVT | [Code](https://github.com/Liu-Yating/UP-Person) |
| CAMeL: Cross-Modality Adaptive Meta-Learning for Text-Based Person Retrieval | 以跨模态元学习适应合成文本域，并结合错误记忆和自适应双速率更新改善跨域文本行人检索。 | TIFS | [Code](https://github.com/Jahawn-Wen/CAMeL-reID) |

### 遥感图文检索 · 9 篇

| 论文题目 | 摘要（中文释义） | 刊会简称 | 代码 |
|---|---|---|---|
| Fine-Grained Visual-Language Alignment for Remote Sensing Image–Text Retrieval | 结合粗粒度对比目标与细粒度空间掩码损失，对齐遥感图像 patch 和文本实体。 | TGRS | [Code](https://github.com/Ji-Haoyang/FGVLA) |
| MSSA: A Multi-Scale Semantic-Aware Method for Remote Sensing Image–Text Retrieval | 通过双分支编码、语义感知交互和多尺度融合建模遥感目标与描述词的对应关系。 | Remote Sens. | [Code](https://github.com/LiaoYun0x0/MSSA) |
| A Resource-Efficient Training Framework for Remote Sensing Text-Image Retrieval | 以资源高效训练策略降低遥感图文检索的训练负担，并在公开遥感图文基准上评测。 | arXiv | [Code](https://github.com/ZhangWeihang99/CMER) |
| Self-Supervised Cross-Modal Text-Image Time Series Retrieval in Remote Sensing | 提出双时相遥感影像与文本之间的自监督双向检索，并以全局融合和时序 Transformer 建模变化信息。 | arXiv | [Code](https://git.tu-berlin.de/rsim/cross-modal-text-tsir) |
| PR-CLIP: Cross-Modal Positional Reconstruction for Remote Sensing Image–Text Retrieval | 以跨模态位置重建显式学习文本实体、空间关系和图像区域的对应关系，提升遥感图文检索的细粒度定位能力。 | Remote Sens. | [Code](https://github.com/ADMIS-TONGJI/PR-CLIP) |
| Efficient Yet Effective: A Dynamic Self-Distillation Framework for Remote Sensing Image-Text Retrieval | 通过动态教师自蒸馏保存预训练语义关系，以较少训练数据提升遥感图文检索效果和数据效率。 | GRSL | [Code](https://github.com/zzl0107/DSD-RSITR) |
| SARCLIP: The First Vision-Language Foundation Model for SAR Image | 构建面向合成孔径雷达的视觉语言基础模型与图文数据集，并评测图像—文本检索等下游任务。 | TGRS | [Code](https://github.com/CAESAR-Radi/SARCLIP) |
| Multi-Perspective Subimage CLIP with Keyword Guidance for Remote Sensing Image-Text Retrieval | 用关键词引导生成遥感子视角图像，并以轻量适配器聚合多视角局部线索，提升细粒度遥感图文对齐。 | ICME | [Code](https://github.com/Lcrucial1f/MPS-CLIP) |
| PatternCIR Benchmark and TisCIR: Advancing Zero-Shot Composed Image Retrieval in Remote Sensing | 构建遥感组合图像检索基准，并以图像—文本顺序式跨模态训练利用编辑意图执行零样本遥感检索。 | IJCAI | [Code](https://github.com/captainhvs/TisCIR) |

</details>

<details id="year-2026">
<summary>2026 · 92 篇</summary>

### 噪声对应鲁棒检索 · 6 篇

| 论文题目 | 摘要（中文释义） | 刊会简称 | 代码 |
|---|---|---|---|
| Pseudo-Text Guided Robust Learning for Noisy Correspondence in Cross-Modal Retrieval | 用伪文本识别并修正噪声描述，结合鲁棒对比学习提升高噪声图文检索表现。 | TIP | [Code](https://github.com/shidan0122/PTRL) |
| Robust Semi-paired Multimodal Learning for Cross-modal Retrieval | 联合少量配对样本和大量非配对数据，通过配对语义学习与可靠伪配对挖掘实现半配对检索。 | AAAI | [Code](https://github.com/QinYang79/RCSL) |
| Noisy Correspondence Learning with Modality Gap Direction Correction | 建模样本级图文对齐漂移并校正模态间隙方向，提高噪声对应识别和跨模态检索质量。 | AAAI | [Code](https://github.com/wwyq1/MGCS) |
| Negative Can Be Positive: A Stable and Noise-Resistant Complementary Contrastive Learning for Cross-Modal Matching | 从负样本中挖掘潜在正向信息，以互补对比学习减轻错误负监督的影响。 | Inf. Fusion | [Code](https://github.com/hxy2969/dcl) |
| INTENT: Invariance and Discrimination-aware Noise Mitigation for Robust Composed Image Retrieval | 联合利用不变性和判别性缓解组合检索三元组噪声，区分真实修改意图与数据偏差。 | AAAI | [Code](https://github.com/iLearn-Lab/AAAI26-INTENT) |
| HABIT: Chrono-Synergia Robust Progressive Learning Framework for Composed Image Retrieval | 逐步估计组合语义差异并适配修改幅度，以渐进式学习处理组合检索中的噪声三元组。 | AAAI | [Code](https://github.com/Lee-zixu/HABIT) |

### 通用图文与交互式检索 · 5 篇

| 论文题目 | 摘要（中文释义） | 刊会简称 | 代码 |
|---|---|---|---|
| CAST: Context-Aware Dynamic Latent Space Transformation for Interactive Text-to-Image Retrieval | 根据多轮交互中变化的用户意图动态变换共享潜在空间，捕获细粒度检索意图变化。 | CVPR | [Code](https://github.com/HuiGuanLab/CAST) |
| Beyond Global Similarity: Multi-Conditional Retrieval for Fine-Grained Cross-Modal Understanding | 构建多条件细粒度检索基准，要求候选同时满足图像和文本中的互补约束。 | CVPR | [Code](https://github.com/EIT-NLP/MCMR) |
| PinPoint: Evaluation of Composed Image Retrieval with Explicit Negatives, Multi-Image Queries, and Paraphrase Testing | 以显式困难负例、多图查询和文本改写测试评估组合检索模型的真实相关性判断能力。 | CVPR | [Code](https://github.com/pinterest/pinpoint-dataset) |
| Retrieving Counterfactuals Improves Visual In-Context Learning | 将相似样本检索与属性引导的组合检索结合，为视觉上下文学习寻找有区分度的反事实示例。 | CVPR | [Code](https://github.com/gzxiong/CIRCLES) |
| Camouflage-aware Image-Text Retrieval via Expert Collaboration | 构建伪装场景图文检索数据集，以全局分支与伪装目标专家协同编码，并用置信图注意力融合互补线索。 | CVPR | [Code](https://github.com/jiangyao-scu/CA-ITR) |

### 组合图像检索 · 15 篇

| 论文题目 | 摘要（中文释义） | 刊会简称 | 代码 |
|---|---|---|---|
| Air-Know: Arbiter-Calibrated Knowledge-Internalizing Robust Network for Composed Image Retrieval | 通过仲裁校准并内化检索知识，增强组合查询噪声与语义歧义下的鲁棒性。 | CVPR | [Code](https://github.com/iLearn-Lab/CVPR26-Air-Know) |
| ConeSep: Cone-based Robust Noise-Unlearning Compositional Network for Composed Image Retrieval | 在锥形语义空间分离组合意图并遗忘噪声对应，改善含噪三元组下的检索。 | CVPR | [Code](https://github.com/iLearn-Lab/CVPR26-ConeSep) |
| WISER: Wider Search, Deeper Thinking, and Adaptive Fusion for Training-Free Zero-Shot Composed Image Retrieval | 结合双路候选搜索、置信验证与意图细化，提升免训练零样本组合检索的召回和排序。 | CVPR | [Code](https://github.com/Physicsmile/WISER) |
| ReCALL: Recalibrating Capability Degradation for MLLM-based Composed Image Retrieval | 诊断多模态大模型转为检索器后的细粒度推理退化，并通过纠正样本持续校准检索能力。 | CVPR | [Code](https://github.com/RemRico/Recall) |
| Beyond Semantic Search: Towards Referential Anchoring in Composed Image Retrieval | 提出实例锚定检索设定和基准，要求修改上下文变化时检索结果仍保持指定实例身份一致。 | CVPR | [Code](https://github.com/HaHaJun1101/OACIR) |
| Adapting In-context Generation for Enhanced Composed Image Retrieval | 将上下文生成适配到组合检索，以生成式语义增强参考图像和修改文本形成的查询。 | CVPR | [Code](https://github.com/JThuge/DAIG) |
| Modality and Task Adaptation for Enhanced Zero-shot Composed Image Retrieval | 通过模态与任务适配增强预训练模型对组合查询的理解，在零样本条件下执行组合检索。 | AAAI | [Code](https://github.com/JThuge/MoTa-Adapter) |
| Self-guided Semantic Inspection for Zero-Shot Composed Image Retrieval | 在训练中主动构造图文语义差异，再自适应组合两种模态，以缩小零样本检索的训练-推理差异。 | CVPR | [Code](https://github.com/Orange1999/DiffComp) |
| G-MIXER: Geodesic Mixup-based Implicit Semantic Expansion and Explicit Semantic Re-ranking for Zero-Shot Composed Image Retrieval | 沿球面测地线扩展隐式组合语义，并用显式文本语义重排候选，兼顾零样本检索多样性与准确度。 | CVPR | [Code](https://github.com/maya0395/gmixer) |
| Duplex Rewards Optimization for Test-Time Composed Image Retrieval | 提出测试时组合检索设定，以反事实多项采样扩展候选奖励，并通过双重奖励建模稳定适配无标注查询。 | AAAI | [Code](https://github.com/HaoliangZhou/TT-RLDR) |
| HINT: Composed Image Retrieval with Dual-Path Compositional Contextualized Network | 通过双路上下文编码建模组合查询中的隐式依赖，并放大匹配与非匹配候选间的相似度差异。 | ICASSP | [Code](https://github.com/zh-mingyu/HINT) |
| MELT: Improve Composed Image Retrieval via the Modification Frequentation-Rarity Balance Network | 以稀有语义增强模块突出低频修改意图，并用扩散式相似度去噪减少困难负例导致的排序干扰。 | ICASSP | [Code](https://github.com/luckylittlezhi/MELT) |
| Training-Free Pseudo-Fusion for Composed Image Retrieval with Diffusion Models and Multimodal Large Language Models | 以扩散模型和多模态大语言模型将组合检索改写为单模态检索问题，无需训练专用跨模态融合网络。 | TMLR | [Code](https://github.com/StevenXuf/PeFuse4CIR) |
| Rethinking Composed Image Retrieval Evaluation: A Fine-Grained Benchmark from Image Editing | 通过可控图像编辑构建覆盖五大类、十五子类的细粒度组合检索基准，揭示现有评测集和嵌入模型的能力缺口。 | ACL | [Code](https://github.com/SighingSnow/edir) |
| Heterogeneous Uncertainty-Guided Composed Image Retrieval with Fine-Grained Probabilistic Learning | 分别估计参考图、修改文本质量与跨模态协调不确定性，并以细粒度概率嵌入提升组合检索鲁棒性。 | AAAI | [Code](https://github.com/tanghme0w/AAAI26-HUG) |

### 文本行人检索 · 11 篇

| 论文题目 | 摘要（中文释义） | 刊会简称 | 代码 |
|---|---|---|---|
| Cross-modal Fuzzy Alignment Network for Text-Aerial Person Retrieval and A Large-scale Benchmark | 以模糊匹配估计文本 token 的视觉可靠性，并利用地面图像桥接空中视角，构建空中行人文本检索基准。 | CVPR | [Code](https://github.com/Yifei-AHU/AERI-PEDES) |
| Text-based Aerial-Ground Person Retrieval | 将文本行人检索扩展到空中和地面视角，研究跨视角域差异下的行人搜索。 | AAAI | [Code](https://github.com/Flame-Chasers/TAG-PR) |
| Cross-Resolution Semantic Transfer for Robust Text-to-Image Person Retrieval | 在混合分辨率图库中迁移高分辨率语义证据并对齐排序分布，增强低清行人检索鲁棒性。 | ACM MM | [Code](https://github.com/AKADOUQ/CRST-Cross-Resolution-Semantic-Transfer-for-Robust-Text-to-Image-Person-Retrieval) |
| Tackling Alignment Ambiguity in Person Retrieval through Conversational Attribute Mining | 通过多模态对话挖掘行人属性，并以双向跨注意力和置信加权缓解图文细粒度对齐歧义。 | CVPR | [Code](https://github.com/sugelamyd123/CECA) |
| Pretrain-then-Adapt: Uncertainty-Aware Test-Time Adaptation for Text-based Person Search | 在测试阶段依据不确定性适配文本行人检索模型，降低目标图库分布变化导致的性能退化。 | SIGIR | [Code](https://github.com/nkuzjh/UATTA) |
| Cross-Modal Full-Mode Fine-Grained Alignment for Text-to-Image Person Retrieval | 以完整模态的细粒度证据对齐文本描述与行人图像，改善局部属性匹配。 | TOMM | [Code](https://github.com/yinhao1102/FMFA) |
| Generative Retrieval for Unsupervised Text-Based Person Search | 先生成候选行人描述再进行置信度加权检索，在无监督设定下利用合成语言监督支持文本行人搜索。 | TPAMI | [Code](https://github.com/Flame-Chasers/GTR) |
| Cross-Modal Person Retrieval with One-to-Many Relation Modeling | 以一对多关系刻画同一行人的多种文本描述与视觉表现，改善跨模态行人特征学习和检索排序。 | TIFS | [Code](https://github.com/Yifei-AHU/OMRE) |
| Interactive Person Retrieval via Multi-Turn Multimodal Conversation | 将单轮文本搜人扩展为多轮多模态对话检索，以逐轮编码和对话记忆聚合补足模糊查询中的身份细节。 | ICML | [Code](https://github.com/Flame-Chasers/MNEMO) |
| Unsupervised Cross-Modal Person Search via Text Style Normalization | 通过大模型生成风格统一的行人描述，并融合图文相似度与多模态聚类，在无标注场景下学习跨模态行人检索。 | Image Vis. Comput. | [Code](https://github.com/flychen321/TSN) |
| Minimizing the Pretraining Gap: Domain-Aligned Text-Based Person Retrieval | 以领域感知扩散合成贴近真实数据的行人图文对，再通过多粒度区域—文本关系对齐缩小预训练与目标域差距。 | Pattern Recogn. | [Code](https://github.com/Shuyu-XJTU/MRA) |

### 遥感图文检索 · 8 篇

| 论文题目 | 摘要（中文释义） | 刊会简称 | 代码 |
|---|---|---|---|
| Towards Discriminative and Consistent Cross-Modal Alignment for Remote Sensing Image–Text Retrieval | 结合判别性表示与一致性约束改善遥感影像和文本对齐，支持遥感图文双向检索。 | Remote Sens. | [Code](https://github.com/ADMIS-TONGJI/DCCA) |
| Robust Remote Sensing Image–Text Retrieval with Noisy Correspondence | 联合建模局部对应和样本关系，在多种噪声配对比例下提升遥感图文检索稳健性。 | CVPR | [Code](https://github.com/MSFLabX/RRSITR) |
| DFPR: Dynamic Fine-Grained Perceptive Bidirectional Image-Text Retrieval | 以实体、属性、关系和量词专家解析文本，并结合谱图滤波和双向校准提升遥感图文细粒度检索。 | ACM MM | [Code](https://github.com/24029100313/DFPR-Dynamic-Fine-Grained-Perceptive-Bidirectional-Image-Text-Retrieval) |
| Multimodal Large Language Models Assisted Hierarchical Image-Caption Fusion for Remote Sensing Image-Text Retrieval | 融合多模态大模型生成的段落、句子和关键词层级描述，通过跨层交互改善遥感影像与文本匹配。 | TMM | [Code](https://github.com/RayzedWang/Caption2CLIP) |
| ReCoTR: Reducing Semantic Cognitive Shift via Dual-Consensus Token Compression for Remote Sensing Image-Text Retrieval | 以跨模态语义共识和模态内结构一致性筛选视觉 token，压缩低置信背景信息以缓解遥感图文检索中的语义漂移。 | TIP | [Code](https://github.com/Jerry710/ReCoTR) |
| From Insufficient to Sufficient: Hierarchical Semantic Alignment for Remote Sensing Image-Text Retrieval | 结合文本语义增强、全局图文对比和选择性细粒度对齐，改善遥感图文特征的信息不平衡。 | ESWA | [Code](https://github.com/hocker-sy/SHSA) |
| Explicit Spatial Localization and Task-Adaptive Balancing for Remote Sensing Image-Text Retrieval | 以显式文本到区域定位和任务自适应平衡提升遥感图文检索的细粒度证据关联与可解释性。 | ISPRS JPRS | [Code](https://github.com/miaomiao101811-ui/SLB-Net) |
| Benchmarking Composed Image Retrieval for Applied Earth Observation | 构建面向地球观测任务的组合图像检索基准，研究图像参考与文本编辑联合表达遥感目标的检索方式。 | arXiv | [Code](https://github.com/billpsomas/rscir) |

### 通用多模态与文档检索 · 22 篇

| 论文题目 | 摘要（中文释义） | 刊会简称 | 代码 |
|---|---|---|---|
| MetaEmbed: Scaling Multimodal Retrieval at Test-Time with Flexible Late Interaction | 以固定数量的可学习元 token 生成紧凑多向量表示，在细粒度匹配能力与大规模检索成本之间灵活权衡。 | ICLR | [Code](https://github.com/facebookresearch/MetaEmbed) |
| RMIR: A Benchmark Dataset for Reasoning-Intensive Multimodal Image Retrieval | 构建强调功能、时间和因果推理的多模态图像检索基准，用于衡量模型超越表面相似度的检索能力。 | CVPR | [Code](https://github.com/amazon-science/rmir) |
| ReMatch: Boosting Representation through Matching for Multimodal Retrieval | 将生成式匹配目标作为辅助训练信号，并学习多向量表示以增强多模态检索特征的判别性。 | CVPR | [Code](https://github.com/FireRedTeam/ReMatch) |
| CMDR: Contextual Multimodal Document Retrieval | 建立多页文档检索任务，使模型利用跨页上下文和间接语义关联定位相关页面，而不局限于单页相似度。 | ECCV | [Code](https://github.com/nttmdlab-nlp/CMDR-Bench) |
| VIRTUE: Visual-Interactive Text-Image Universal Embedder | 通过视觉—文本交互构造统一嵌入空间，并以多阶段训练支持文本搜图、图搜图及组合图像检索。 | ICLR | [Code](https://github.com/sony/virtue) |
| U-MARVEL: Unveiling Key Factors for Universal Multimodal Retrieval via Embedding Learning with MLLMs | 系统分析多模态大语言模型嵌入式检索的关键因素，并通过针对性训练增强通用图文及多模态检索。 | ICLR | [Code](https://github.com/chaxjli/U-MARVEL) |
| VLM2Vec-V2: Advancing Multimodal Embedding for Videos, Images, and Visual Documents | 将视觉语言模型扩展为统一视频、图像和视觉文档嵌入器，并以多任务基准和指令化训练提升跨模态检索能力。 | TMLR | [Code](https://github.com/TIGER-AI-Lab/VLM2Vec) |
| UME-R1: Exploring Reasoning-Driven Generative Multimodal Embeddings | 先以监督微调赋予模型多模态推理与生成式嵌入能力，再通过强化学习进一步优化检索表示和推理质量。 | ICLR | [Code](https://github.com/XMUDeepLIT/UME-R1) |
| ObjEmbed: Towards Universal Multimodal Object Embeddings | 将图像编码为对象区域级及全局嵌入，并结合对象语义相似度和定位质量支持局部、全局图像检索。 | ICML | [Code](https://github.com/WeChatCV/ObjEmbed) |
| Recurrence Meets Transformers for Universal Multimodal Retrieval | 将递归式跨模态融合融入视觉语言 Transformer，形成多层级表示以支持统一多模态检索。 | TPAMI | [Code](https://github.com/aimagelab/ReT-2) |
| ModernVBERT: Towards Smaller Visual Document Retrievers | 以紧凑视觉语言编码器直接理解文档页面，探索更小、更高效的视觉文档检索模型。 | ICML | [Code](https://github.com/illuin-tech/modernvbert) |
| Guided Query Refinement: Multimodal Hybrid Retrieval with Test-Time Optimization | 在测试时迭代优化多模态查询，并结合稠密与稀疏检索信号提升混合检索的相关性。 | ICLR | [Code](https://github.com/IBM/test-time-hybrid-retrieval) |
| Bottleneck Tokens for Unified Multimodal Retrieval | 以少量瓶颈 token 压缩并汇聚多模态输入信息，构建更高效的统一检索表示。 | arXiv | [Code](https://github.com/siryuson/BottleneckTokens) |
| Inference-Free Multimodal Learned Sparse Retrieval for Production-Scale Visual Document Search | 将视觉文档转化为可索引的稀疏表示，免去在线多模态模型推理，面向大规模文档搜索降低服务成本。 | arXiv | [Code](https://github.com/naver/v-splade) |
| UniversalRAG: Retrieval-Augmented Generation over Corpora of Diverse Modalities and Granularities | 通过模态感知路由在不同模态和粒度的语料间选择检索源，构建适用于异构多模态语料的检索增强生成流程。 | ACL | [Code](https://github.com/wgcyeo/UniversalRAG) |
| MoCa: Modality-aware Continual Pre-training Makes Better Bidirectional Multimodal Embeddings | 以跨文本—图像联合重建开展模态感知持续预训练，再用异构对比微调扩展训练目标，学习双向通用多模态检索嵌入。 | ACL | [Code](https://github.com/haon-chen/MoCa) |
| VisRet: Visualization Improves Knowledge-Intensive Text-to-Image Retrieval | 先将文本查询生成到图像模态，再进行图像内检索，以绕过跨模态嵌入对姿态、视角等细微视觉关系刻画不足的问题。 | ACL | [Code](https://github.com/xiaowu0162/Visualize-then-Retrieve) |
| MM-BRIGHT: A Multi-Task Multimodal Benchmark for Reasoning-Intensive Retrieval | 构建覆盖 29 个领域、四类检索方向的多模态推理基准，系统评估文本、图像及组合查询检索技术文档的能力。 | arXiv | [Code](https://github.com/mm-bright/MM-BRIGHT) |
| BRIDGE: Multimodal-to-Text Retrieval via Reinforcement-Learned Query Alignment | 以强化学习将图像—文本混合查询改写为面向检索的文本，再用推理增强的稠密检索器查找相关文档。 | arXiv | [Code](https://github.com/mm-bright/multimodal-reasoning-retrieval) |
| MARVEL: Multimodal Adaptive Reasoning-intensive Expand-rerank and Retrieval | 通过多模态查询扩展、召回与重排组成统一流程，改善复杂视觉问题到文本语料的推理型检索。 | arXiv | [Code](https://github.com/mm-bright/multimodal-reasoning-retrieval) |
| VISA-Agent: A Visual Symbolic Agent for Reasoning-Intensive Multimodal Retrieval | 将查询图像解析为结构化符号文本，与原始问题及图像描述形成多路文本查询，再融合检索结果完成多模态搜文档。 | Mathematics | [Code](https://github.com/HarnessLab/VISA-Agent) |
| Multi-Constraint Relational Semantic Alignment Towards Image-Text Retrieval | 以贝叶斯后验约束、动量质心更新和动态尺度适配分别加强细粒度对应、模态一致性及多粒度图文对齐。 | TMM | [Code](https://github.com/xiaoyiseu/McRSA) |

### 视频文本检索 · 8 篇

| 论文题目 | 摘要（中文释义） | 刊会简称 | 代码 |
|---|---|---|---|
| EagleNet: Energy-Aware Fine-Grained Relationship Learning Network for Text-Video Retrieval | 构建文本—帧关系图并建模帧间上下文，以能量感知匹配和 sigmoid 对比目标提升视频文本细粒度检索。 | CVPR | [Code](https://github.com/draym28/EagleNet) |
| Robust Test-time Video-Text Retrieval: Benchmarking and Adapting for Query Shifts | 建立查询分布变化下的视频—文本检索评测，并在测试时自适应更新模型以增强分布外鲁棒性。 | ICLR | [Code](https://github.com/bingqingzhang/vtr_tta) |
| TAME: Temporal-Aware Mixture-of-Experts for Text-Video Retrieval | 采用时间感知专家混合结构建模不同视频片段与文本的匹配，提升跨模态视频检索表现。 | IEEE Access | [Code](https://github.com/sejong-rcv/TAME) |
| Adaptive Multi-Agent Reasoning for Text-to-Video Retrieval | 按查询需求动态编排检索、时序推理与查询改写代理，并利用检索反馈和历史推理轨迹协调复杂视频查询。 | ICMR | [Code](https://github.com/nikkiwoo-gh/multi-agent-retrieval) |
| Dual-Attention Video Representation Learning for Parameter Efficient Text-Video Retrieval | 以双重注意力学习视频全局与局部时序表征，并在较少可训练参数下完成图像预训练模型向文本—视频检索的迁移。 | TMM | [Code](https://github.com/bzy-source/DAVRL) |
| SAVE: Speech-Aware Video Representation Learning for Video-Text Retrieval | 增设语音语义分支，并以软跨模态对齐融合语音、音频和视觉线索，弥补常规视频文本检索忽略音轨的问题。 | CVPR | [Code](https://github.com/ruc-aimc-lab/SAVE) |
| PE2LR: Probabilistic Embeddings With Evidence Learning and Refinement for Text-Video Retrieval | 将视频和文本嵌入建模为概率分布，以证据理论估计匹配不确定性，并通过分布级表征学习和嵌入细化增强跨模态一致性。 | TIP | [Code](https://github.com/rzheng77/PE2LR-text-video-retrieval) |
| Adapting MLLMs for Nuanced Video Retrieval | 仅用文本困难负例对多模态大模型进行对比微调，使统一嵌入处理时间顺序、否定语义及视频加文本编辑等细粒度检索。 | ECCV | [Code](https://github.com/bpiyush/TARA) |

### 持续文本视频检索 · 1 篇

| 论文题目 | 摘要（中文释义） | 刊会简称 | 代码 |
|---|---|---|---|
| StructAlign: Structured Cross-Modal Alignment for Continual Text-to-Video Retrieval | 以类别级 ETF 几何先验对齐文本和视频，并通过跨模态关系保持抑制持续学习中的模态漂移与灾难性遗忘。 | SIGIR | [Code](https://github.com/Mysteriousplayer/SIGIR26-StructAlign) |

### 组合视频检索 · 3 篇

| 论文题目 | 摘要（中文释义） | 刊会简称 | 代码 |
|---|---|---|---|
| ReTrack: Evidence-Driven Dual-Stream Directional Anchor Calibration Network for Composed Video Retrieval | 通过双流方向性锚点校准整合参考视频、文本修改与检索证据，改善组合视频查询的目标定位。 | AAAI | [Code](https://github.com/iLearn-Lab/AAAI26-ReTrack) |
| RELATE: Enhance Composed Video Retrieval via Minimal-Redundancy Hierarchical Collaboration | 解析修改文本的层次结构并稀疏化视频时序特征，减少冗余帧干扰，同时支持组合视频和图像检索。 | ICASSP | [Code](https://github.com/iLearn-Lab/ICASSP26-RELATE) |
| COVA: Text-guided Composed Video Retrieval for Audio-Visual Content | 将文本引导的组合视频检索扩展到音视频内容，结合视听线索与修改指令检索目标视频。 | ICASSP | [Code](https://github.com/PerceptualAI-Lab/CoVA) |

### 视频时刻检索 · 1 篇

| 论文题目 | 摘要（中文释义） | 刊会简称 | 代码 |
|---|---|---|---|
| Beyond Caption-Based Queries in Video Moment Retrieval | 构建更接近真实搜索表达的时刻检索基准，并通过抑制解码器查询坍塌改善欠描述、多时刻查询下的定位泛化。 | CVPR | [Code](https://github.com/davidpujol/Beyond_Caption-Based_Queries_for_Video_Moment_Retrieval) |

### 部分相关视频文本检索 · 6 篇

| 论文题目 | 摘要（中文释义） | 刊会简称 | 代码 |
|---|---|---|---|
| Revisiting Uncertainty: On Evidential Learning for Partially Relevant Video Retrieval | 以证据学习估计视频片段相关性的不确定性，降低不确定匹配对部分相关视频检索的干扰。 | ICML | [Code](https://github.com/lijun2005/ICML26-Holmes) |
| Imagine Before Concentration: Diffusion-Guided Registers Enhance Partially Relevant Video Retrieval | 借助扩散引导的寄存器特征增强视频表示，使模型更准确聚焦查询相关片段。 | CVPR | [Code](https://github.com/lijun2005/CVPR26-DreamPRVR) |
| Bidirectional Cross-Modal Collaborative Alignment via Semantic-Guided Visual Embeddings for Partially Relevant Video Retrieval | 以语义引导视觉嵌入开展双向跨模态协同对齐，强化文本与部分相关视频片段之间的匹配。 | TIP | [Code](https://github.com/cyanlll/BOA) |
| Intrinsic Temporal Adaptation of CLIP for Partially Relevant Video Retrieval | 在 CLIP 表示中引入内在时序适配，使模型能够从整段视频中提取与文本查询相关的局部事件。 | EMNLP | [Code](https://github.com/hynnsk/ITA) |
| A3PRVR: Action-and-object Aware Alignment for Partially Relevant Video Retrieval | 联合动作与物体语义对齐文本查询和视频片段，以更准确检索部分相关视频。 | AAAI | [Code](https://github.com/chuanshen-chen/A3PRVR) |
| CaptAin: Caption-driven Alignment for Bridging Modality Gaps in Partially Relevant Video Retrieval | 利用视频字幕作为桥接线索弥合文本与视觉表征差距，增强局部相关片段的跨模态对齐。 | CVPR Findings | [Code](https://github.com/sYYmmEtra/CaptAin-PRVR) |

### 跨模态哈希检索 · 6 篇

| 论文题目 | 摘要（中文释义） | 刊会简称 | 代码 |
|---|---|---|---|
| Polysemic Semantic Instance Network for Cross-Modal Hashing | 以多语义实例表示保留样本的多义语义结构，避免单一类别表示造成的信息损失并改善跨模态哈希检索。 | AAAI | [Code](https://github.com/QinLab-WFU/DPSIH) |
| Deep Distance Weighted Sampling Hashing for Cross-modal Retrieval | 以距离加权采样突出信息量更高的跨模态样本对，增强紧凑二值表示的判别性。 | TMM | [Code](https://github.com/QinLab-WFU/DDWSH) |
| Hub-Removal Sparse Hashing for Cross-Modal Retrieval | 通过稀疏哈希和 hubness 抑制减少高频中心样本对近邻排序的偏置，提高跨模态检索效率与准确性。 | TCSVT | [Code](https://github.com/hutt94/HRSH) |
| Deep Discriminative Structure Proxy Hashing for Cross-modal Retrieval | 以结构化语义代理组织类别关系，并对比正负响应学习更清晰的汉明空间决策边界。 | ICML | [Code](https://github.com/QinLab-WFU/DDSPH) |
| Deep Global-sense Hard-negative Discriminative Generation Hashing for Cross-modal Retrieval | 通过图关系传播捕获全局样本结构，并自适应生成语义一致的困难负例，强化跨模态哈希空间的判别边界。 | ICLR | [Code](https://github.com/QinLab-WFU/DGHDGH) |
| Deep Uncertainty-aware Probabilistic Hashing for Cross-modal Retrieval | 以概率哈希建模输入质量和语义歧义带来的不确定性，避免不完整或退化模态造成二值表示偏移。 | TOMM | [Code](https://github.com/QinLab-WFU/DUaPH) |

</details>
