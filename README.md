<div align="center">
<h1>Healer-ML 研究论文库</h1>
<p><strong>Research Paper Library · 2021–2026</strong></p>
<p><a href="#cross-modal">跨模态检索</a>　·　<a href="#fruit-counting">果实计数</a>　·　<a href="#micro-expression">微表情识别</a></p>
</div>

---

<a id="cross-modal"></a>
## 01 · 跨模态检索

**专题导航：** [跨模态对齐中的负样本抑制](papers/negative-sample-suppression.md)（假负样本、噪声对应与代码核验）

<details>
<summary><strong>展开年度论文目录 · 332 篇（2021–2026）</strong></summary>

**按年直达：** [2021 · 22篇](#year-2021) · [2022 · 27篇](#year-2022) · [2023 · 26篇](#year-2023) · [2024 · 72篇](#year-2024) · [2025 · 93篇](#year-2025) · [2026 · 92篇](#year-2026)


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

</details>

---

<a id="fruit-counting"></a>
## 02 · 果实计数

<details>
<summary><strong>展开果实计数目录 · 165 篇（农业、遥感、开放/类无关及相关基准，2021–2026）</strong></summary>

**分类导航：** [农业果实计数目录](papers/fruit-counting.md) · [各方向数据集与下载状态](papers/fruit-counting.md#datasets-by-direction) · [遥感/航拍计数](papers/counting-research.md#remote-sensing-counting) · [开放词汇/开放世界计数](papers/counting-research.md#open-vocabulary-counting) · [类无关/少样本计数](papers/counting-research.md#class-agnostic-counting) · [视频计数](papers/counting-research.md#video-counting) · [数据集与评测基准](papers/counting-research.md#counting-benchmarks)

**完整逐篇清单：** [论文摘要、刊会/年份与代码核验](papers/counting-research.md)

**按年直达：** [2021 · 8 篇](#fruit-year-2021) · [2022 · 16 篇](#fruit-year-2022) · [2023 · 19 篇](#fruit-year-2023) · [2024 · 32 篇](#fruit-year-2024) · [2025 · 44 篇](#fruit-year-2025) · [2026 · 46 篇](#fruit-year-2026)

表格统一按发表年份折叠；**类别写在摘要开头**（农业果实、遥感、开放词汇、类无关/少样本、视频或基准），不另建分类论文表。农业果实原有 74 篇仍全部保留；跨领域论文按正式发表年份并入下方对应年度表。代码栏只链接论文/作者关联的实现或资源，并注明仅数据集、部分实现及未确认代码等状态。

<details id="fruit-year-2021">

<summary>2021 · 8 篇</summary>

<details>
<summary>农业果实计数与果园估产 · 6 篇</summary>

| 论文题目 | 摘要（中文释义） | 刊会简称 | 代码 |
| --- | --- | --- | --- |
| [Fruit detection and load estimation of an orange orchard using the YOLO models through simple approaches in different imaging and illumination conditions](https://www.sciencedirect.com/science/article/pii/S0168169921005500) | 用 YOLO 在自然橙园图像中检测并汇总果数，比较成像与光照条件，验证果数和估产相关性。（范围：A/B） | CEA | 未核验 |
| [Design, development, and performance evaluation of a robot for yield estimation of kiwifruit](https://www.sciencedirect.com/science/article/pii/S0168169921001502) | 履带式田间机器人沿猕猴桃棚架采图，用视觉检测与回归估计果数。（范围：A/B） | CEA | 未核验 |
| [Estimation of Fruit Load in Australian Mango Orchards Using Machine Vision](https://www.mdpi.com/2073-4395/11/9/1711) | 多视角机器视觉评估澳大利亚芒果园树级/园级负载，并与包装线实际数量比较，讨论负载制图和采收规划。（范围：B） | Agronomy | 未核验 |
| [Attempting to Estimate the Unseen—Correction for Occluded Fruit in Tree Fruit Load Estimation by Machine Vision with Deep Learning](https://www.mdpi.com/2073-4395/11/2/347) | 用冠层可见图像特征学习遮挡修正因子，减少不可见果实造成的负载低估；在 880 棵树上与包装线计数比较。（范围：B） | Agronomy | 未核验 |
| [Reliability of a commercial platform for estimating flower cluster and fruit number, yield, tree geometry and light interception in apple trees under different rootstocks and row orientations](https://www.sciencedirect.com/science/article/pii/S0168169921005366) | 验证商用果园传感平台对苹果花簇、果数、产量和树体参数的估计可靠性。（范围：A/B） | CEA | — |
| [End-to-End Automatic Berry Counting for Table Grape Thinning](https://doi.org/10.1109/ACCESS.2020.3048374) | 面向鲜食葡萄疏果，提出端到端葡萄粒计数网络并用于单穗浆果数量估计。（范围：A） | IEEE Access | 未核验 |

</details>

<details>
<summary>遥感/航拍计数 · 1 篇</summary>

| 论文题目 | 摘要（中文释义） | 刊会简称 | 代码 |
| --- | --- | --- | --- |
| [Counting from Sky: A Large-Scale Data Set for Remote Sensing Object Counting and a Benchmark Method](https://doi.org/10.1109/TGRS.2020.3020555) | 【遥感计数】发布大规模遥感目标计数数据集与基线，建立卫星/航拍视角下的密度估计评测。 | IEEE TGRS | [代码与数据](https://github.com/gaoguangshuai/Counting-from-Sky-A-Large-scale-Dataset-for-Remote-Sensing-Object-Counting-and-A-Benchmark-Method) |

</details>

<details>
<summary>类无关/少样本/示例驱动计数 · 1 篇</summary>

| 论文题目 | 摘要（中文释义） | 刊会简称 | 代码 |
| --- | --- | --- | --- |
| [Learning to Count Everything](https://openaccess.thecvf.com/content/CVPR2021/html/Ranjan_Learning_To_Count_Everything_CVPR_2021_paper.html) | 【类无关/少样本】利用少量视觉示例学习跨类别计数，是通用少样本计数的重要基线。 | CVPR | [作者代码](https://github.com/cvlab-stonybrook/LearningToCountEverything) |

</details>

</details>

<details id="fruit-year-2022">

<summary>2022 · 16 篇</summary>

<details>
<summary>农业果实计数与果园估产 · 8 篇</summary>

| 论文题目 | 摘要（中文释义） | 刊会简称 | 代码 |
| --- | --- | --- | --- |
| [A weakly-supervised approach for flower/fruit counting in apple orchards](https://www.sciencedirect.com/science/article/pii/S0166361522000306) | CountNet 仅以图像级总数监督学习，不要求逐果框/掩膜；用于苹果花与果计数。（范围：P/A） | Comput. Ind. | 未核验 |
| [A novel apple fruit detection and counting methodology based on deep learning and trunk tracking in modern orchard](https://www.sciencedirect.com/science/article/pii/S0168169922003179) | YOLO 检测与树干跟踪相结合，为果实分配身份并跨视频帧去重。（范围：A） | CEA | 未核验 |
| [Culling Double Counting in Sequence Images for Fruit Yield Estimation](https://www.mdpi.com/2073-4395/12/2/440) | 检测后使用跨图像匹配去除重复果实计数，面向苹果和柑橘视频估产。（范围：A/B） | Agronomy | 未核验 |
| [Tracking and Counting of Tomato at Different Growth Period Using an Improving YOLO-Deepsort Network for Inspection Robot](https://www.mdpi.com/2075-1702/10/6/489) | 改进 YOLO 与 DeepSORT 跟踪温室番茄不同生长阶段目标，按区域/轨迹进行果数统计。（范围：A） | Machines | 未核验 |
| [Slicing aided large scale tomato fruit detection and counting in 360-degree video data from a greenhouse](https://www.sciencedirect.com/science/article/pii/S0263224122011733) | 把 360° 温室视频展开成超宽图，再切片检测并拼接边缘重叠目标，完成整行番茄数量统计。（范围：A） | Measurement | 未核验 |
| [Fruit counting using autonomous flight of small UAV](https://www.jstage.jst.go.jp/article/jass/38/2/38_29/_article) | 小型无人机自主飞行采集柑橘树影像并估计果数，属于低空果园计数路线。（范围：A） | Jpn. J. Agric. Syst. | 未核验 |
| [Yield estimation of citrus fruit using rapid image processing in natural background](https://www.sciencedirect.com/science/article/pii/S2772375521000277) | 基于自然背景下的颜色分割和图像处理统计柑橘果数，并用于产量估算。（范围：A/B） | SAT | 未核验 |
| [Apple Counting using Convolutional Neural Networks](https://arxiv.org/abs/2208.11566) | 比较 CNN 计数与传统图像方法，在多种苹果数据集上评估计数/产量估计。（范围：A/B） | arXiv | 未核验 |

</details>

<details>
<summary>遥感/航拍计数 · 7 篇</summary>

| 论文题目 | 摘要（中文释义） | 刊会简称 | 代码 |
| --- | --- | --- | --- |
| [IS-Count: Large-Scale Object Counting from Satellite Images with Covariate-Based Importance Sampling](https://ojs.aaai.org/index.php/AAAI/article/view/21462) | 【遥感计数】以协变量重要性抽样估计卫星图像中的区域目标总量，降低训练分布与目标区域分布偏差。 | AAAI | [官方代码](https://github.com/sustainlab-group/IS-Count) |
| [Object Counting for Remote-Sensing Images via Adaptive Density Map-Assisted Learning (ADMAL)](https://doi.org/10.1109/TGRS.2022.3208326) | 【遥感计数】以自适应密度图辅助高分辨率遥感目标计数，适应密集目标与空间分布变化。 | IEEE TGRS | [代码与预训练模型](https://github.com/gcding/ADMAL-pytorch) |
| [Distillation Remote Sensing Object Counting via Multi-Scale Context Feature Aggregation](https://doi.org/10.1109/TGRS.2021.3125249) | 【遥感计数】通过多尺度上下文聚合与知识蒸馏压缩遥感计数模型。 | IEEE TGRS | 未找到官方模型代码 |
| [PSGCNet: A Pyramidal Scale and Global Context Guided Network for Dense Object Counting in Remote-Sensing Images](https://doi.org/10.1109/TGRS.2022.3153946) | 【遥感计数】以金字塔尺度特征和全局上下文建模遥感图像中的多尺度密集对象。 | IEEE TGRS | [作者代码](https://github.com/gaoguangshuai/PSGCNet) |
| [Global Multi-Scale Information Fusion for Multi-Class Object Counting in Remote Sensing Images](https://doi.org/10.3390/rs14164026) | 【遥感计数】融合全局与多尺度特征，完成遥感图像多类别目标计数。 | Remote Sens. | 未找到官方模型代码 |
| [Object Counting in Remote Sensing via Triple Attention and Scale-Aware Network](https://doi.org/10.3390/rs14246363) | 【遥感计数】结合三重注意力和尺度感知模块，改善复杂背景下的多尺度密度估计。 | Remote Sens. | 未找到官方模型代码 |
| [Density Map-based Vehicle Counting in Remote Sensing Images with Limited Resolution](https://doi.org/10.1016/j.isprsjprs.2022.05.004) | 【遥感计数】针对有限分辨率影像中的密集车辆，使用密度图处理目标粘连与计数。 | ISPRS JPRS | [RSVC 数据/生成资源](https://github.com/YinongGuo/RSVC2021-Dataset)（非模型代码） |

</details>

<details>
<summary>类无关/少样本/示例驱动计数 · 1 篇</summary>

| 论文题目 | 摘要（中文释义） | 刊会简称 | 代码 |
| --- | --- | --- | --- |
| [Exemplar-Free Class-Agnostic Counting](https://openaccess.thecvf.com/content/ACCV2022/papers/Ranjan_Exemplar_Free_Class_Agnostic_Counting_ACCV_2022_paper.pdf) | 【类无关计数】不提供测试视觉示例，利用 objectness 与重复性线索推断新类别实例数。 | ACCV | 未确认官方代码 |

</details>

</details>

<details id="fruit-year-2023">

<summary>2023 · 19 篇</summary>

<details>
<summary>农业果实计数与果园估产 · 11 篇</summary>

| 论文题目 | 摘要（中文释义） | 刊会简称 | 代码 |
| --- | --- | --- | --- |
| [Apple orchard production estimation using deep learning strategies: A comparison of tracking-by-detection algorithms](https://www.sciencedirect.com/science/article/abs/pii/S0168169922008213) | 系统比较苹果园视频中的检测-跟踪组合及其果数/产量估算表现。（范围：A/B） | CEA | 未核验 |
| [NDMFCS: An automatic fruit counting system in modern apple orchard using abatement of abnormal fruit detection](https://www.sciencedirect.com/science/article/pii/S0168169923004246) | YOLOv4-tiny 检测、异常检测剔除和树干跟踪身份分配组成完整苹果计数流程。（范围：A） | CEA | 未核验 |
| [Twice matched fruit counting system: An automatic fruit counting pipeline in modern apple orchard using mutual and secondary matches](https://www.sciencedirect.com/science/article/pii/S1537511023001885) | 利用互匹配与二次匹配降低跨帧 ID 切换和重复计数，给出现代苹果园果数估计。（范围：A） | Biosyst. Eng. | 未核验 |
| [Real-time tracking and counting of grape clusters in the field based on channel pruning with YOLOv5s](https://www.sciencedirect.com/science/article/pii/S0168169923000509) | 剪枝轻量化 YOLOv5s 并结合视频跟踪，实现田间葡萄串实时计数。（范围：A） | CEA | 未核验 |
| [Semi-supervised Counting of Grape Berries in the Field Based on Density Mutual Exclusion](https://www.sciopen.com/article/10.34133/plantphenomics.0115) | 半监督密度图计数，设计密度互斥约束以缓解浆果密集重叠。（范围：A） | Plant Phenomics | [Code](https://github.com/youth-tang/CDMENet-main) |
| [Instance Segmentation and Berry Counting of Table Grape before Thinning Based on AS-SwinT](https://www.sciopen.com/article/10.34133/plantphenomics.0085) | Swin Transformer 实例分割葡萄粒，并回归单穗果数，用于疏果前评估。（范围：A） | Plant Phenomics | [作者仓库含代码压缩包](https://github.com/AWEN975/AS-SwinT)；未验证本地复现 |
| [Tomato cluster detection and counting using improved YOLOv5 based on RGB-D fusion](https://www.sciencedirect.com/science/article/pii/S0168169923001291) | 融合 RGB-D 检测番茄簇，并以 ByteTrack 与计数区域消除重复；机器人实测平均计数准确率 95.1%。（范围：A） | CEA | 未核验 |
| [An efficient online citrus counting system for large-scale unstructured orchards based on the unmanned aerial vehicle](https://onlinelibrary.wiley.com/doi/10.1002/rob.22147) | 无人机在线采集非结构化果园图像，跟踪并计数柑橘，针对跟踪失误设计非均匀分布计数器。（范围：A） | J. Field Robot. | 未核验 |
| [Tree-level citrus yield prediction utilizing ground and aerial machine vision and machine learning](https://www.sciencedirect.com/science/article/pii/S2772375522000429) | 融合无人机树体特征与地面单/双侧柑橘计数，建立树级产量预测。（范围：B） | SAT | 未核验 |
| [Seeing the Fruit for the Leaves: Robotically Mapping Apple Fruitlets in a Commercial Orchard](https://arxiv.org/abs/2308.07512) | 机器人從果树两侧扫描并构建商业苹果园幼果地图，评估幼果可见性和计数。（范围：P/A） | IROS | 未核验 |
| [UAV Photogrammetry-Based Apple Orchard Blossom Density Estimation and Mapping](https://www.mdpi.com/2311-7524/9/2/266) | 用无人机影像和摄影测量点云估计苹果花密度并制图，服务于早期负载管理。（范围：P） | Horticulturae | 未核验 |

</details>

<details>
<summary>遥感/航拍计数 · 3 篇</summary>

| 论文题目 | 摘要（中文释义） | 刊会简称 | 代码 |
| --- | --- | --- | --- |
| [Cross-Region Building Counting in Satellite Imagery using Counting Consistency](https://doi.org/10.1007/s00521-023-08923-0) | 【遥感计数】以计数一致性应对卫星影像地域域偏移，估计跨区域建筑数量。 | Neural Comput. Appl. | [作者代码](https://github.com/intelligentMachines-ITU/domain-Adaptive-Building-Counting) |
| [Remote Sensing Object Counting Through Regression Ensembles and Learning to Rank](https://doi.org/10.1109/TGRS.2023.3266884) | 【遥感计数】融合回归集成与排序学习，提升密集遥感场景计数的稳定性。 | IEEE TGRS | [作者代码](https://github.com/huangyongbobo/eFreeNet) |
| [A Lightweight Multiscale Feature Fusion Network for Remote Sensing Object Counting](https://doi.org/10.1109/TGRS.2023.3238185) | 【遥感计数】通过轻量多尺度特征融合兼顾遥感目标计数精度与计算效率。 | IEEE TGRS | 未找到官方模型代码 |

</details>

<details>
<summary>开放词汇/开放世界计数 · 3 篇</summary>

| 论文题目 | 摘要（中文释义） | 刊会简称 | 代码 |
| --- | --- | --- | --- |
| [Zero-Shot Object Counting](https://openaccess.thecvf.com/content/CVPR2023/html/Xu_Zero-Shot_Object_Counting_CVPR_2023_paper.html) | 【开放计数】以类别文本为条件生成密度图，在缺少该类别计数训练样本时估计目标数量。 | CVPR | [官方代码](https://github.com/cvlab-stonybrook/zero-shot-counting) |
| [CLIP-Count: Towards Text-Guided Zero-Shot Object Counting](https://dl.acm.org/doi/10.1145/3581783.3611789) | 【开放计数】利用文本提示选择 CLIP 视觉语义，再通过密度估计完成未见类别计数。 | ACM MM | [作者代码](https://github.com/songrise/CLIP-Count) |
| [CounTX: Open-world Text-specified Object Counting](https://arxiv.org/abs/2306.01851) | 【开放计数】将任意文本类别与图像特征交互，实现不需要人工框选示例的文本指定计数。 | BMVC | [作者代码](https://github.com/niki-amini-naieni/CounTX) |

</details>

<details>
<summary>类无关/少样本/示例驱动计数 · 1 篇</summary>

| 论文题目 | 摘要（中文释义） | 刊会简称 | 代码 |
| --- | --- | --- | --- |
| [LOCA: A Low-Shot Object Counting Network with Iterative Prototype Adaptation](https://openaccess.thecvf.com/content/ICCV2023/html/Dukic_A_Low-Shot_Object_Counting_Network_with_Iterative_Prototype_Adaptation_ICCV_2023_paper.html) | 【类无关/少样本】用少量框选示例迭代更新类别原型，适配图像中的目标外观与尺度。 | ICCV | [作者代码](https://github.com/val-iisc/LOCA) |

</details>

<details>
<summary>计数基准/推理/生成控制 · 1 篇</summary>

| 论文题目 | 摘要（中文释义） | 刊会简称 | 代码 |
| --- | --- | --- | --- |
| [Teaching CLIP to Count to Ten](https://openaccess.thecvf.com/content/ICCV2023/html/Paiss_Teaching_CLIP_to_Count_to_Ten_ICCV_2023_paper.html) | 【计数推理】评测并增强视觉语言模型对数词和物体数量的理解；属于数量推理，不是密度图计数器。 | ICCV | 未确认官方代码 |

</details>

</details>

<details id="fruit-year-2024">

<summary>2024 · 32 篇</summary>

<details>
<summary>农业果实计数与果园估产 · 17 篇</summary>

| 论文题目 | 摘要（中文释义） | 刊会简称 | 代码 |
| --- | --- | --- | --- |
| [AgRegNet: A deep regression network for flower and fruit density estimation, localization, and counting in orchards](https://www.sciencedirect.com/science/article/pii/S0168169924009256) | 无需逐目标检测框/多边形标注，回归花与果实密度、位置和数量。（范围：A/P） | CEA | 未核验 |
| [Using unmanned aerial vehicle acquired RGB images and Density-Cluster-Count model for tree-level apple flower quantification](https://www.sciencedirect.com/science/article/pii/S0168169924007804) | 无人机 RGB 影像与密度-聚类-计数模型估计树级苹果花量并制图。（范围：P） | CEA | 未核验 |
| [Probability map-based grape detection and counting](https://www.sciencedirect.com/science/article/pii/S0168169924005660) | 单网络预测葡萄簇与果粒概率图，后处理同时完成簇定位、果粒计数和每簇粒数估计。（范围：A） | CEA | [Code](https://github.com/volcanoYcc/Probability-Map-based-Grape-Detection-and-Counting) |
| [Advancing tracking-by-detection with MultiMap: Towards occlusion-resilient online multiclass strawberry counting](https://www.sciencedirect.com/science/article/pii/S0957417424014544) | MultiMap 多特征匹配增强遮挡下草莓多类别在线跟踪计数。（范围：A） | ESWA | [Code](https://github.com/Xuehaiz/MultiMap) |
| [Multiple orange detection and tracking with 3-D fruit relocalization and neural-net based yield regression in commercial sweet orange orchards](https://www.sciencedirect.com/science/article/pii/S0168169924005908) | 多视角橙果跟踪与 3D 重新定位防止重复计数，再用神经网络结合树体信息估计总果数/负载。（范围：A/B） | CEA | 未核验 |
| [A robust and efficient citrus counting approach for large-scale unstructured orchards](https://www.sciencedirect.com/science/article/pii/S0308521X24000179) | 无人机数据流、低照度图像增强、Fruit-YOLO 与 DeepSORT 组成大规模柑橘园在线计数管线。（范围：A） | Agric. Syst. | 未核验 |
| [Green pepper fruits counting based on improved DeepSort and optimized Yolov5s](https://www.frontiersin.org/journals/plant-science/articles/10.3389/fpls.2024.1417682/full) | 改进 YOLOv5s 与 DeepSORT 跟踪遮挡、重叠的田间青椒并统计果数。（范围：A） | Front. Plant Sci. | 未核验 |
| [Tracking and Counting Apples in Orchards Under Intermittent Occlusions and Low Frame Rates](https://openaccess.thecvf.com/content/CVPR2024W/Vision4Ag/html/Matos_Tracking_and_Counting_Apples_in_Orchards_Under_Intermittent_Occlusions_and_CVPRW_2024_paper.html) | 利用几何一致性、SfM 与二分图匹配，在间歇遮挡和低帧率下追踪并计数苹果。（范围：A） | CVPRW | 未核验 |
| [Automatic Apple Detection and Counting with AD-YOLO and MR-SORT](https://www.mdpi.com/1424-8220/24/21/7012) | 手机视频中的苹果检测与 MR-SORT 跟踪去重，输出计数。（范围：A） | Sensors | 未核验 |
| [An automatic tracking method for fruit abscission of litchi using convolutional networks](https://www.sciencedirect.com/science/article/pii/S0168169924006045) | 对荔枝枝条长期视频中的果实进行跟踪计数，研究落果动态与生长变化。（范围：A） | CEA | 未核验 |
| [Autonomous Yield Estimation System for Small Commercial Orchards Using UAV and AI](https://www.mdpi.com/2504-446X/8/12/734) | 小型商业果园 UAV 自动采集并通过果实检测/计数与回归估算树级产量。（范围：B） | Drones | 未核验 |
| [AgroCounters—A repository for counting objects in images in the agricultural domain by using deep-learning algorithms: Framework and evaluation](https://www.sciencedirect.com/science/article/pii/S016816992400379X) | 在农业通用单图计数框架中比较检测、回归和密度估计方法，覆盖果蔬等对象。（范围：A） | CEA | [Code](https://github.com/farjon/Counting_in_Agri) |
| [Detection, counting, and maturity assessment of blueberries in canopy images using YOLOv8 and YOLOv9](https://www.sciencedirect.com/science/article/pii/S2772375524002259) | 发布蓝莓冠层图像数据集并评估检测、成熟度和图像级果数误差。（范围：A） | SAT | [Code](https://github.com/vicdxxx/BlueberryDetectionAndCounting) |
| [ChatGPT and general-purpose AI count fruits in pictures surprisingly well without programming or training](https://www.sciencedirect.com/science/article/pii/S2772375524002934) | 比较 GPT-4V、T-Rex 与 YOLOv8 对农场咖啡樱桃图像的计数，评估少样本和人工反馈。（范围：A） | SAT | — |
| [FruitNeRF: A Unified Neural Radiance Field based Fruit Counting Framework](https://arxiv.org/abs/2408.06190) | 利用多视角重建与语义 NeRF 在三维场景中对不同果实类型聚类计数。（范围：A） | IROS | [Code](https://github.com/meyerls/fruitnerf) |
| [Artificial Size Slicing Aided Fine Tuning (ASSAFT) and Hyper Inference (ASSAHI) in tomato detection](https://www.sciencedirect.com/science/article/pii/S0168169924006719) | 在 360° 温室行图像上改进分块检测，并报告番茄计数流程结果。（范围：A） | CEA | 未核验 |
| [StraTracker: A dynamic counting method for growing strawberries based on multi-target tracking](https://www.sciencedirect.com/science/article/pii/S0168169924009554) | 将草莓动态计数建模为多目标跟踪，覆盖多个生长阶段；YOLOv8n 检测器报告 38.3 FPS，跟踪 MOTA 为 83.28%、HOTA 为 77.26%，计数与真值相关系数 R²=0.91（另报告 GEH=2.33）。（范围：A） | CEA | 未核验 |

</details>

<details>
<summary>遥感/航拍计数 · 7 篇</summary>

| 论文题目 | 摘要（中文释义） | 刊会简称 | 代码 |
| --- | --- | --- | --- |
| [NWPU-MOC: A Benchmark for Fine-grained Multi-category Object Counting in Aerial Images](https://arxiv.org/abs/2401.10530) | 【遥感计数/基准】构建多类别航拍计数数据与基准，支持车辆、船舶等目标的细粒度评估。 | IEEE TGRS | [基准、数据与代码](https://github.com/lyongo/NWPU-MOC) |
| [Few-Shot Object Counting With Dynamic Similarity-Aware in Latent Space (DSALVANet)](https://doi.org/10.1109/TGRS.2024.3350383) | 【遥感计数/少样本】用潜在空间动态相似度，借少量示例适配航拍新类别与场景。 | IEEE TGRS | [作者代码](https://github.com/kadvinj/DSALVANet) |
| [Hierarchical Kernel Interaction Network for Remote Sensing Object Counting](https://doi.org/10.1109/TGRS.2023.3348870) | 【遥感计数】通过层级核交互捕获多尺度空间上下文，改善密度图与数量预测。 | IEEE TGRS | 未找到官方模型代码 |
| [DOPNet: Dense Object Prediction Network for Multi-Class Object Counting and Localization in Remote Sensing Images](https://doi.org/10.1109/TGRS.2024.3349702) | 【遥感计数】联合预测密度与目标位置，面向遥感多类别目标的计数和定位。 | IEEE TGRS | [作者代码](https://github.com/Ceoilmp/DOPNet) |
| [Balanced Density Regression Network for Remote Sensing Object Counting](https://doi.org/10.1109/TGRS.2024.3402271) | 【遥感计数】通过平衡密度回归缓解样本分布偏斜，改善密集目标计数。 | IEEE TGRS | [作者代码](https://github.com/HotChieh/BDRNet) |
| [Uncertainty-aware Continuous Implicit Neural Representations for Remote Sensing Object Counting](https://proceedings.mlr.press/v238/xu24k.html) | 【遥感计数】以连续隐式密度表示和不确定性估计降低栅格预测对目标尺度的限制。 | AISTATS | [作者代码](https://github.com/SiyuanXu-tamu/UNIC) |
| [ResCount: A Residual Feature Fusion Network for Ship Counting in Remote Sensing Images](https://doi.org/10.1109/LGRS.2024.3462444) | 【遥感计数】融合残差特征并以密度预测完成遥感船舶计数。 | IEEE GRSL | 未找到官方模型代码 |

</details>

<details>
<summary>开放词汇/开放世界计数 · 5 篇</summary>

| 论文题目 | 摘要（中文释义） | 刊会简称 | 代码 |
| --- | --- | --- | --- |
| [VLCounter: Text-Aware Visual Representation for Zero-Shot Object Counting](https://ojs.aaai.org/index.php/AAAI/article/view/28050) | 【开放计数】将类别文本注入视觉表示，改善零样本计数中的语义—目标区域对齐。 | AAAI | [论文页所列代码](https://github.com/Seunggu0305/VLCounter) |
| [Zero-shot Object Counting with Good Exemplars (VA-Count)](https://www.ecva.net/papers/eccv_2024/papers_ECCV/papers/00812.pdf) | 【开放计数/示例提示】从当前图像选择可靠视觉示例辅助零样本目标定位；不同于仅文本提示。 | ECCV | [作者代码](https://github.com/HopooLinZ/VA-Count) |
| [Class-Agnostic Object Counting with Text-to-Image Diffusion Model (CountDiff)](https://www.ecva.net/papers/eccv_2024/papers_ECCV/html/8663_ECCV_2024_paper.php) | 【开放/类无关计数】利用扩散模型知识，在视觉示例少样本和类别名零样本设置下计数。 | ECCV | 未找到官方模型代码 |
| [CountGD: Multi-Modal Open-World Counting](https://arxiv.org/abs/2407.04619) | 【开放计数】将文本、视觉示例或二者联合提示接入 Grounding DINO，支持开放世界目标计数。 | NeurIPS | [官方代码](https://github.com/niki-amini-naieni/CountGD) |
| [Referring Expression Counting](https://openaccess.thecvf.com/content/CVPR2024/html/Dai_Referring_Expression_Counting_CVPR_2024_paper.html) | 【开放计数】发布 REC-8K，以属性、动作和上下文表达区分同类目标并计数。 | CVPR | [论文代码与数据](https://github.com/sydai/referring-expression-counting) |

</details>

<details>
<summary>类无关/少样本/示例驱动计数 · 3 篇</summary>

| 论文题目 | 摘要（中文释义） | 刊会简称 | 代码 |
| --- | --- | --- | --- |
| [PseCo: Point, Segment and Count: A Generalized Framework for Object Counting](https://openaccess.thecvf.com/content/CVPR2024/papers/Huang_Point_Segment_and_Count_A_Generalized_Framework_for_Object_Counting_CVPR_2024_paper.pdf) | 【类无关/少样本】统一点、分割和计数监督，通过视觉示例适配通用对象计数。 | CVPR | [作者代码](https://github.com/Hzzone/PseCo) |
| [DAVE: A Detect-and-Verify Paradigm for Low-Shot Counting](https://openaccess.thecvf.com/content/CVPR2024/html/Pelhan_DAVE_-_A_Detect-and-Verify_Paradigm_for_Low-Shot_Counting_CVPR_2024_paper.html) | 【类无关/少样本】先检测候选，再验证与示例的相似性，减少密集场景漏计和重计。 | CVPR | [作者代码](https://github.com/jerpelhan/DAVE) |
| [GeCo: A Novel Unified Architecture for Low-Shot Counting by Detection and Segmentation](https://proceedings.neurips.cc/paper_files/paper/2024/file/7a0f8055c838df8e62329a76c7c6403d-Paper-Conference.pdf) | 【类无关/少样本】将检测和分割纳入低样本计数架构，以少量示例适配任意类别。 | NeurIPS | [作者代码](https://github.com/jerpelhan/GeCo) |

</details>

</details>

<details id="fruit-year-2025">

<summary>2025 · 44 篇</summary>

<details>
<summary>农业果实计数与果园估产 · 19 篇</summary>

| 论文题目 | 摘要（中文释义） | 刊会简称 | 代码 |
| --- | --- | --- | --- |
| [Estimation of passion fruit yield based on YOLOv8n + OC-SORT + CRCM algorithm](https://www.sciencedirect.com/science/article/pii/S0168169924011189) | YOLOv8n 检测、OC-SORT 跟踪和中心区域补偿计数，估算百香果园果数/产量。（范围：A/B） | CEA | 未核验 |
| [Assessment of the tomato cluster yield estimation algorithms via tracking-by-detection approaches](https://www.sciencedirect.com/science/article/pii/S2214317325000150) | 在大规模番茄簇多目标跟踪数据上比较检测器与跟踪器组合，直接评估产量计数准确度。（范围：A） | Inf. Process. Agric. | 未核验 |
| [Row-based kiwifruit counting pipeline for smartphone-captured videos using fruit tracking and detection region adaptation guided by support-post](https://www.sciencedirect.com/science/article/pii/S0168169925005824) | 针对手机拍摄的猕猴桃行视频，结合支柱引导区域自适应与果实跟踪减少漏计/重计。（范围：A） | CEA | 未核验 |
| [Mandarin count estimation with 360-degree tree video and transformer-based deep learning](https://www.sciencedirect.com/science/article/pii/S2772375525001078) | 融合单树 360° 视频视角信息，以 Transformer 估算疏果前柑橘负载。（范围：A/B） | SAT | 未核验 |
| [Deep learning framework for fruit counting and yield mapping in tart cherry using YOLOv8 and YOLO11](https://www.sciencedirect.com/science/article/pii/S2772375525001819) | 比较采收机输送带视频上的 YOLOv8/YOLO11 果实检测计数，并构建酸樱桃产量图。（范围：A/B） | SAT | 未核验 |
| [Estimation of orange tree production by regression from video segments under uncontrolled conditions](https://link.springer.com/article/10.1007/s00521-024-10772-4) | 把非受控果园视频片段的多帧预测聚合成更稳定的橙树果数/产量估计。（范围：B） | Neural Comput. Appl. | [Code](https://github.com/pjsv1990uji/Orange-count---FPN) |
| [Multi-Species Fruit-Load Estimation Using Deep Learning Models](https://www.mdpi.com/2624-7402/7/7/220) | 基于 MetaFruit 五类果实与补充数据比较检测、回归和热图密度模型，重点讨论跨品种负载估计。（范围：A/B） | AgriEngineering | 未核验 |
| [FruitNeRF++: A Generalized Multi-Fruit Counting Method Utilizing Contrastive Learning and Neural Radiance Fields](https://arxiv.org/abs/2505.19863) | 在 FruitNeRF 三维多视角计数基础上加入对比学习，提升跨果种/跨场景表示与计数泛化。（范围：A） | IROS | [Code](https://github.com/meyerls/FruitNeRFpp) |
| [CountingFruit: Real-Time 3D Fruit Counting with Language-Guided Semantic Gaussian Splatting](https://arxiv.org/abs/2506.01109) | 将语言引导语义与 Gaussian Splatting 结合，在三维场景中实时聚类计数果实。（范围：A） | arXiv | [Code](https://github.com/Cola-1/FruitLangGS) |
| [A novel multiscale feature enhancement network using learnable density map for red clustered pepper yield estimation](https://www.frontiersin.org/journals/plant-science/articles/10.3389/fpls.2025.1548035/full) | 用可学习密度图与多尺度特征估计田间簇生红椒数量/产量。（范围：A/B） | Front. Plant Sci. | 未核验 |
| [Mask-GK: An efficient method based on mask Gaussian kernel for segmentation and counting of grape berries in field](https://www.sciencedirect.com/science/article/pii/S0168169925003928) | 把实例标注编码为 mask Gaussian kernel 概率表示，再进行葡萄粒分割与计数。（范围：A） | CEA | [Code](https://github.com/volcanoYcc/Mask-GK) |
| [A precise berry counting method for in-cluster grapes to guide berry thinning](https://www.frontiersin.org/journals/plant-science/articles/10.3389/fpls.2025.1739688/full) | MVDNet 联合密度图回归和果穗分割，输出整图及逐穗葡萄粒数，面向疏果。（范围：A） | Front. Plant Sci. | [Code](https://github.com/AWEN975/MVDNet_code) |
| [AI-based framework for early detection and segmentation of green citrus fruits in orchards](https://www.sciencedirect.com/science/article/pii/S277237552500067X) | MViTv2 与 Cascade Mask R-CNN 检测/分割早期小型绿柑橘，并在全树图像上比较模型果数与人工计数。（范围：A（中等）） | SAT | 未核验 |
| [AppleYOLO: Apple yield estimation method using improved YOLOv8 based on Deep OC-SORT](https://www.sciencedirect.com/science/article/pii/S0957417425003860) | 改进 YOLOv8 与 Deep OC-SORT 结合，进行苹果视频跟踪、重复目标抑制和产量计数。（范围：A/B） | ESWA | 未核验 |
| [Uncertainty-driven semi-supervised learning for phenology-aware apple flower counting](https://www.sciencedirect.com/science/article/pii/S0168169925010257) | 基于物候与不确定性引导半监督学习统计无人机苹果花量。（范围：P） | CEA | 未核验 |
| [Deep learning and georeferenced RGB-D imaging for hydroponic strawberry yield mapping](https://www.sciencedirect.com/science/article/pii/S2772375525005246) | 结合 RGB-D 和地理定位为水培草莓建立产量图，并与人工果数比较。（范围：A/B） | SAT | 未核验 |
| [Improving passion fruit yield estimation with multi-scale feature fusion and density-attention mechanisms in smart agriculture](https://www.sciencedirect.com/science/article/pii/S0168169925010646) | 以多尺度特征和密度注意力处理百香果密集目标并回归树级数量/产量。（范围：A/B） | CEA | 未核验 |
| [A Dynamic Kalman Filtering Method for Multi-Object Fruit Tracking and Counting in Complex Orchards](https://pmc.ncbi.nlm.nih.gov/articles/PMC12252135/) | 将改进 YOLOv8n、动态遗忘因子 Kalman 滤波与 IoU/Re-ID 关联结合，在复杂果园视频中持续跟踪并计数；论文报告计数 R²=0.85、RMSE=1.57。（范围：A） | Sensors | [论文数据可用性声明中的作者代码](https://github.com/zhaiyaning/Fruit_Tacking) |
| [Apple phenotyping using deep learning and 3D depth analysis: An experimental study on fruitlet sizing during early development](https://www.sciencedirect.com/science/article/pii/S2772375525001972) | 结合 RGB-D 视频、YOLO 与深度信息，对苹果幼果簇进行计数和直径测量；属于早期负载代理，论文报告平均计数误差 0.63 个幼果/视频。（范围：P/A） | Smart Agric. Technol. | [作者代码与数据处理流程](https://github.com/checolag/apple-fruitlet-detection-and-sizing) |

</details>

<details>
<summary>遥感/航拍计数 · 7 篇</summary>

| 论文题目 | 摘要（中文释义） | 刊会简称 | 代码 |
| --- | --- | --- | --- |
| [Remote Sensing Object Counting With Online Knowledge Learning](https://arxiv.org/abs/2303.10318) | 【遥感计数】用在线知识学习适应遥感目标及场景分布变化，降低新场景标注负担。 | IEEE TGRS | 未找到官方模型代码 |
| [Counting Beyond Domains: A Cross-Domain Benchmark and Method for Remote Sensing Object Counting](https://doi.org/10.1109/TGRS.2025.3622599) | 【遥感计数】建立跨地域、传感器与影像风格变化的评测，并提出跨域适配方法。 | IEEE TGRS | [作者代码](https://github.com/jwang-rs/CBD-pytorch) |
| [Input-Regulated Remote Sensing Counting With Region Understanding](https://doi.org/10.1109/TGRS.2025.3639196) | 【遥感计数】通过图驱动输入调节和动态区域理解增强少标注遥感目标计数。 | IEEE TGRS | 未确认公开官方代码 |
| [Cross-Domain Density Map-Generated Ship Counting Network for Remote Sensing Images](https://doi.org/10.1109/LGRS.2024.3510093) | 【遥感计数】结合域适配与密度图生成，提升不同分布遥感场景的船舶计数。 | IEEE GRSL | 未找到官方模型代码 |
| [Mamba-MOC: Multi-Category Object Counting in Remote Sensing Images Based on Mamba](https://doi.org/10.1109/IGARSS55030.2025.11243409) | 【遥感计数】引入 Mamba 状态空间模块，对大幅面遥感图像中的多类别目标计数。 | IGARSS | 未找到官方模型代码 |
| [EdgeCount: Efficient Remote Sensing Object Counting via Edge-Guided Feature Learning](https://doi.org/10.1109/TCVST.2024.3469933) | 【遥感计数】以边缘引导特征增强小目标轮廓，兼顾遥感计数精度与效率。 | IEEE TCSVT | 未找到官方模型代码 |
| [Scale-Invariant Implicit Neural Representations for Remote Sensing Object Counting](https://doi.org/10.1109/CVPRW67362.2025.00217) | 【遥感计数】以尺度不变连续隐式表示估计遥感目标密度；为 EarthVision workshop 论文。 | CVPRW EarthVision | 未找到官方模型代码 |

</details>

<details>
<summary>开放词汇/开放世界计数 · 11 篇</summary>

| 论文题目 | 摘要（中文释义） | 刊会简称 | 代码 |
| --- | --- | --- | --- |
| [OmniCount: Multi-label Object Counting with Semantic-Geometric Priors](https://ojs.aaai.org/index.php/AAAI/article/view/34151) | 【开放计数】结合语义与几何先验，对一张图中用户指定的多个类别进行计数。 | AAAI | [作者代码](https://github.com/mondalanindya/OmniCount) |
| [T2ICount: Enhancing Cross-modal Understanding for Zero-Shot Counting](https://openaccess.thecvf.com/content/CVPR2025/html/Qian_T2ICount_Enhancing_Cross-modal_Understanding_for_Zero-Shot_Counting_CVPR_2025_paper.html) | 【开放计数】增强文本提示与局部目标区域的跨模态对应，提升未见类别零样本计数。 | CVPR | [作者代码](https://github.com/cha15yq/T2ICount) |
| [Exploring Contextual Attribute Density in Referring Expression Counting](https://openaccess.thecvf.com/content/CVPR2025/html/Wang_Exploring_Contextual_Attribute_Density_in_Referring_Expression_Counting_CVPR_2025_paper.html) | 【开放计数】以上下文属性密度和多尺度视觉特征定位、计数细粒度指代表达指定对象。 | CVPR | [作者代码 CAD-GD](https://github.com/Xu3XiWang/CAD-GD) |
| [SDVPT: Semantic-Driven Visual Prompt Tuning for Open-World Object Counting](https://doi.org/10.1145/3746027.3754581) | 【开放计数】以语义驱动视觉提示调优，将已见类知识迁移到未见类并适配多种开放世界计数器。 | ACM MM | [部分实现](https://github.com/Eamon-0v0/SDVPT)（仓库标注部分组件待补） |
| [TrueCount: Improving Open-World Object Counting with Visual-Language Models and Dynamic Multi-Modal Inputs](https://doi.org/10.1145/3746027.3755426) | 【开放计数】动态融合 RGB、分割、深度及文本/视觉提示，并估计模态置信度以处理遮挡场景。 | ACM MM | 未找到作者官方模型代码 |
| [VQCounter: Designing Visual Prompt Queue for Accurate Open-World Counting](https://www.ijcai.org/proceedings/2025/252) | 【开放计数】以视觉提示队列扩展示例多样性，结合模态切换与匹配损失支持开放世界计数。 | IJCAI | 未找到作者官方代码 |
| [Text-Promptable Object Counting via Quantity Awareness Enhancement (QUANet)](https://arxiv.org/abs/2507.06679) | 【开放计数】通过数量感知提示、视觉—文本数量对齐及双流解码器增强文本提示计数。 | arXiv 预印本 | [作者代码](https://github.com/viscom-tongji/QUANet) |
| [Expanding Zero-Shot Object Counting with Rich Prompts (RichCount)](https://arxiv.org/abs/2505.15398) | 【开放计数】丰富文本表示并强化视觉—文本对齐，改善未见类别与复杂提示计数。 | arXiv 预印本 | 未找到作者官方代码 |
| [Counting Through Occlusion: Framework for Open World Amodal Counting (CountOCC)](https://arxiv.org/abs/2511.12702) | 【开放计数】从可见上下文重建遮挡实例特征，估计可见与被遮挡目标总数。 | arXiv 预印本 | [作者代码](https://github.com/rabeya-akter/CountOCC) |
| [CountSE: Soft Exemplar Open-set Object Counting](https://openaccess.thecvf.com/content/ICCV2025/html/Liu_CountSE_Soft_Exemplar_Open-set_Object_Counting_ICCV_2025_paper.html) | 【开放计数】由文本语义生成多尺度软示例，再以语义筛选和聚类提升开放集目标定位与计数。 | ICCV | [官方代码](https://github.com/pppppz22/CountSE) |
| [LGCount: Enhancing Zero-shot Object Counting via Text-guided Local Ranking and Number-evoked Global Attention](https://openaccess.thecvf.com/content/ICCV2025/html/Zhang_Enhancing_Zero-shot_Object_Counting_via_Text-guided_Local_Ranking_and_Number-evoked_ICCV_2025_paper.html) | 【开放计数】以文本引导局部排序和数量感知全局注意力处理零样本计数，并构建 ZSC-8K。 | ICCV | [作者代码](https://github.com/zaqai/LGCount) |

</details>

<details>
<summary>类无关/少样本/示例驱动计数 · 4 篇</summary>

| 论文题目 | 摘要（中文释义） | 刊会简称 | 代码 |
| --- | --- | --- | --- |
| [A Simple-but-Effective Baseline for Training-Free Class-Agnostic Counting](https://openaccess.thecvf.com/content/WACV2025/html/Lin_A_Simple-but-Effective_Baseline_for_Training-Free_Class-Agnostic_Counting_WACV_2025_paper.html) | 【类无关计数】通过超像素提示、语义特征和原型更新，实现无需额外训练的示例驱动计数。 | WACV | 未确认作者官方代码 |
| [Counting with Ease: Class-Agnostic Counting via One-Shot Detection across Diverse Domains (CACAL)](https://doi.org/10.1016/j.neunet.2025.107961) | 【类无关计数】以单个查询示例跨域定位和计数，并提出涵盖工业、农业等场景的 LOCO 基准。 | Neural Networks | [仓库仅含说明，非模型实现](https://github.com/imMid-Star/CACAL) |
| [FocalCount: Towards Class-Count Imbalance in Class-Agnostic Counting](https://arxiv.org/abs/2502.10677) | 【类无关计数】研究类别数量不均衡，通过类别数估计和 Focal-MSE 强化少见类别的计数误差。 | arXiv 预印本 | 论文称将发布；尚未找到公开仓库 |
| [CountZES: Counting via Zero-Shot Exemplar Selection](https://arxiv.org/abs/2512.16415) | 【示例驱动计数】自动选取无需人工标注的视觉示例，再进行跨场景计数；并非纯文本零样本。 | arXiv 预印本 | [作者代码](https://github.com/Muhammad-Ibraheem-Siddiqui/CountZES) |

</details>

<details>
<summary>计数基准/推理/生成控制 · 3 篇</summary>

| 论文题目 | 摘要（中文释义） | 刊会简称 | 代码 |
| --- | --- | --- | --- |
| [Mind the Prompt: A Novel Benchmark for Prompt-Based Class-Agnostic Counting (PrACo)](https://openaccess.thecvf.com/content/WACV2025/html/Ciampi_Mind_the_Prompt_A_Novel_Benchmark_for_Prompt-Based_Class-Agnostic_Counting_WACV_2025_paper.html) | 【开放计数基准】以负提示和多类干扰图评估模型是否按提示选择目标；是评测基准而非新计数器。 | WACV | [基准代码](https://github.com/ciampluca/PrACo) |
| [YOLO-Count: Differentiable Object Counting for Text-to-Image Generation](https://openaccess.thecvf.com/content/ICCV2025/html/Zeng_YOLO-Count_Differentiable_Object_Counting_for_Text-to-Image_Generation_ICCV_2025_paper.html) | 【计数与生成】将可微计数器用作文生图中的目标数量控制模块，属于计数/生成交叉方向。 | ICCV | [作者代码](https://github.com/mlpc-ucsd/YOLO-Count) |
| [Can Current AI Models Count What We Mean, Not What They See? A Benchmark and Systematic Evaluation (PairTally)](https://arxiv.org/abs/2509.13939) | 【计数基准】以 PairTally 评估模型按文字意图区分外观相似子类并计数，不是新计数模型。 | DICTA / arXiv | [基准、数据与评测代码](https://github.com/bbvisual/PairTally_Benchmark) |

</details>

</details>

<details id="fruit-year-2026">

<summary>2026 · 46 篇</summary>

<details>
<summary>农业果实计数与果园估产 · 13 篇</summary>

| 论文题目 | 摘要（中文释义） | 刊会简称 | 代码 |
| --- | --- | --- | --- |
| [Benchmarking Dense and Indiscernible Object Counting with Blueberries](https://proceedings.mlr.press/v306/bo26a.html) | 提出 DIOCblueberry 蓝莓密集、遮挡与背景近似计数基准及 MaskCount；利用 CLIP 伪掩膜抑制背景、对比学习区分蓝莓与叶片，并以边缘感知裁剪缓解切块漏计。（直接果实计数） | ICML | 数据集：[DIOCblueberry](https://huggingface.co/datasets/weihao-bo/DIOCblueberry)；未找到可访问的官方模型代码 |
| [Low-annotation apple flower counting: A color-SAM enhanced and uncertainty-guided semi-supervised framework](https://www.sciencedirect.com/science/article/pii/S2643651526000270) | Color-SAM 与不确定性引导半监督密度估计用于少标注苹果花计数。（范围：P） | Plant Phenomics | [Code](https://github.com/haohuihui5019/USCount-Net) |
| [Accurate counting of small and dense Chinese cherry in natural orchard via fruit-oriented perception and sharpening network](https://www.sciencedirect.com/science/article/abs/pii/S0168169926005041) | FOPSN 密度图计数网络针对小目标、黏连和自然果园复杂背景优化。（范围：A） | CEA | 未核验 |
| [YOLO11-SBS: leveraging ACE and ORCM to gauge robust and accurate apple counting in complex orchards](https://www.frontiersin.org/journals/plant-science/articles/10.3389/fpls.2026.1841916/full) | 改进 YOLO11 在复杂果园图像中检测并统计苹果，重点关注遮挡和背景干扰。（范围：A） | Front. Plant Sci. | 未核验 |
| [Automated oil palm fruit counting using deep learning for reliable yield estimation in natural background](https://www.sciencedirect.com/science/article/pii/S2772375526006015) | 对自然背景下油棕鲜果串图像进行检测计数，比较 YOLOv5s、YOLOv8n 与 Mask R-CNN，并报告计数误差。（范围：A/B） | SAT | 未核验 |
| [Agrosense v2: An AI-enabled system for precision orchard sensing and tree-level monitoring](https://www.sciencedirect.com/science/article/pii/S0168169926003923) | 真实柑橘园集成树识别、地理定位和果实检测计数，将树上/地面果数汇总为树级时空信息。（范围：A/B） | CEA | 未核验 |
| [Research on Greenhouse Eggplant Fruit Detection and Tracking-Based Counting Using an Improved YOLOv5s-DeepSORT](https://www.mdpi.com/2077-0472/16/2/253) | 改进 YOLOv5s-DeepSORT 对温室茄子视频跟踪并按计数区统计。（范围：A） | Agriculture | 未核验 |
| [Tomato Maturity Classification and Fruit Counting Based on RGB and Multispectral Images](https://www.mdpi.com/2076-3417/16/7/3227) | 检测-跟踪去重后按 RGB/多光谱特征识别成熟度并统计不同成熟阶段的番茄数量。（范围：A） | Appl. Sci. | 未核验 |
| [Simultaneous Maturity Recognition and Yield Counting of Truss and Individual Tomatoes Using Improved YOLOv8-EME and Optimized ByteTrack Tracker](https://www.mdpi.com/2311-7524/12/10/1199) | YOLOv8-EME 与优化 ByteTrack 同时识别番茄串、单果成熟度并分别计数。（范围：A） | Horticulturae | 未核验 |
| [A lightweight multi-view detection and counting method for real-time cherry tomato yield estimation using greenhouse inspection robots](https://www.sciencedirect.com/science/article/pii/S2772375526004843) | 面向巡检机器人的轻量检测-跟踪-计数-补偿管线，使用多视角信息减少遮挡导致的漏计。（范围：A/B） | SAT | 未核验 |
| [Video-based fruit detection and tracking: effects of scanning conditions on fruit load estimation](https://doi.org/10.1016/j.compag.2026.112330) | 在 420 棵苹果树上比较 RGB-D 相机、扫描距离、日期和单/双侧扫描对视频计数、采收真值与负载图的影响。（范围：A/B） | CEA | [论文数据/代码声明所列作者仓库](https://github.com/imatge-upc/VideoFruitCounting) |
| [BerryFlowerNet: A Customized Convolutional Neural Network for Blueberry Flower Cluster Detection and Flowering Stage Prediction with a Field Phenotyping Robot](https://www.mdpi.com/2077-0472/16/11/1159) | 以田间表型机器人采集蓝莓从花蕾至绿果阶段图像，检测并计数花簇、预测花期；属成熟果计数前的生殖负载代理。（范围：P） | Agriculture | [作者实验室代码与数据](https://github.com/UGA-BSAIL/BerryFlowerNet) |
| [Unified Multi-Level Grape Counting Framework with Low Annotation Cost for Natural Orchard Scenes](https://doi.org/10.3390/app16157500) | UniGC 统一完成可见葡萄粒点计数、葡萄串检测/计数及逐串粒数估计，训练仅需点和框标注。（范围：A） | Appl. Sci. | [作者代码与数据](https://github.com/xiaofengxie-dl/UniGC) |

</details>

<details>
<summary>遥感/航拍计数 · 10 篇</summary>

| 论文题目 | 摘要（中文释义） | 刊会简称 | 代码 |
| --- | --- | --- | --- |
| [See What We Cannot See: A Geo-guided Reasoning Benchmark for Object Counting under Adverse Earth Observation Conditions (GROC)](https://openaccess.thecvf.com/content/CVPR2026/html/Wang_See_What_We_Cannot_See_A_Geo-guided_Reasoning_Benchmark_for_CVPR_2026_paper.html) | 【遥感计数/基准】评测地理辅助信息在云雾、阴影和低照等不利观测下对目标计数的作用。 | CVPR | [基准代码](https://github.com/jwang-rs/GROC) |
| [SCOUT-Count: Stylization with covariance-whitening and uncertainty for domain-generalized remote sensing object counting](https://www.sciencedirect.com/science/article/abs/pii/S0924271626003369) | 【遥感计数】结合风格扩增、协方差白化和不确定性建模，缓解跨地域、跨分辨率域偏移。 | ISPRS JPRS | [论文代码](https://github.com/WindermerePeaks/SCOUT-Count) |
| [RS-OVC: Open-Vocabulary Counting for Remote-Sensing Data](https://arxiv.org/abs/2604.08704) | 【遥感开放计数】以文本或视觉提示指定卫星/航拍目标，支持训练中未见类别。 | ICPR | [官方代码](https://github.com/tamirshor7/RS-OVC) |
| [GACENet: Global Adaptive Context Enhancement Network for Remote Sensing Object Counting](https://doi.org/10.1109/TGRS.2026.3679358) | 【遥感计数】通过全局自适应上下文增强，处理大视场影像中的密度变化与尺度差异。 | IEEE TGRS | 未找到官方模型代码 |
| [S2C-Net: Scale-Sensitive Contextual Counting Network for Remote Sensing Images](https://doi.org/10.1109/TGRS.2026.3693659) | 【遥感计数】以尺度敏感上下文聚合处理遥感密集计数中的目标尺寸变化。 | IEEE TGRS | [作者仓库](https://github.com/xuptLHj/S2C-Net)（复现完整性未验证） |
| [Scale-Aware Gated Routing Distillation Network for Remote Sensing Object Counting (SAGRD)](https://doi.org/10.3390/rs18172939) | 【遥感计数】利用尺度感知门控路由与蒸馏增强遥感多尺度目标计数。 | Remote Sens. | 未找到官方模型代码 |
| [HierarchicalGeoCount: Hierarchical Geometric Feature Learning for Zero-Shot Remote Sensing Object Counting](https://doi.org/10.1016/j.jvcir.2026.104793) | 【遥感开放计数】通过层级几何特征迁移至训练中未见的遥感目标类别。 | J. Vis. Commun. Image Represent. | 未找到官方模型代码 |
| [TreeMatch: Tree-Structured Matching for Cross-Domain Object Counting](https://arxiv.org/abs/2606.24786) | 【跨域/遥感计数】以树结构匹配处理域偏移，并在遥感/航拍场景评测。 | ECCV | [作者代码与数据](https://github.com/dgominski/treematch) |
| [COBICount: Counting Objects in the Wild with Contextual Bias Mitigation](https://arxiv.org/abs/2609.39366) | 【跨域计数】针对复杂背景和域变化抑制上下文偏置，包含遥感场景评测。 | arXiv 预印本 | 未找到公开官方代码 |
| [VesselBench-800K: A Large-Scale Benchmark for Vessel Detection and Counting in Satellite Imagery](https://arxiv.org/abs/2609.37003) | 【遥感计数基准】发布卫星船舶检测与计数数据基准，侧重数据集和评测资源。 | arXiv 预印本 | 论文所指仓库当前不可访问 |

</details>

<details>
<summary>开放词汇/开放世界计数 · 12 篇</summary>

| 论文题目 | 摘要（中文释义） | 刊会简称 | 代码 |
| --- | --- | --- | --- |
| [CountGD++: Generalized Prompting for Open-World Counting](https://arxiv.org/abs/2512.23351) | 【开放计数】组合正/负文本与视觉提示和伪示例，增强复杂目标指定和开放世界泛化。 | CVPR | [官方代码](https://github.com/niki-amini-naieni/CountGDPlusPlus) |
| [Boosting Quantitive and Spatial Awareness for Zero-Shot Object Counting (QICA)](https://openaccess.thecvf.com/content/CVPR2026/papers/Zhang_Boosting_Quantitive_and_Spatial_Awareness_for_Zero-Shot_Object_Counting_CVPR_2026_paper.pdf) | 【开放计数】以数量—空间感知特征聚合改善 CLIP 零样本计数的定位与数量估计。 | CVPR | 论文所指代码仓库当前不可访问 |
| [CountEx: Fine-Grained Counting via Exemplars and Exclusion](https://arxiv.org/abs/2602.19432) | 【开放计数】以正示例指定目标、负示例或文本排除相似类别，并提出 CoCount 基准。 | ECCV | [官方代码与基准](https://github.com/bbvisual/CountEx) |
| [RT-Counter: Real-Time Text-Guided Open-Vocabulary Object Counting](https://arxiv.org/abs/2606.17561) | 【开放计数】以视觉原型文本化和轻量交织 Transformer 改进文本—目标对齐；论文报告 FSC-147 上 112.48 FPS。 | arXiv 预印本 | [作者代码](https://github.com/Jason-Mar1/RT-Counter) |
| [MambaCount: Efficient Text-guided Open-vocabulary Object Counting with Spatial Sparse State Space Duality Block](https://arxiv.org/abs/2606.17650) | 【开放计数】将文本引导计数与稀疏状态空间模块结合，目标是在较低计算量下保留空间结构。 | arXiv 预印本 | 未找到官方代码 |
| [Test-Time Training for Robust Text-Guided Open-Vocabulary Object Counting (Dual-TTT)](https://arxiv.org/abs/2606.17601) | 【开放计数】研究测试时适应，缓解文本指定类别变化导致的分布偏移。 | arXiv 预印本 | 未确认公开官方代码 |
| [Count Anything](https://arxiv.org/abs/2605.30846) | 【跨域开放计数】提出文本计数模型与 CLOC 基准，覆盖通用、遥感、农业及显微等场景。 | arXiv 预印本 | [作者代码、模型与配置](https://github.com/Mengqi-Lei/count-anything) |
| [Count Anything at Any Granularity](https://arxiv.org/abs/2605.10887) | 【开放计数】通过视觉示例、细粒度文本和负提示指定实例/属性/类别等不同粒度，并提出 HieraCount。 | arXiv 预印本 | [项目与数据资源](https://verg-avesta.github.io/KubriCount/)（模型训练代码未确认） |
| [TPECount: Text-guided Patch-level Exemplar Selection for Zero-Shot Counting](https://doi.org/10.1016/j.engappai.2026.113986) | 【开放计数】按文本提示选择 patch 级视觉示例，增强零样本计数的检索与空间定位。 | Eng. Appl. AI | [作者代码](https://github.com/aHui3/TPECount) |
| [Towards Generalizable Object Counting via Dual-Prompted Cross-Modality Fusion Network (DCFNet)](https://doi.org/10.1016/j.inffus.2025.103837) | 【开放计数】融合文本与框提示，通过跨模态语义和空间交互提升泛化。 | Inf. Fusion | [作者代码](https://github.com/wzzhai/DCFNet) |
| [PD-count: Prompt-driven Zero-shot Object Counting with Dynamic Frequency Transformation](https://doi.org/10.1016/j.eswa.2026.131295) | 【开放计数】结合提示条件视觉—语言特征与动态频域变换，预测零样本目标密度图。 | ESWA | 未找到官方代码 |
| [DualCount: Structurally Consistent Density and Point Modeling for Zero-Shot Object Counting](https://link.springer.com/book/10.1007/978-3-032-37335-9?page=1) | 【开放计数】联合密度图和实例点建模，以质量守恒及质心对齐约束改善计数。 | ECCV | 未找到官方代码 |

</details>

<details>
<summary>类无关/少样本/示例驱动计数 · 5 篇</summary>

| 论文题目 | 摘要（中文释义） | 刊会简称 | 代码 |
| --- | --- | --- | --- |
| [Generalized-Scale Object Counting with Gradual Query Aggregation (GeCo2)](https://ojs.aaai.org/index.php/AAAI/article/view/37780) | 【类无关/少样本】渐进聚合多尺度示例查询，在免切块条件下处理密集小目标。 | AAAI | [官方代码](https://github.com/jerpelhan/GECO2) |
| [CountingDINO: A Training-free Pipeline for Class-Agnostic Counting using Unsupervised Backbones](https://openaccess.thecvf.com/content/WACV2026/html/Pacini_CountingDINO_A_Training-free_Pipeline_for_Class-Agnostic_Counting_using_Unsupervised_Backbones_WACV_2026_paper.html) | 【类无关计数】利用自监督 DINO 特征与示例原型，在推理时无需额外训练即可计数。 | WACV | [官方代码](https://github.com/lorebianchi98/CountingDINO) |
| [Bootstrapping MLLM for Weakly-Supervised Class-Agnostic Object Counting (WS-COC)](https://arxiv.org/abs/2602.12774) | 【弱监督/类无关计数】以图像级数量监督引导 MLLM 计数，减少点级标注依赖；并非文本开放词汇计数。 | ICLR | [作者代码](https://github.com/viscom-tongji/WS-COC) |
| [OCCAM: Class-Agnostic, Training-Free, Prior-Free and Multi-Class Object Counting](https://arxiv.org/abs/2601.13871) | 【类无关计数】结合 SAM2 与聚类，探索无训练、无示例的多类别计数。 | arXiv 预印本 | [项目页](https://mikespanak.github.io/OCCAM_counter)（未确认可用实现） |
| [Spatially-Aware Class-Agnostic Object Counting (UpCount)](https://arxiv.org/abs/2607.16826) | 【类无关计数】以多层 ViT 特征、空间细化和候选验证处理结构复杂目标。 | arXiv 预印本 | [作者代码](https://github.com/r28112072-rgb/upcount) |

</details>

<details>
<summary>视频目标计数 · 3 篇</summary>

| 论文题目 | 摘要（中文释义） | 刊会简称 | 代码 |
| --- | --- | --- | --- |
| [Open-World Object Counting in Videos (CountVid)](https://ojs.aaai.org/index.php/AAAI/article/view/37214) | 【开放视频计数】用文本或图像示例指定目标，跨帧跟踪去重并统计视频中出现过的唯一实例。 | AAAI | [官方代码与数据](https://github.com/niki-amini-naieni/CountVid) |
| [Depth-Guided Video Object Counting in Crowded Scenes](https://arxiv.org/abs/2608.06236) | 【开放视频计数】融合 RGB-D、文本/视觉提示和跨帧去重，面向遮挡拥挤视频目标计数。 | ACM MM | [作者代码](https://github.com/streamer-AP/DG-Net) · [数据集](https://huggingface.co/datasets/aerospace123/RGBD-VideoCount) |
| [SAM3Count: Zero-Shot Open Vocabulary Counting in Images and Videos](https://openreview.net/pdf?id=t3NZw67uAM) | 【开放图像/视频计数】以 SAM3 对文本指定目标计数并支持大图切块；为 CVPR workshop 论文。 | CVPRW | [部分推理/演示代码](https://github.com/Joan947/SAM3Count)（训练代码待发布） |

</details>

<details>
<summary>计数基准/推理/生成控制 · 3 篇</summary>

| 论文题目 | 摘要（中文释义） | 刊会简称 | 代码 |
| --- | --- | --- | --- |
| [The MixCount Dataset: Bridging the Data Gap for Open-Vocabulary Object Counting](https://arxiv.org/abs/2605.18063) | 【开放计数基准】构建同图多类、易混目标的合成数据与细粒度标注，侧重数据资源而非新计数器。 | arXiv 预印本 | [数据集](https://huggingface.co/datasets/CorentinDumery/MixCount)；未确认模型代码 |
| [UNICBench: UNIfied Counting Benchmark for MLLM](https://openaccess.thecvf.com/content/CVPR2026/html/Rong_UNICBench_UNIfied_Counting_Benchmark_for_MLLM_CVPR_2026_paper.html) | 【计数基准】统一评估多模态大语言模型的计数能力，不是专用开放词汇计数器。 | CVPR | 未确认官方代码 |
| [Mitigating Noise-Induced Layout Priors for Object Counting in Diffusion Models](https://proceedings.mlr.press/v306/gu26f.html) | 【计数与生成】调节扩散噪声和早期注意力布局，让文生图结果符合提示数量；非已有图像实例计数。 | ICML | [论文所列代码](https://github.com/lxlong1201/Mitigate_Noise_Prior) |

</details>

</details>

### 果园估产综述（背景阅读，不计入年度原始研究计数）

| 论文题目 | 摘要（中文释义） | 刊会简称 | 代码 |
| --- | --- | --- | --- |
| [A review: research progress on intelligent technologies for orchard yield monitoring](https://www.frontiersin.org/journals/plant-science/articles/10.3389/fpls.2026.1879872/full) | 总结 RGB/RGB-D、LiDAR、多/高光谱、UGV/UAV 与目标检测、实例分割、多目标跟踪、点云和多模态融合，将果数/负载监测作为产量监测中间环节。 | Front. Plant Sci. | — |
| [Research progress on precision orchard yield estimation based on multi-source information perception sensors](https://www.frontiersin.org/journals/plant-science/articles/10.3389/fpls.2026.1759956/full) | 依 PRISMA 思路综述机器视觉、光谱遥感、多源融合与果园平台；指出融合有助提升稳健性，但遮挡、数据异质性和跨场景适配仍是难点。 | Front. Plant Sci. | — |

</details>

---

<a id="micro-expression"></a>
## 03 · 微表情识别

<details>
<summary><strong>展开年度目录 · 22 篇（2021–2026）</strong></summary>

**按年直达：** [2021](#micro-year-2021) · [2022](#micro-year-2022) · [2023](#micro-year-2023) · [2024](#micro-year-2024) · [2025](#micro-year-2025) · [2026](#micro-year-2026)

<details id="micro-year-2021">
<summary>2021 · 0 篇</summary>

该年份暂无已收录论文。

</details>

<details id="micro-year-2022">
<summary>2022 · 0 篇</summary>

该年份暂无已收录论文。

</details>

<details id="micro-year-2023">
<summary>2023 · 0 篇</summary>

该年份暂无已收录论文。

</details>

<details id="micro-year-2024">
<summary>2024 · 0 篇</summary>

该年份暂无已收录论文。

</details>

<details id="micro-year-2025">
<summary>2025 · 11 篇</summary>

### 时空运动表征与多尺度特征建模 · 6 篇

| 论文题目 | 摘要（中文释义） | 刊会简称 | 代码 |
| --- | --- | --- | --- |
| [High-level LoRA and Hierarchical Fusion for Enhanced Micro-Expression Recognition](https://doi.org/10.1007/s00371-024-03676-w) | 将视觉基础模型的高层 LoRA 微调与层级融合结合，聚合帧间及时空特征，以较少可训练参数提升微表情识别。 | The Visual Computer | [Code](https://github.com/CYF-cuber/HLoRA_MER_dinov2) |
| [MOL: Joint Estimation of Micro-Expression, Optical Flow, and Landmark via Transformer-Graph-Style Convolution](https://arxiv.org/abs/2506.14511) | 以原始帧端到端学习局部—全局特征，并联合微表情识别、光流估计与人脸关键点检测。 | TPAMI | [Code](https://github.com/CYF-cuber/MOL) |
| [Micro-Expression Recognition via Fine-Grained Dynamic Perception](https://doi.org/10.1145/3765901) | 以局部—全局 Transformer 和排序池化提取动态表示，并用动态影像辅助任务缓解小样本问题。 | ACM TOMM | [Code](https://github.com/CYF-cuber/FDP) |
| [Entire-detail Motion Dual-Branch Network for Micro-Expression Recognition](https://doi.org/10.1016/j.patrec.2025.01.021) | 双分支分别建模整体运动与局部细节运动，结合累积注意力聚焦关键面部区域。 | PRL | [Code](https://github.com/likemby/EDMDBN) |
| [HFA-Net: Hierarchical Feature Aggregation Network for Micro-Expression Recognition](https://doi.org/10.1007/s40747-025-01804-0) | 局部分支提取多尺度细微变化，全局分支建模面部结构关系，再跨层聚合融合。 | C&IS | [Code](https://github.com/tairuwu/HFA-Net) |
| [M³ENet: A Multi-Modal Fusion Network for Efficient Micro-Expression Recognition](https://doi.org/10.3390/s25206276) | 融合关键帧 RGB 外观与多类光流，并用增强和 focal loss 应对小样本与类别不平衡。 | Sensors | [Code](https://github.com/xuanyv/M3ENet) |

### AU 先验、语义对齐与多模态理解 · 3 篇

| 论文题目 | 摘要（中文释义） | 刊会简称 | 代码 |
| --- | --- | --- | --- |
| [FED-PsyAU: Privacy-Preserving Micro-Expression Recognition via Psychological AU Coordination and Dynamic Facial Motion Modeling](https://openaccess.thecvf.com/content/ICCV2025/html/Li_FED-PsyAU_Privacy-Preserving_Micro-Expression_Recognition_via_Psychological_AU_Coordination_and_Dynamic_ICCV_2025_paper.html) | 将上下脸动作单元协同先验融入分层图注意力，并在联邦学习中跨客户端训练。 | ICCV | [Code](https://github.com/MELABIPCAS/FED-PsyAU) |
| [MER-CLIP: AU-Guided Vision-Language Alignment for Micro-Expression Recognition](https://doi.org/10.1109/TAFFC.2025.3584918) | 将 AU 转写为面部运动描述，与视频表征做 CLIP 式跨模态对齐，并加入情绪推断和面部混合增强。 | TAFFC | [Code](https://github.com/Liusff/MER-CLIP) |
| [MELLM: Exploring LLM-Powered Micro-Expression Understanding Enhanced by Subtle Motion Perception](https://arxiv.org/abs/2505.07007) | 融合 onset–apex 光流与灰度帧，结合多模态大模型探索细粒度微表情理解。 | arXiv | [Code](https://github.com/zyzhangUstc/MELLM) |

### 关键帧鲁棒性 · 1 篇

| 论文题目 | 摘要（中文释义） | 刊会简称 | 代码 |
| --- | --- | --- | --- |
| [Rethinking Key-frame-based Micro-expression Recognition: A Robust and Accurate Framework Against Key-frame Errors](https://openaccess.thecvf.com/content/ICCV2025/html/Zhang_Rethinking_Key-frame-based_Micro-expression_Recognition_A_Robust_and_Accurate_Framework_Against_ICCV_2025_paper.html) | 以完整序列和 AU 相关运动建模降低关键帧标注误差影响，提升微表情识别鲁棒性。 | ICCV | [Code](https://github.com/tony19980810/CausalNet) |

### 联合定位与识别 · 1 篇

| 论文题目 | 摘要（中文释义） | 刊会简称 | 代码 |
| --- | --- | --- | --- |
| [Boosting Micro-Expression Analysis via Prior-Guided Video-Level Regression](https://doi.org/10.1145/3746027.3762026) | 以视频级回归统一微表情定位与识别，按时间演化和持续时长选择区间，并共享任务表征。 | ACM MM | [Code](https://github.com/zizheng-guo/BoostingVRME) |

</details>

<details id="micro-year-2026">
<summary>2026 · 11 篇</summary>

### 动态运动建模与高效识别 · 6 篇

| 论文题目 | 摘要（中文释义） | 刊会简称 | 代码 |
| --- | --- | --- | --- |
| [Temporal–Spatial Cross-Fusion for Dynamic Micro Expression Recognition](https://doi.org/10.1016/j.patcog.2026.113715) | 结合 RetNet 与 Transformer 并行融合时空特征，显式建模微表情发生位置及其变化。 | Pattern Recogn. | [Code](https://github.com/Cross-Innovation-Lab/TSFmicro) |
| [DBDE-Net: Dual-Branch Detail-Enhanced Network for Micro-Expression Recognition](https://doi.org/10.1016/j.neucom.2026.133167) | 双支路分别建模 onset–apex 局部细节与完整序列，并用运动注意力增强弱纹理。 | Neurocomputing | [Code](https://github.com/Binghr-08/DBDENet) |
| [MPFNet: A Multi-Prior Fusion Network with a Progressive Training Strategy for Micro-Expression Recognition](https://doi.org/10.1109/TAFFC.2025.3617652) | 以 I3D 和坐标注意力双编码器逐步融合多类先验，提供并行与层级两种融合策略。 | TAFFC | [Code](https://github.com/Mac0504/MPFNet) |
| [Modeling the Evolution Dynamics to Enhance Micro-Expression Recognition](https://doi.org/10.1007/s11704-025-40976-3) | 用 Transformer 建模完整表情序列的动态演化，并结合光流、面部校正和 AU 区域定位。 | Front. Comput. Sci. | [Code](https://github.com/hitheyuhong/TA_MER_FOR_CCAC) |
| [Micro-expression Recognition Based on Adaptive Amplification of Dynamic Weak Texture Information](https://doi.org/10.1016/j.cviu.2026.104904) | 自适应放大微表情弱纹理，再用多尺度通道—空间模块提取局部细节完成分类。 | CVIU | [Code](https://github.com/cxhwxhn/AA-DWT-MER) |
| [SOFP: Capturing Subtle Facial Dynamics with Symmetric Optical Flow Perception for Micro-Expression Recognition](https://doi.org/10.1016/j.patcog.2026.113199) | 将光流划分为双侧对称区域，以注意力编码局部与全局运动，并融合区域关系。 | Pattern Recogn. | [Code](https://github.com/Healer-ML/MER) |

### AU 语义、文本—视觉对齐与动作编码 · 1 篇

| 论文题目 | 摘要（中文释义） | 刊会简称 | 代码 |
| --- | --- | --- | --- |
| [From Pixels to Semantics: Unified Facial Action Representation Learning for Micro-Expression Analysis](https://proceedings.iclr.cc/paper_files/paper/2026/hash/ac56fb3fab015124b541f6299016a21c-Abstract-Conference.html) | 以离散面部动作 token 表示像素运动，并用稀疏 Transformer 与情绪文本锚点辅助识别。 | ICLR | [Code（部分实现）](https://github.com/KinopioIsAllIn/D-FACE) |

### 标注质量与识别可靠性 · 2 篇

| 论文题目 | 摘要（中文释义） | 刊会简称 | 代码 |
| --- | --- | --- | --- |
| [Evaluating and Correcting Human Annotation Bias in Dynamic Micro-Expression Recognition](https://doi.org/10.1109/TAFFC.2026.3671731) | 根据完整序列重选关键帧，评估并缓解人工标注偏差，提供多数据集训练实现。 | TAFFC | [Code](https://github.com/Cross-Innovation-Lab/GAMDSS) |
| [Where and How Well: Reliability-Guided Dual-View Displacement Learning for Micro-Expression Recognition](https://github.com/cszyzhang/DVAW) | 联合学习 onset→apex 与 offset→apex 位移并预测可靠性，以双视角形变增强识别。 | ACM MM* | [Code（含权重/评测材料）](https://github.com/cszyzhang/DVAW) |

### 长视频定位识别与持续/增量学习 · 2 篇

| 论文题目 | 摘要（中文释义） | 刊会简称 | 代码 |
| --- | --- | --- | --- |
| [ME-TST+: Micro-Expression Analysis via Temporal State Transition With ROI Relationship Awareness](https://doi.org/10.1109/TCSVT.2026.3682021) | 以视频级回归处理长视频，结合多粒度 ROI 与 SlowFast-Mamba 联合优化定位和情绪识别。 | TCSVT | [Code](https://github.com/zizheng-guo/ME-TST) |
| [Incremental Micro-Expression Recognition: A Benchmark](https://doi.org/10.1109/TAFFC.2026.3680615) | 建立微表情增量识别协议和六类基线，评估持续适应新数据及保留旧知识的能力。 | TAFFC | [Code](https://github.com/ZhengQinLai/IMER-benchmark) |

> *DVAW 的 ACM MM 2026 venue 信息按作者仓库核验；截至检索日未找到可独立核对的 ACM DL 条目。D-FACE 仓库实现尚不完整，详见[专题页](papers/micro-expression-recognition.md)。*

</details>

### 数据集与采集信息

采集设备、帧率、样本规模、被试划分与标注设置待逐项核验后补充；目前不虚列未核验数据。

</details>
