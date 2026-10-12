# 微表情识别

[返回三方向论文总览](README.md) · [跨模态检索目录](../README.md) · [果实计数目录](fruit-counting.md)

> 本页整理微表情识别相关研究，区分正式发表、预印本及数据集/代码资源，并记录采集设备与帧率等关键信息。

## 主题范围

- 微表情检测、识别与时空定位
- 动作单元、光流及时空特征建模
- 小样本、自监督、弱监督与跨域泛化
- 跨数据库评测、类别不平衡与开放集识别
- 数据集、采集设备、帧率、标注和伦理规范

## 论文目录

| 论文题目 | 摘要（中文释义） | 期刊简称 | 年份 | 论文 / 代码 |
|---|---|---|---:|---|
| SOFP: Capturing Subtle Facial Dynamics with Symmetric Optical Flow Perception for Micro-Expression Recognition | 将光流划分为四个双侧对称面部区域，以注意力编码器提取局部与全局运动；通过对称区域感知融合模块建模区域一致性和交互关系，在多个微表情数据库上评测。 | Pattern Recogn. | 2026 | [论文](https://doi.org/10.1016/j.patcog.2026.113199) · [Code](https://github.com/Healer-ML/MER) |

## 2025–2026 有代码论文（按年份与方法方向）

以下条目优先按正式出版年份归档；尚未正式发表的工作按预印本首次发布年份归档。检索截止 **2026-10-12**；“代码已核验”表示能访问作者/项目仓库并确认存在模型、训练、测试或评测实现，不代表已在本地逐项复现实验。既有 SOFP 条目保留在上表，不重复列入下表。

### 2025

#### 时空运动表征与多尺度特征建模

| 论文题目 | 摘要（中文释义） | 期刊/会议简称 | 代码核验 |
|---|---|---|---|
| [High-level LoRA and Hierarchical Fusion for Enhanced Micro-Expression Recognition](https://doi.org/10.1007/s00371-024-03676-w) | 将视觉基础模型的高层 LoRA 微调与层级融合结合，聚合帧间及空时特征，以较少可训练参数提升微表情识别。 | The Visual Computer | [作者代码](https://github.com/CYF-cuber/HLoRA_MER_dinov2)（训练实现） |
| [MOL: Joint Estimation of Micro-Expression, Optical Flow, and Landmark via Transformer-Graph-Style Convolution](https://arxiv.org/abs/2506.14511) | 以原始帧端到端学习局部—全局特征，并联合微表情识别、光流估计与人脸关键点检测，减少对人工关键帧的依赖。 | TPAMI | [作者代码](https://github.com/CYF-cuber/MOL)（训练/测试实现） |
| [Micro-Expression Recognition via Fine-Grained Dynamic Perception](https://doi.org/10.1145/3765901) | 按时间顺序排序帧级特征，以局部—全局 Transformer 和排序池化提取动态表示，并用动态影像构造辅助任务缓解小样本问题。 | ACM TOMM | [作者代码](https://github.com/CYF-cuber/FDP)（数据处理、训练实现） |
| [Entire-detail Motion Dual-Branch Network for Micro-Expression Recognition](https://doi.org/10.1016/j.patrec.2025.01.021) | 双分支分别建模整体运动和局部细节运动，结合带累积注意力的 Swin Transformer 聚焦关键面部区域。 | PRL | [作者代码](https://github.com/likemby/EDMDBN)（模型、训练与配置） |
| [HFA-Net: Hierarchical Feature Aggregation Network for Micro-Expression Recognition](https://doi.org/10.1007/s40747-025-01804-0) | 局部分支用多尺度注意力捕获细微变化，全局分支用 Retentive Memory Transformer 建模结构关系，再跨层聚合并自适应融合。 | C&IS | [作者代码](https://github.com/tairuwu/HFA-Net)（公开实现） |
| [M³ENet: A Multi-Modal Fusion Network for Efficient Micro-Expression Recognition](https://doi.org/10.3390/s25206276) | 融合起始/顶点/结束帧 RGB 外观与水平、垂直及应变光流，并用数据增强和 focal loss 应对小样本与类别不平衡。 | Sensors | [作者代码](https://github.com/xuanyv/M3ENet)（公开实现） |

#### AU 先验、语义对齐与多模态理解

| 论文题目 | 摘要（中文释义） | 期刊/会议简称 | 代码核验 |
|---|---|---|---|
| [FED-PsyAU: Privacy-Preserving Micro-Expression Recognition via Psychological AU Coordination and Dynamic Facial Motion Modeling](https://openaccess.thecvf.com/content/ICCV2025/html/Li_FED-PsyAU_Privacy-Preserving_Micro-Expression_Recognition_via_Psychological_AU_Coordination_and_Dynamic_ICCV_2025_paper.html) | 将心理学中的上下脸动作单元协同先验与统计 AU 模式融入分层图注意力，并在联邦学习中跨客户端训练而不共享原始视频。 | ICCV | [作者代码](https://github.com/MELABIPCAS/FED-PsyAU)（公开实现） |
| [MER-CLIP: AU-Guided Vision-Language Alignment for Micro-Expression Recognition](https://doi.org/10.1109/TAFFC.2025.3584918) | 将 AU 标注转写为面部肌肉运动描述，与视频表征进行 CLIP 式跨模态对齐，并加入情绪推断模块和面部混合增强。 | TAFFC | [作者代码](https://github.com/Liusff/MER-CLIP)（配置、训练/测试实现） |
| [MELLM: Exploring LLM-Powered Micro-Expression Understanding Enhanced by Subtle Motion Perception](https://arxiv.org/abs/2505.07007) | 将 onset–apex 光流与灰度帧融合成运动增强输入，结合多模态大模型和基于 FACS/情绪标签构建的指令数据，探索细粒度微表情理解。 | arXiv 预印本 | [作者代码](https://github.com/zyzhangUstc/MELLM)（项目仓库公开） |

#### 关键帧鲁棒性

| 论文题目 | 摘要（中文释义） | 期刊/会议简称 | 代码核验 |
|---|---|---|---|
| [Rethinking Key-frame-based Micro-expression Recognition: A Robust and Accurate Framework Against Key-frame Errors](https://openaccess.thecvf.com/content/ICCV2025/html/Zhang_Rethinking_Key-frame-based_Micro-expression_Recognition_A_Robust_and_Accurate_Framework_Against_ICCV_2025_paper.html) | CausalNet 输入完整微表情序列，以 AU 相关运动定位减少冗余，并建模肌肉收缩—舒张关系，针对关键帧索引噪声提升鲁棒性。 | ICCV | [作者代码](https://github.com/tony19980810/CausalNet)（训练、评测及示例权重） |

#### 联合定位与识别

| 论文题目 | 摘要（中文释义） | 期刊/会议简称 | 代码核验 |
|---|---|---|---|
| [Boosting Micro-Expression Analysis via Prior-Guided Video-Level Regression](https://doi.org/10.1145/3746027.3762026) | 以视频级回归统一微表情定位与识别，通过可扩展区间选择刻画表情的时间演化、持续时间和类别分布，并让定位与识别任务共享主体参数。 | ACM MM | [作者代码](https://github.com/zizheng-guo/BoostingVRME)（含训练/推理脚本；数据和预训练权重另行获取） |

### 2026

#### 动态运动建模与高效识别

| 论文题目 | 摘要（中文释义） | 期刊/会议简称 | 代码核验 |
|---|---|---|---|
| [Temporal–Spatial Cross-Fusion for Dynamic Micro Expression Recognition](https://doi.org/10.1016/j.patcog.2026.113715) | TSFmicro 将 RetNet 与 Transformer 结合，并行融合时间动态和空间特征，以显式建模“何处发生、如何变化”的互补信息。 | Pattern Recogn.（online first） | [作者代码](https://github.com/Cross-Innovation-Lab/TSFmicro)（模型实现） |
| [DBDE-Net: Dual-Branch Detail-Enhanced Network for Micro-Expression Recognition](https://doi.org/10.1016/j.neucom.2026.133167) | 一支提取 onset–apex 差分中的局部细节，另一支建模完整采样序列；通过垂直运动注意力和细节增强卷积改善弱运动表征。 | Neurocomputing | [作者代码](https://github.com/Binghr-08/DBDENet)（模型与训练代码） |
| [MPFNet: A Multi-Prior Fusion Network with a Progressive Training Strategy for Micro-Expression Recognition](https://doi.org/10.1109/TAFFC.2025.3617652) | 以 I3D 和坐标注意力构建通用/增强双编码器，并用渐进训练整合多种先验；提供并行融合与层级融合两种方案。 | TAFFC | [作者代码](https://github.com/Mac0504/MPFNet)（模型、光流处理和训练相关脚本） |
| [Modeling the Evolution Dynamics to Enhance Micro-Expression Recognition](https://doi.org/10.1007/s11704-025-40976-3) | 用五层 Transformer 建模完整表情序列的动态演化，并结合光流、面部校正和 AU 区域定位；重点评测 CAS(ME)³、DFME 等数据。 | Front. Comput. Sci. | [作者代码](https://github.com/hitheyuhong/TA_MER_FOR_CCAC)（训练代码） |
| [Micro-expression Recognition Based on Adaptive Amplification of Dynamic Weak Texture Information](https://doi.org/10.1016/j.cviu.2026.104904) | 自适应放大微表情弱纹理运动，再用多尺度通道—空间特征模块提取局部细节并完成分类。 | CVIU | [作者代码](https://github.com/cxhwxhn/AA-DWT-MER)（含模型、数据工具与训练脚本） |

#### AU 语义、文本—视觉对齐与动作编码

| 论文题目 | 摘要（中文释义） | 期刊/会议简称 | 代码核验 |
|---|---|---|---|
| [From Pixels to Semantics: Unified Facial Action Representation Learning for Micro-Expression Analysis](https://proceedings.iclr.cc/paper_files/paper/2026/hash/ac56fb3fab015124b541f6299016a21c-Abstract-Conference.html) | D-FACE 用预训练离散面部动作 tokenizer 将像素运动编码为语义动作 token，再用稀疏注意力 Transformer 和情绪文本锚点辅助识别。 | ICLR | [作者代码](https://github.com/KinopioIsAllIn/D-FACE)（**部分实现**：仓库含模型/训练脚本；作者注明预训练细节仍在补充） |

#### 标注质量、可靠性与学习设置

| 论文题目 | 摘要（中文释义） | 期刊/会议简称 | 代码核验 |
|---|---|---|---|
| [Evaluating and Correcting Human Annotation Bias in Dynamic Micro-Expression Recognition](https://doi.org/10.1109/TAFFC.2026.3671731) | GAMDSS 根据完整序列动态重选关键帧，量化并缓解人工标注偏差，尤其关注跨文化数据中的关键帧误差；可作为模块集成到已有识别器。 | TAFFC | [作者代码](https://github.com/Cross-Innovation-Lab/GAMDSS)（多数据集训练脚本和模型实现） |
| [Where and How Well: Reliability-Guided Dual-View Displacement Learning for Micro-Expression Recognition](https://github.com/cszyzhang/DVAW) | DVAW 联合学习 onset→apex 与 offset→apex 位移，并预测位移可靠性，以双视角形变描述增强微表情运动识别。 | ACM MM* | [作者代码与复现包](https://github.com/cszyzhang/DVAW)（模型、权重、折级预测和指标脚本；不含原始/裁剪数据） |

#### 长视频定位识别与持续/增量学习

| 论文题目 | 摘要（中文释义） | 期刊/会议简称 | 代码核验 |
|---|---|---|---|
| [ME-TST+: Micro-Expression Analysis via Temporal State Transition With ROI Relationship Awareness](https://doi.org/10.1109/TCSVT.2026.3682021) | 将长视频微表情分析建模为视频级回归，以多粒度 ROI 和 SlowFast-Mamba 捕获短时细节与长时演化，并在特征和结果层联合优化定位与情绪识别。 | TCSVT | [作者代码](https://github.com/zizheng-guo/ME-TST)（含 ME-TST/ME-TST+ 实现） |
| [Incremental Micro-Expression Recognition: A Benchmark](https://doi.org/10.1109/TAFFC.2026.3680615) | 建立微表情增量识别设置，按数据集序列组织任务并设计两类跨评估协议，提供六种基线，研究数据持续到来时的适应与旧知识保持。 | TAFFC | [基准代码](https://github.com/ZhengQinLai/IMER-benchmark)（数据处理、增量基线与实验配置） |

> *DVAW 的 MM 2026 会议信息按作者仓库及作者主页的论文记录核验；截至本页核对日，尚未找到可独立核对的 ACM Digital Library 论文条目。代码仓库及其评测材料已确认公开，因此列入代码资源，但 venue 状态保留此说明。TSFmicro 已在线发表，出版方页面将其编入 2026 年第 179 卷后续期次。*

### 相关新论文：暂未核验到公开作者代码

以下论文与微表情识别高度相关，但截至 **2026-10-12** 未在论文页或作者公开仓库中确认可用实现，故不计入上面的代码论文数量；“未核验到”不等于作者未来不会开源。

- [Dynamic Stereotype Theory Induced Micro-expression Recognition with Oriented Deformation](https://openaccess.thecvf.com/content/CVPR2025/html/Zhang_Dynamic_Stereotype_Theory_Induced_Micro-expression_Recognition_with_Oriented_Deformation_CVPR_2025_paper.html) — CVPR 2025；SODA4MER 通过定向形变、自监督顶点帧定位及动态变化建模实现 apex-free 识别。
- [Region-Aware Instance Consistency Learning for Micro-Expression Recognition](https://openaccess.thecvf.com/content/CVPR2026/papers/Cai_Region-Aware_Instance_Consistency_Learning_for_Micro-Expression_Recognition_CVPR_2026_paper.pdf) — CVPR 2026；以多实例运动表征、区域注意一致性和可学习面部区域发现减少对人工 apex 标注的依赖；截至核对日未找到作者公开代码仓库。
- [R2-MER: Micro-Expression Recognition Via Region-Aware Reconstruction and Modality-Aware Fusion](https://ieeexplore.ieee.org/abstract/document/11702790/) — TAFFC 2026；自监督关键区域扰动预训练后融合静态外观与光流动态特征；本轮未找到作者代码链接。
- [A Micro-Expression Recognition Algorithm Fusing Visual Information with Textual Semantics](https://doi.org/10.1016/j.eswa.2025.129000) — ESWA 2026；构建 AU 文本描述，并以跨模态注意力融合视觉与 AU 语义；检索到正式论文页面，未核验到作者代码。
- [Regulatory Focus Theory Induced Micro-Expression Analysis with Structured Representation Learning](https://doi.org/10.1145/3746027.3755855) — ACM MM 2025；AC4AU 以结构化表征和 AU 专家路由做 apex-free 微表情动作单元分析；论文称代码可按请求提供，但截至核对日未找到公开代码仓库，且任务重点是 AU 检测/分析而非情绪类别识别。
- [TGRF-Net: Text-Semantic Guided Region Focused Network for Micro-Expression Recognition](https://doi.org/10.1109/TAFFC.2026.3688654) — TAFFC 2026；通过分层文本提示做视觉—语义交互，并用动态边界损失缓解类别不平衡；截至核对日未找到作者公开代码仓库。
- [Micro-Expression Analysis Based on Self-Adaptive Pseudo-Labeling and Residual Connected Channel Attention Mechanisms](https://doi.org/10.1109/TIP.2025.3642527) — TIP（2025 online / 2026 卷期）；STRM 联合长视频微表情定位与识别，用自适应伪标签及多尺度残差通道注意力提升弱运动建模；截至核对日未核验到公开作者代码。
- [AHAT-MER: Asymmetric Hourglass Attention Transformer Network for Micro-Expression Recognition](https://doi.org/10.1016/j.neucom.2026.133845) — Neurocomputing 2026；以非对称层级注意力捕获面部区域与局部运动，并通过监督对比约束稳定区域表征；截至核对日未核验到作者公开代码。

### 检索与代码核验口径

- 检索范围：2025–2026 年正式发表论文及相关预印本；优先核对出版社/会议论文页、arXiv 原文和作者代码仓库。
- 收录范围：微表情分类/识别、增量识别，以及直接增强识别输入/标注质量的方法；纯检测、纯 spotting、纯数据集或纯生成工作不作为核心识别条目。
- 代码判定：只有找到可访问的作者/项目仓库且存在实现文件或复现实验脚本才标记为“代码已核验”。不把仅有论文提及、第三方复现或仅有数据下载页当成作者代码。
- 复现边界：仓库公开不代表数据集可直接下载或许可证允许再分发；具体数据仍需按原数据集申请与许可获取。D-FACE、DVAW 的公开内容边界已在表中单列。

## 数据集与采集信息

数据集条目另标注采集设备、帧率、样本规模、被试划分和标注设置；待逐项核验后补充。
