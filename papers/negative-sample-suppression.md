# 跨模态对齐中的负样本抑制：假负样本识别与噪声鲁棒学习

[返回三方向论文总览](README.md) · [跨模态检索年度目录](../README.md#cross-modal) · [研究论文导航](README.md)

**检索与代码核验截止：2026-10-12。** 本专题聚焦图文/视觉语言检索中的假负样本（false negatives, FNs）：训练时未被标注为配对、却与锚点语义相关的图像—文本对。主表优先收录明确处理假负样本的会议论文；另列错误正配对/噪声对应方法，因为它们常被泛称为“负样本抑制”，但问题定义并不相同。中文摘要为内容释义。代码状态只在论文页、作者主页或与论文明确关联的作者仓库中核验；“本次未找到”不等于证明代码从未发布。

## 问题边界：先分清标签错在哪一边

| 问题 | 训练标签实际情况 | 典型后果 | 本专题如何归类 |
| --- | --- | --- | --- |
| **假负样本（FN）** | 未配对样本被当作负例，但两者实际语义相关/可检索 | 对比损失把语义相近样本推远，损害召回与语义结构 | **主线：识别、重标、降权或跳过假负样本** |
| **噪声正配对 / 假正例（FP）** | 被标为正例的图文对实际不匹配 | 错误配对把不同语义拉近 | 相邻问题：筛除、校正或重新匹配错误正例 |
| **局部负证据** | 词语—区域等局部片段确实不匹配 | 用错局部对应会抬高整对相似度 | 相关但不同：将不匹配片段作为判别线索，不代表全局假负样本抑制 |

因此，论文标题中出现 *negative*、方法涉及 *noisy correspondence*，并不自动表示它解决了假负样本。尤其是 noisy correspondence 工作往往重点是**错误正配对**；下文明确分栏，避免混作同一类。例如 [Negative-Aware Attention Framework for Image-Text Matching（CVPR·2022）](https://openaccess.thecvf.com/content/CVPR2022/html/Zhang_Negative-Aware_Attention_Framework_for_Image-Text_Matching_CVPR_2022_paper.html) 用局部词语—区域错配作为匹配判别证据，[作者代码](https://github.com/CrossmodalGroup/NAAF)可用；它不是全局假负样本抑制方法。

## 一、直接处理假负样本：核心论文与代码

| 论文（会议简称·年份） | 摘要与方法要点（中文释义） | 代码核验 |
| --- | --- | --- |
| [Your Negative May not Be True Negative: Boosting Image-Text Matching with False Negative Elimination](https://arxiv.org/abs/2308.04380) — **ACM MM·2023** | 针对图文匹配中“高相似未配对样本可能是假负例”的问题，FNE 根据锚点与样本的相似度估计正、负分布，再用贝叶斯后验作为负样本抽样权重；动量记忆库扩大候选负例范围，并降低简单负例权重以保留真正困难的负例。重点是**风险感知采样**，而非简单删除所有高相似样本。 | [作者代码仓库](https://github.com/LuminosityX/FNE)；仓库含训练、评估与损失实现。**已核验** |
| [Integrating Language Guidance Into Image-Text Matching for Correcting False Negatives](https://ieeexplore.ieee.org/abstract/document/10081045) — **TMM·2024**（2023 在线发表） | 将语言预训练模型用于发现标注为负、但可能语义匹配的图像；通过 Language Guidance Loss 自适应修正这些样本在视觉—语义嵌入空间中的位置。作者还在经过人工校正假负标注的 ECCV Caption 上验证模型找回相关样本的能力。 | [作者官方 PyTorch 实现](https://github.com/AAA-Zheng/LG_ITM)。**已核验** |
| [Cross-Modal and Uni-Modal Soft-Label Alignment for Image-Text Retrieval](https://ojs.aaai.org/index.php/AAAI/article/view/29789) — **AAAI·2024** | CUSA 从单模态预训练模型获取软标签，以 Cross-modal Soft-label Alignment（CSA）补充跨模态匹配关系，并以 Uni-modal Soft-label Alignment（USA）保存图像或文本内部的语义邻近关系；论文明确将其用于缓解假负样本造成的语义损失。方法可插入既有图文检索模型。 | [论文页提供的作者代码](https://github.com/lerogo/aaai24_itr_cusa)。**已核验** |
| [Improved Probabilistic Image-Text Representations](https://proceedings.iclr.cc/paper_files/paper/2024/hash/ad9d6ab10446114cf5482d5e1f971a84-Abstract-Conference.html) — **ICLR·2024** | PCME++ 用概率嵌入刻画图文匹配的不确定性与多重语义，改进概率距离以避免蒙特卡洛计算负担；进一步引入 pseudo-positives，缓解大量假负样本对匹配损失的伤害。论文在 MS-COCO、CxC、ECCV Caption 评测，并测试噪声对应鲁棒性。 | [NAVER AI 官方代码](https://github.com/naver-ai/pcmepp)。**已核验** |
| [MAFA: Managing False Negatives for Vision-Language Pre-training](https://openaccess.thecvf.com/content/CVPR2024/html/Byun_MAFA_Managing_False_Negatives_for_Vision-Language_Pre-training_CVPR_2024_paper.html) — **CVPR·2024** | 面向网络采集图文数据天然存在的一对多语义关系，先通过 connection mining 找出未标注的相关配对并将假负例转为正例，再对图文对比损失使用 label smoothing；结合分组小批次采样，改善视觉语言预训练，并考察下游检索等任务。 | [作者官方实现](https://github.com/jaeseokbyun/MAFA)；CVPR 论文页也给出仓库。**已核验** |
| [False Negatives Consensus Suppression for Text-to-Image Person Re-identification](https://doi.org/10.1109/ICME59968.2025.11209807) — **ICME·2025** | 面向文本搜行人图像，指出同一行人或语义高度相近的行人描述可能被当作负例。FNCD 以双粒度线索一致检测潜在假负样本，AFNS 再按样本自适应调整其相似度权重，以减轻错误排斥对细粒度图文对齐的影响。 | 检索到 IEEE 论文记录；**本次未找到可确认的作者公开代码仓库**。不把第三方目录或相似项目记作官方代码。 |
| [TriSim: Tri-Dimensional Similarity Modeling with Extreme Value Theory for False-Negative Mitigation in Remote Sensing Image-Text Retrieval](https://openaccess.thecvf.com/content/CVPR2026/html/Zheng_TriSim_Tri-Dimensional_Similarity_Modeling_with_Extreme_Value_Theory_for_False-Negative_CVPR_2026_paper.html) — **CVPR·2026** | 面向遥感图文检索，联合建模图—图、图—文、文—文三种相似度，避免仅凭单一跨模态阈值识别假负例；通过 Mahalanobis 距离与极值理论拟合尾部分布筛选候选，再用概率权重控制 triplet loss，并通过模态内显著区域差异强化判别特征。 | CVPR 官方论文页目前列出论文/PDF，未列代码；**本次未找到可确认的作者公开代码仓库**。 |

## 二、相邻但不同：错误正配对与噪声对应

这些方法值得和假负样本工作一起读，因为它们同样影响跨模态对齐；但它们主要解决“错误正例被拉近”，不能直接作为假负样本抑制方法统计。

| 论文（刊会简称·年份） | 摘要与和假负样本的关系 | 代码核验 |
| --- | --- | --- |
| [Learning with Noisy Correspondence for Cross-modal Matching](https://proceedings.neurips.cc/paper_files/paper/2021/hash/f5e62af885293cf4d511ceef31e61c80-Abstract.html) — **NeurIPS·2021** | NCR 根据网络记忆效应划分较干净/噪声配对，再以 co-teaching 自适应校正跨模态对应；核心是**错配配对的鲁棒学习**，不是专门检测未标注语义正例。 | [作者官方 PyTorch 仓库](https://github.com/XLearning-SCU/2021-NeurIPS-NCR)。**已核验** |
| [Deep Evidential Learning with Noisy Correspondence for Cross-Modal Retrieval](https://xlearning-lab.com/assets/2022-ACMMM-Deep-Evidential-Learning-with-Noisy-Correspondence-for-Cross-modal-Retrieval.pdf) — **ACM MM·2022** | DECL 以 Dirichlet 证据表示图文匹配不确定性，并以动态鲁棒损失处理噪声对应及困难负样本。它主要针对训练配对噪声；其不确定性/动态负例机制可作鲁棒训练参考，但不应等同于明确的假负样本标注校正。 | [作者 PyTorch 仓库](https://github.com/QinYang79/DECL)。**已核验** |
| [Cross-Modal Retrieval With Partially Mismatched Pairs](https://pubmed.ncbi.nlm.nih.gov/37027687/) — **TPAMI·2023** | RCL 研究部分错配正配对，采用 complementary contrastive learning，优先利用更可靠的负信息来减少错误正例带来的过拟合，同时补足弱监督下的学习信号；覆盖图文和视频—文本检索。关键词中的“negative information”指训练信息来源，不表示其主要任务就是发现假负样本。 | [作者代码仓库](https://github.com/penghu-cs/RCL)。**已核验** |
| [Cross-modal Active Complementary Learning with Self-refining Correspondence](https://papers.neurips.cc/paper_files/paper/2023/hash/4e580cdd54fe38ca9a5b8ea6fe99bb44-Abstract-Conference.html) — **NeurIPS·2023** | CRCL 用 Active Complementary Loss 降低错误监督风险，并通过多阶段自校正对应关系减少高噪声下的误差累积；重点仍是噪声配对鲁棒性，而不是纯粹的假负例筛除。 | [作者 PyTorch 仓库](https://github.com/QinYang79/CRCL)。**已核验** |
| [Cross-modal Retrieval with Noisy Correspondence via Consistency Refining and Mining](https://pubmed.ncbi.nlm.nih.gov/38507381/) — **TIP·2024** | CREAM 区分标注对应关系与语义一致性：协同学习校正正配对，同时挖掘负例中的潜在一致性，既抑制错误正例过拟合，也利用假负例承载的一致性信息。因此它是**正负噪声一体处理**的相邻方法。 | [作者官方实现](https://github.com/XLearning-SCU/2024-TIP-CREAM)。论文与仓库均确认。**已核验** |
| [Negative Pre-aware for Noisy Cross-Modal Matching](https://ojs.aaai.org/index.php/AAAI/article/view/28564) — **AAAI·2024** | NPC 估计每个训练样本带来的负面影响并分配置信度权重，再以 GMM 从记忆库选择高置信样本；这里的“negative impact”主要指噪声对应样本的有害训练影响，不应望文生义地理解为假负样本检测器。 | [AAAI 论文页明确给出代码](https://github.com/ZhangXu0963/NPC)。**已核验** |
| [Noisy-Correspondence Learning for Text-to-Image Person Re-identification](https://openaccess.thecvf.com/content/CVPR2024/html/Qin_Noisy-Correspondence_Learning_for_Text-to-Image_Person_Re-identification_CVPR_2024_paper.html) — **CVPR·2024** | RDE 以双粒度嵌入的一致判断筛出较可靠训练配对，再用 Triplet Alignment Loss 对所有负例构造上界式训练信号，面向行人图文**错误对应/错配**。这是行人检索噪声监督的重要参照，但假负例不是其主要问题定义。 | [作者官方 PyTorch 仓库](https://github.com/QinYang79/RDE)。**已核验** |
| [Learning to Rematch Mismatched Pairs for Robust Cross-Modal Retrieval](https://openaccess.thecvf.com/content/CVPR2024/html/Han_Learning_to_Rematch_Mismatched_Pairs_for_Robust_Cross-Modal_Retrieval_CVPR_2024_paper.html) — **CVPR·2024** | L2RM 以最优传输从错配样本间寻找潜在正确对应，并以 partial OT 限制错误正配对；它是**重新配对**而非抑制语义相关的假负例。 | [作者代码仓库](https://github.com/hhc1997/L2RM)。**已核验** |

## 三、方法谱系与对比

| 机制家族 | 代表工作 | 如何处理疑似假负例 | 优点 | 主要风险/适用条件 |
| --- | --- | --- | --- | --- |
| 概率估计后采样/降权 | FNE、FNCS | 估计候选为假负例的概率，再改变采样或损失权重 | 保留真正困难负例，抑制强误排斥 | 相似度分布/检测线索校准不准时会误删真负例；要报告检出精度与召回 |
| 软标签与语义扩展 | LG、CUSA、PCME++ | 用语言/单模态语义或概率嵌入补充潜在正关系 | 适合一对多、多描述及标签不完备数据 | 伪正例过多会稀释判别性；标注数据要支持多正样本验证 |
| 关系挖掘与显式重标 | MAFA | 发现隐含跨模态边，将部分负例转为正例并平滑对比目标 | 适用于大规模图文预训练 | 关系挖掘成本、阈值及错误关联传播需评估 |
| 多视角相似度与尾部统计 | TriSim | 图图、图文、文文三视角共同判断，极值统计识别疑似假负例 | 尤其针对遥感影像“同类场景高度相似” | 统计假设、阈值及数据域迁移可能影响识别；当前代码未确认公开 |
| 错配正例修复 | NCR、RCL、CRCL、CREAM、NPC、RDE、L2RM | 过滤、降权、校正或重新匹配错误正配对；个别方法也利用负例中的语义一致性 | 处理网络采集数据中错标/错配监督 | 与 FN 定义不同；比较实验需分别控制 FP、FN，不能只报统一“噪声率” |

## 四、结论与可复用的实验建议

1. **图文通用检索**：可从 FNE（概率采样）、CUSA/LG（语义软监督）、PCME++（概率嵌入）、MAFA（连接挖掘与重标）建立互补基线；不要只比较不同骨干网络。
2. **遥感图文检索**：TriSim针对遥感场景相似而跨模态阈值容易误判的特点，提示同时纳入图像—图像、文本—文本近邻；但应以 RSICD、RSITMD 等数据单独核验，不能直接外推到自然图像。
3. **文本行人检索**：除配对级标签外，应按身份构造多正关系；同一行人的不同图像/描述可能语义相关。FNCS 是直接假负样本方向，RDE 是噪声对应的相邻参照，二者要分开比较。
4. **评价设计**：在合成标签噪声时分别控制假负例率与假正例率；报告检索 R@K/mR、假负例识别 Precision/Recall、真实困难负例保留率，并做阈值/伪正例比例消融。只报最终 R@1 无法判断收益来自正确抑制还是过度放宽负例。
5. **代码复现顺序**：先跑官方仓库的原始配置，再统一骨干、批大小、候选池与噪声构造；仓库存在不等于当前依赖可运行，预训练权重、数据许可和旧版 CUDA/PyTorch 环境仍需单独核对。

**核心判断：** 直接假负样本方法的主线已经从“避免把高相似未配对样本作为硬负例”（FNE），发展到“发现/补足潜在正关系”（LG、CUSA、MAFA）、“用不确定性表达多重语义”（PCME++），并扩展到行人检索（FNCS）和遥感检索（TriSim）。落地时应将假负例与错误正配对分开建模；忽略这一区分会导致方法归类和实验结论失真。

## 检索索引与核验说明

- [Awesome-Noisy-Correspondence](https://github.com/XLearning-SCU/Awesome-Noisy-Correspondence)：用于扩展噪声对应方向的候选文献；本页关键结论以论文/出版社页面和作者代码仓库复核。
- [Awesome-Text-Image-Person-Retrieval](https://github.com/Yifei-AHU/Awesome-Text-Image-Person-Retrieval)：用于发现文本行人检索相关候选；会议归属、摘要与代码状态仍以论文页及作者仓库为准。
- 对“本次未找到代码”的论文，表示截至上述日期、经论文官方页与作者关联仓库检索后没有确认入口；不将第三方复现、同名仓库或非官方汇总页计作作者代码。
