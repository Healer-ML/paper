# 负样本抑制与干扰物排除：目标计数方法专题

[返回果实计数目录](fruit-counting.md) · [返回三方向论文总览](README.md) · [跨领域计数与开放计数专题](counting-research.md)

**检索截止：2026-10-12。** 本专题调研视觉计数中利用负样本、负提示、反例或候选验证来减少误计的现有方法，优先列出会议论文并核对论文/作者仓库中的代码状态；随后补充期刊、农业直接相关工作与评测基准。论文摘要为中文释义，不是逐字翻译。代码状态按论文官方页面、作者项目页或其明确关联仓库核验；“未找到/未核验”仅表示本次检索没有确认到公开实现，不断言代码绝对不存在。

## 研究问题与范围

本调研聚焦三个问题：

1. 负证据在计数流程的哪个环节发挥作用：输入提示、训练/特征学习、候选验证，还是背景先验？
2. 哪些会议方法有可访问代码，公开程度和可复现边界如何？
3. 这些方法迁移到农业果实计数时，能否抑制叶片、枝梗、果帽、未成熟果及相似品种造成的误计？

检索覆盖 2021–2026 年，关键词组合包括 negative exemplar/sample/prompt、exclusion、distractor、hard negative、false positive verification、background suppression、fine-grained counting、fruit counting；按论文官方会议/出版社页面与作者仓库逐项交叉检查。纳入直接改变计数模型排除干扰物能力的工作；将只作评测、只抑制背景、或只筛选正例的工作单列，不把它们误称为显式负样本计数。本文没有找到 2021–2022 年可核验、同时以负 exemplars/负提示为核心且有代码的主流计数会议论文；这表示检索范围内未检出，不代表该时期绝无相关工作。

## 一、方法分类：不要把“负样本抑制”混为一谈

| 类别 | 负证据进入的位置 | 代表机制 | 主要抑制的错误 | 与果实场景的关系 |
| --- | --- | --- | --- | --- |
| 显式负提示 / 负 exemplar | 推理输入 | 用户同时提供“要数什么”和“不要数什么”的文本或视觉样例，模型对正负提示进行区分 | 与目标外观相似的类别/属性被一起计入 | 最贴近成熟/未成熟、不同果种、果实/果帽等细粒度排除；依赖负例质量 |
| 负 exemplar 判别学习 | 训练或特征匹配 | 正、负 exemplar 分别形成目标/非目标证据，学习更具判别性的相似度或密度响应 | 正例外观不充分导致的相似物误激活 | 可将叶片、枝条、果帽等作为困难负例；训练集必须覆盖品种与成像变化 |
| 候选验证 / outlier removal | 推理候选阶段 | 先高召回地产生候选，再验证并剔除非目标候选 | 检测或密度响应中的离群误检 | 能改善精度，但不一定能表达用户想排除的细粒度类别 |
| 前景/背景抑制 | 特征/空间区域 | 掩膜、显著性或语义分割压低背景区域，再计数前景 | 叶片、土壤、枝条等背景干扰 | 农业直接相关；但“果实 vs 背景”不等于“果实 A vs 相似果实 B” |
| 正例筛选 / 负标签评测 | 输入质量控制 / 评估 | 筛掉不准的软 exemplar；或测试模型对不存在类别/干扰类是否拒绝响应 | 错误正例或语义落地失败 | 对构建果园 hard-negative benchmark 有用，但本身不一定提出负样本抑制模型 |
| 计数数值 hard negative | 图文训练目标 | 将正确数量描述改成错误数量，要求模型偏好正确图文对 | 数量语义理解错误 | 属于“数错数量”的反事实负样本，不是“目标类别 vs 干扰类别”抑制，不能直接视作果园排除方法 |

## 二、会议论文：方法与代码优先

### 2.1 显式负提示、负 exemplar 与候选误检抑制

| 论文（刊会/年份） | 方法与中文摘要（负证据如何起作用） | 代码核验 |
| --- | --- | --- |
| [DAVE: A Detect-and-Verify Paradigm for Low-Shot Counting](https://openaccess.thecvf.com/content/CVPR2024/html/Pelhan_DAVE_-_A_Detect-and-Verify_Paradigm_for_Low-Shot_Counting_CVPR_2024_paper.html) — **CVPR 2024** | 低样本计数器先生成高召回候选，再通过验证器识别并移除离群候选，针对多类别图像中其他类别导致的误检和计数高估。它属于**模型自动候选验证**，并非用户输入负提示；是“先尽量找全、再排除”的代表路线。[1] | [作者官方 PyTorch 代码](https://github.com/jerpelhan/DAVE)，含推理、评测脚本与模型下载说明。**已核验。** |
| [Zero-shot Object Counting with Good Exemplars (VA-Count)](https://www.ecva.net/papers/eccv_2024/papers_ECCV/html/812_ECCV_2024_paper.php) — **ECCV 2024** | EEM 搜索候选 exemplar，Noise Suppression Module（NSM）以对比学习区分较优与较差 exemplar，降低错误 exemplar 传播到密度图的负面作用。重点是**自动筛选/抑制噪声示例**，并非完整的用户负提示框架。[2] | [作者仓库](https://github.com/HopooLinZ/VA-Count)已公开并提供推理、训练命令；但 README 对“示例选择/训练代码即将发布”的说明与仓库当前文件/命令存在不完全一致之处。**有代码，复现前需核对脚本、权重和所需组件是否齐全。** |
| [CountSE: Soft Exemplar Open-set Object Counting](https://openaccess.thecvf.com/content/ICCV2025/html/Liu_CountSE_Soft_Exemplar_Open-set_Object_Counting_ICCV_2025_paper.html) — **ICCV 2025** | 文本引导生成多尺度 soft exemplars，再经相似度选择与聚类过滤，减少不准确正例对开放集计数的污染。它抑制的是**错误正例 exemplar**，并不显式指定“哪些物体不要数”。[3] | [作者代码](https://github.com/pppppz22/CountSE)。ICCV 官方论文页直接给出代码入口。**已核验。** |
| [CountGD++: Generalized Prompting for Open-World Counting](https://robots.ox.ac.uk/~vgg/publications/2026/AminiNaienib26/) — **CVPR 2026** | 将“数什么”扩展为正文本/正视觉样例，将“不要数什么”扩展为负文本/负视觉样例；还支持外部图像示例与自动生成的 pseudo-exemplars。其核心价值是推理时可明确表达排除意图，是目前最直接对应负提示交互的会议方法之一。[4] | [作者官方代码](https://github.com/niki-amini-naieni/CountGDPlusPlus)；CVPR 论文页亦列出项目与代码入口。仓库有 PyTorch 推理/训练说明。**已核验。** |
| [CountEx: Fine-Grained Counting via Exemplars and Exclusion](https://arxiv.org/abs/2602.19432) — **ECCV 2026** | 面向外观相近类别，联合正/负文本及可选视觉 exemplar；Discriminative Query Refinement 先识别两类共享特征，再提取负类独有特征，并选择性从正查询中抑制。它与 CountGD++ 的通用负提示互补：CountEx 更强调**细粒度类间/类内区分**，并配套 CoCount（1,780 段视频、10,086 帧、97 组类别对）。[5] | [作者官方实现与 CoCount](https://github.com/bbvisual/CountEx)；[CoCount 数据集集合](https://huggingface.co/collections/BBVisual/cocount)。仓库含训练/评测代码、数据格式与模型入口。**已核验。** |

### 2.2 相关会议工作：负样本定义需按任务理解

| 论文（刊会/年份） | 方法与中文摘要 | 代码核验 |
| --- | --- | --- |
| [Teaching CLIP to Count to Ten](https://openaccess.thecvf.com/content/ICCV2023/html/Paiss_Teaching_CLIP_to_Count_to_Ten_ICCV_2023_paper.html) — **ICCV 2023** | 对图像说明自动替换数量词，构造只在数量上不同的反事实 caption，并用计数对比损失区分正确/错误数量。它是明确的 hard-negative 训练，但负例针对“数量不对”，而非“把叶子或其他果种排除”。[6] | 未核验到原作者官方代码入口；[CountCLIP](https://github.com/SforAiDl/CountCLIP)是第三方复现，不能标作原论文官方实现。 |
| [Benchmarking Dense and Indiscernible Object Counting with Blueberries](https://proceedings.mlr.press/v306/bo26a.html) — **ICML 2026** | 提出 DIOCblueberry 与 MaskCount；CLIP 产生伪分割掩膜抑制背景，并以对比损失拉开蓝莓和叶片特征。它是本专题中与农业果实最直接相关的会议工作，但机制属于**前景/背景抑制**，目前论文页未给出模型仓库入口。[7] | [DIOCblueberry 数据集](https://huggingface.co/datasets/weihao-bo/DIOCblueberry)公开可访问；截至核验日，未从论文官方页面确认 MaskCount 模型代码仓库。**数据公开不等于模型代码已公开。** |

## 三、评测基准：测“排除能力”，不等于提出新抑制模型

| 论文/资源（刊会或年份） | 基准价值 | 代码/数据 |
| --- | --- | --- |
| [Can Current AI Models Count What We Mean, Not What They See? A Benchmark and Systematic Evaluation (PairTally)](https://arxiv.org/abs/2509.13939) — **DICTA 2025** | PairTally 以可控图像对测试细粒度计数，覆盖不同类别以及同类颜色、纹理、尺寸等差异；专门暴露模型把相似 distractor 一起计数的问题。它是诊断基准，不是负样本抑制算法。[8] | [作者基准、数据和评测代码](https://github.com/bbvisual/PairTally_Benchmark)；仓库列出 681 张配对图像、标注与多个计数器评测实现。**已核验。** |
| [Does it Really Count? Assessing Semantic Grounding in Text-Guided Class-Agnostic Counting](https://arxiv.org/abs/2605.02752) — **arXiv 2026 预印本** | PrACo++ 提出 negative-label 与 distractor 测试，检查文本提示是否被正确落地、模型能否在类别不存在或存在干扰物时避免虚假响应。适合评价负提示模型的拒识能力；论文为评测研究，不是一个新的排除式计数器。[9] | [arXiv 关联的 PrACo 仓库](https://github.com/ciampluca/PrACo)包含基准脚本和多种模型适配。**注意：当前 README 以较早的 PrACo 基准为主，虽列有 CountGD++ 适配，但不应据此把它视为 PrACo++ 完整专属实现。** |

## 四、期刊与农业直接相关补充

| 论文（期刊/年份） | 方法与适用性 | 代码核验 |
| --- | --- | --- |
| [ConCoNet: Class-agnostic counting with positive and negative exemplars](https://www.sciencedirect.com/science/article/abs/pii/S0167865523001253) — **Pattern Recognition Letters, 2023** | 将正、负 exemplar 的相似度信息合并进 class-agnostic 计数器，可作为“显式 exemplar 排除”的早期方法基础。论文在 FSC-147 等通用计数设定验证，并非果园专用方法。[10] | 本次未确认到论文作者公开的官方代码仓库。 |
| [PolaCount: Text-specified zero-shot object counting with pyramid polarity-aware cross-attention](https://www.sciencedirect.com/science/article/pii/S0925231225018077) — **Neurocomputing, 2025** | 在多尺度文本—视觉交叉注意力中分离正、负相关分量并组合，抑制矛盾响应；不同于输入显式负类文本/样例，它是特征计算层的 polarity-aware 机制。[11] | 本次未核验到作者代码仓库；论文页面未给出代码链接。 |
| [Dynamic example network for class-agnostic object counting (DEN)](https://www.sciencedirect.com/science/article/pii/S0031320325006582) — **Pattern Recognition, 2026** | 迭代扩充正 exemplar，并从跨图像数据中挖掘负 exemplar，提高类无关计数的判别能力。论文讨论了苹果与果帽等易混淆示例，可作为农业负样本设计的直接启发；但不是果园专用模型。[12] | 论文称代码与模型将公开；本次尚未核验到作者可访问的正式仓库。**代码计划 ≠ 已公开代码。** |

## 五、横向比较与农业迁移判断

### 5.1 现有方法的互补关系

- **用户能否指定不要数什么：** CountGD++、CountEx最直接。CountGD++支持正/负文本与视觉例子；CountEx通过显式抑制负类独有表征处理更细粒度的相似对象。两者的公开实现有利于构建果实排除原型。
- **能否在没有负提示时压低误检：** DAVE使用检测后验证；VA-Count抑制质量差的 exemplar；CountSE过滤不准确的 soft positive exemplar。它们改善错误候选或错误输入，但不等价于用户指定的语义负类。
- **最接近田间背景噪声的工作：** ICML 2026 MaskCount直接区分蓝莓与叶片并抑制背景，农业域证据更直接；但若目标是“成熟果 vs 未成熟果”或“目标品种 vs 相似品种”，背景掩膜机制仍不足以代替细粒度负提示。
- **评测缺口：** PairTally、CoCount、PrACo++提供相似类别或语义拒识评测思路；但目前无法据此声称这些方法已在不同果园、品种、成熟阶段和视频跨帧场景中全面验证。

### 5.2 对果实计数可落地的实验设计

1. **按误计来源建负类，而非只标“背景”。** 建议至少区分：叶片/枝条/果柄；果帽/萼片；未成熟与成熟果；近似颜色或形状的其他果种；反光、遮挡和切块边缘伪影。农业场景里，困难负例应与正例在颜色、尺度、纹理或视角上相似。
2. **优先验证两个互补机制。** 将 CountGD++/CountEx 作为显式负提示基线；将 DAVE 或 MaskCount 的验证/前景抑制思想作为自动排错基线。不要把它们合并成一个“负样本模型”标签。
3. **迁移时按数据许可重建评测集。** 可从本仓库[农业果实数据集清单](fruit-counting.md#dataset-agriculture)选择 MinneApple、BlueberryDCM、DIOCblueberry 等，再增加成熟度/果种/叶片干扰的负标签。通用 CoCount/PairTally 不能替代真实果园测试。
4. **指标同时报告计数误差和排除质量。** 除 MAE/RMSE 外，建议报告负类误计率（false inclusion）、目标漏计率（false exclusion）、按负类类别分层的 Precision/Recall，以及每株/每幅图的误计数；视频另测跨帧重复计数。强负提示可能提高排除率但误删外观变化较大的真目标，因此必须报告漏计权衡。
5. **做负例质量与强度消融。** 比较无负例、简单背景负例、同类属性负例、跨类近邻负例；逐步改变负 exemplar 数量、相似度和文本粒度，检查是否出现过度抑制、跨品种泛化下降或视角变化失效。

**综合结论：** 现有方法从“负 exemplar 学判别”（ConCoNet、VA-Count、DEN）发展到“负提示直接表达排除意图”（CountGD++、CountEx），并辅以候选验证（DAVE）和农业前景/背景抑制（MaskCount）。对于果实计数，最值得直接复用的是显式正负提示与农业背景抑制的组合；但截至本次核验，显式负提示方法在果实成熟度、果种近邻和田间视频上的专项评测仍有限，不能把通用基准结果等同于果园有效性。

## 参考文献与来源

[1] Pelhan et al. *DAVE – A Detect-and-Verify Paradigm for Low-Shot Counting*. CVPR 2024. [官方论文页](https://openaccess.thecvf.com/content/CVPR2024/html/Pelhan_DAVE_-_A_Detect-and-Verify_Paradigm_for_Low-Shot_Counting_CVPR_2024_paper.html) · [作者代码](https://github.com/jerpelhan/DAVE)

[2] Zhu et al. *Zero-shot Object Counting with Good Exemplars*. ECCV 2024. [官方论文页](https://www.ecva.net/papers/eccv_2024/papers_ECCV/html/812_ECCV_2024_paper.php) · [作者代码](https://github.com/HopooLinZ/VA-Count)

[3] Liu et al. *CountSE: Soft Exemplar Open-set Object Counting*. ICCV 2025. [CVF论文页](https://openaccess.thecvf.com/content/ICCV2025/html/Liu_CountSE_Soft_Exemplar_Open-set_Object_Counting_ICCV_2025_paper.html) · [作者代码](https://github.com/pppppz22/CountSE)

[4] Amini-Naieni & Zisserman. *CountGD++: Generalized Prompting for Open-World Counting*. CVPR 2026. [Oxford/VGG论文页](https://robots.ox.ac.uk/~vgg/publications/2026/AminiNaienib26/) · [作者代码](https://github.com/niki-amini-naieni/CountGDPlusPlus)

[5] Huang et al. *CountEx: Fine-Grained Counting via Exemplars and Exclusion*. ECCV 2026. [arXiv论文页](https://arxiv.org/abs/2602.19432) · [作者代码与 CoCount](https://github.com/bbvisual/CountEx)

[6] Paiss et al. *Teaching CLIP to Count to Ten*. ICCV 2023. [CVF论文页](https://openaccess.thecvf.com/content/ICCV2023/html/Paiss_Teaching_CLIP_to_Count_to_Ten_ICCV_2023_paper.html) · [第三方复现 CountCLIP](https://github.com/SforAiDl/CountCLIP)

[7] Bo et al. *Benchmarking Dense and Indiscernible Object Counting with Blueberries*. ICML 2026, PMLR 306. [PMLR论文页](https://proceedings.mlr.press/v306/bo26a.html) · [DIOCblueberry数据](https://huggingface.co/datasets/weihao-bo/DIOCblueberry)

[8] Nguyen et al. *Can Current AI Models Count What We Mean, Not What They See? A Benchmark and Systematic Evaluation*. DICTA 2025. [arXiv论文页](https://arxiv.org/abs/2509.13939) · [作者基准与代码](https://github.com/bbvisual/PairTally_Benchmark)

[9] Pacini et al. *Does it Really Count? Assessing Semantic Grounding in Text-Guided Class-Agnostic Counting*. arXiv 2026. [论文页](https://arxiv.org/abs/2605.02752) · [作者评测代码](https://github.com/ciampluca/PrACo)

[10] Soliven et al. *ConCoNet: Class-agnostic counting with positive and negative exemplars*. Pattern Recognition Letters 171 (2023), 148–154. [出版社论文页](https://www.sciencedirect.com/science/article/abs/pii/S0167865523001253)

[11] Qian et al. *PolaCount: Text-specified zero-shot object counting with pyramid polarity-aware cross-attention*. Neurocomputing 652 (2025), 131135. [出版社论文页](https://www.sciencedirect.com/science/article/pii/S0925231225018077)

[12] Liu et al. *Dynamic example network for class-agnostic object counting*. Pattern Recognition 170 (2026), 111998. [出版社论文页](https://www.sciencedirect.com/science/article/pii/S0031320325006582)
