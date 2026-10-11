# 计数研究专题：开放计数、遥感计数与农业果实计数

[返回三方向论文总览](../README.md) · [果实计数分类目录](fruit-counting.md)

**检索截止：2026-10-11。** 本专题按任务设定和应用领域分别整理 2021–2026 年代表性及近期研究，重点补充开放词汇/开放世界计数、遥感目标计数和农业果实计数，并逐条核对论文出处与代码仓库。代码核验检查公开仓库、README、源码和训练/推理入口；“未找到”表示本轮未确认到公开官方实现，不等于证明作者没有代码。仓库可访问不等于环境已部署或结果已复现；数据集、评测脚本、部分实现与模型完整实现分别标注。

> **题名校正：** 用户举例中的 arXiv:2606.17561 实际是 **RT-Counter**，而 **CountSE** 是独立的 ICCV 2025 论文；二者的代码仓库也不同，详见下表。

## 先区分任务设定

- **文本开放词汇 / 零样本计数**：用户用自然语言指定目标类别，模型无需为每个新类别重新训练；核心是文本语义与图像空间实例的对应。
- **开放世界 / 多模态提示计数**：可用文本、正/负视觉示例，或二者共同描述目标；不等同于“纯文本零样本”。
- **类无关 / 少样本计数**：模型可数未见类别，但往往需要框选示例、点提示、交互或弱监督；这里单独归类，不把它们全部标成开放词汇。
- **应用领域**：遥感、农业是数据与场景维度，可以采用闭集、少样本或开放词汇方法。RS-OVC 等兼具领域和开放词汇属性，因此在相关类别交叉引用。
- **邻近任务**：视频唯一目标计数、计数推理、计数条件图像生成与通用 MLLM 计数基准会注明其边界，不与单图密集计数混为一谈。

<a id="open-vocabulary-counting"></a>
## 一、开放词汇 / 开放世界计数（文本指定为主，设定有别）

### 2021–2023：从类无关泛化走向文本指定

| 论文 | 主要内容（中文释义） | 刊会 / 年份 | 代码核验 |
|---|---|---|---|
| [Zero-Shot Object Counting](https://openaccess.thecvf.com/content/CVPR2023/html/Xu_Zero-Shot_Object_Counting_CVPR_2023_paper.html) | 将类别名称作为语义条件，在无该类别计数训练样本时生成密度图；是文本零样本计数的早期代表。 | CVPR 2023 | [官方实现](https://github.com/cvlab-stonybrook/zero-shot-counting) |
| [CLIP-Count: Towards Text-Guided Zero-Shot Object Counting](https://dl.acm.org/doi/10.1145/3581783.3611789) | 用文本提示选择 CLIP 视觉语义，再通过密度估计把开放类别描述映射为对象数量。 | ACM MM 2023 | [作者代码](https://github.com/songrise/CLIP-Count) |
| [CounTX: Open-world Text-specified Object Counting](https://arxiv.org/abs/2306.01851) | 将任意文本类别与图像特征交互，进行开放世界文本指定计数；属于文本条件方法，不需要人工框示例。 | BMVC 2023 | [作者代码](https://github.com/niki-amini-naieni/CounTX) |

### 2024–2025：视觉语言适配与提示增强

| 论文 | 主要内容（中文释义） | 刊会 / 年份 | 代码核验 |
|---|---|---|---|
| [VLCounter: Text-Aware Visual Representation for Zero-Shot Object Counting](https://ojs.aaai.org/index.php/AAAI/article/view/28050) | 在视觉表示中显式注入类别文本信息，改善零样本计数中语言语义与目标区域的对齐。 | AAAI 2024 | [AAAI 页面所列代码](https://github.com/Seunggu0305/VLCounter) |
| [Zero-shot Object Counting with Good Exemplars (VA-Count)](https://www.ecva.net/papers/eccv_2024/papers_ECCV/papers/00812.pdf) | 研究无训练样本的零样本计数，并从图像中选择更可靠的视觉示例辅助目标定位；和纯文本指定设定不同。 | ECCV 2024 | [作者代码](https://github.com/HopooLinZ/VA-Count)（仓库公开；训练组件完整度需按仓库说明判断） |
| [Class-Agnostic Object Counting with Text-to-Image Diffusion Model (CountDiff)](https://www.ecva.net/papers/eccv_2024/papers_ECCV/html/8663_ECCV_2024_paper.php) | 利用扩散模型知识实现类无关计数，在有视觉示例的少样本与仅类别名的零样本设置中均评估；属于两类设置交叉。 | ECCV 2024 | 本轮未找到可确认的作者官方模型代码。 |
| [CountGD: Multi-Modal Open-World Counting](https://arxiv.org/abs/2407.04619) | 将 Grounding DINO 改造为开放世界计数器，可通过文本、视觉示例或两者共同指定目标。 | NeurIPS 2024 | [官方实现与项目页](https://github.com/niki-amini-naieni/CountGD) |
| [Referring Expression Counting](https://openaccess.thecvf.com/content/CVPR2024/html/Dai_Referring_Expression_Counting_CVPR_2024_paper.html) | 提出 REC-8K，按同类别内的属性、动作和上下文短语区分目标（如颜色、队列位置）；比只输入类别名更细粒度。 | CVPR 2024 | [论文官方代码与数据](https://github.com/sydai/referring-expression-counting) |
| [OmniCount: Multi-label Object Counting with Semantic-Geometric Priors](https://ojs.aaai.org/index.php/AAAI/article/view/34151) | 面向多标签开放词汇场景，结合语义与几何先验，在一张图中对用户指定的多个类别计数。 | AAAI 2025 | [作者代码](https://github.com/mondalanindya/OmniCount) |
| [T2ICount: Enhancing Cross-modal Understanding for Zero-Shot Counting](https://openaccess.thecvf.com/content/CVPR2025/html/Qian_T2ICount_Enhancing_Cross-modal_Understanding_for_Zero-Shot_Counting_CVPR_2025_paper.html) | 通过跨模态学习增强文本提示与局部目标区域的对应，提升自然语言指定类别的零样本计数。 | CVPR 2025 | [作者代码](https://github.com/cha15yq/T2ICount) |
| [Exploring Contextual Attribute Density in Referring Expression Counting](https://openaccess.thecvf.com/content/CVPR2025/html/Wang_Exploring_Contextual_Attribute_Density_in_Referring_Expression_Counting_CVPR_2025_paper.html) | 为细粒度指代表达建模上下文属性密度，结合 Grounding DINO 多尺度视觉特征定位并计数表达所指对象。 | CVPR 2025 | [作者仓库 CAD-GD](https://github.com/Xu3XiWang/CAD-GD)公开，含可运行实现。 |
| [SDVPT: Semantic-Driven Visual Prompt Tuning for Open-World Object Counting](https://doi.org/10.1145/3746027.3754581) | 以可插拔语义驱动视觉提示调优迁移已见类知识到未见类别，支持多种开放世界计数器。 | ACM MM 2025 | [作者代码与预训练权重](https://github.com/Eamon-0v0/SDVPT)已公开；README 标明部分测试/训练组件仍在 TODO，属**部分实现**。 |
| [TrueCount: Improving Open-World Object Counting with Visual-Language Models and Dynamic Multi-Modal Inputs](https://doi.org/10.1145/3746027.3755426) | 动态融合 RGB、分割、深度与文本/视觉提示，并估计各模态置信度以增强复杂遮挡和层叠场景计数。 | ACM MM 2025 | 本轮未找到与论文/作者明确关联的公开官方模型代码。 |
| [VQCounter: Designing Visual Prompt Queue for Accurate Open-World Counting](https://www.ijcai.org/proceedings/2025/252) | 通过视觉提示队列扩大示例多样性，并结合模态切换和 Voronoi 匹配损失，评估零样本与少样本计数。 | IJCAI 2025 | 本轮未找到可确认的作者官方代码仓库。 |
| [Text-Promptable Object Counting via Quantity Awareness Enhancement (QUANet)](https://arxiv.org/abs/2507.06679) | 通过数量感知文本提示、视觉—文本数量对齐与双流解码器增强文本提示计数的数量语义。 | arXiv 2025 预印本 | [作者官方实现](https://github.com/viscom-tongji/QUANet)公开，论文 arXiv 页面明确给出。 |
| [Expanding Zero-Shot Object Counting with Rich Prompts (RichCount)](https://arxiv.org/abs/2505.15398) | 以两阶段训练丰富文本表示并强化视觉—文本对齐，提升未见类别与复杂提示下的零样本计数。 | arXiv 2025 预印本 | 未找到可确认的作者官方仓库；第三方课程/复现代码不计为官方实现。 |
| [Mind the Prompt: A Novel Benchmark for Prompt-Based Class-Agnostic Counting (PrACo)](https://openaccess.thecvf.com/content/WACV2025/html/Ciampi_Mind_the_Prompt_A_Novel_Benchmark_for_Prompt-Based_Class-Agnostic_Counting_WACV_2025_paper.html) | 提出提示感知基准，以缺失类别负提示和多类拼接干扰图评估模型是否真正理解“要数什么”；属于评测基准而非新计数器。 | WACV 2025 | [论文复现实验代码](https://github.com/ciampluca/PrACo)由 CVF 页面明确列出。 |
| [Counting Through Occlusion: Framework for Open World Amodal Counting (CountOCC)](https://arxiv.org/abs/2511.12702) | 从可见目标上下文重建遮挡区域的目标特征，推断可见与被遮挡实例总数；是开放世界计数的 amodal 扩展。 | arXiv 2025 预印本 | [作者公开仓库](https://github.com/rabeya-akter/CountOCC)含训练与推理入口（如 `main.py`、`main_inference.py`）；仓库可访问。 |
| [CountSE: Soft Exemplar Open-set Object Counting](https://openaccess.thecvf.com/content/ICCV2025/html/Liu_CountSE_Soft_Exemplar_Open-set_Object_Counting_ICCV_2025_paper.html) | 论文提出文本引导零样本开放集计数：从文本语义产生多尺度软示例，再以语义筛选和聚类过滤提升定位与计数。这里的 exemplar 是模型生成的软特征，不是要求用户手工框选的 few-shot 输入。 | ICCV 2025 | [官方实现](https://github.com/pppppz22/CountSE) |
| [Enhancing Zero-shot Object Counting via Text-guided Local Ranking and Number-evoked Global Attention (LGCount)](https://openaccess.thecvf.com/content/ICCV2025/html/Zhang_Enhancing_Zero-shot_Object_Counting_via_Text-guided_Local_Ranking_and_Number-evoked_ICCV_2025_paper.html) | 以文本引导局部排序和数量感知全局注意力改善文本零样本计数，并构建 ZSC-8K。 | ICCV 2025 | [作者官方仓库](https://github.com/zaqai/LGCount)公开，含训练与评测脚本 `run.py`、模型和数据准备说明。 |
| [YOLO-Count: Differentiable Object Counting for Text-to-Image Generation](https://openaccess.thecvf.com/content/ICCV2025/html/Zeng_YOLO-Count_Differentiable_Object_Counting_for_Text-to-Image_Generation_ICCV_2025_paper.html) | 将计数器用作文本生成图像的数量控制/可微监督模块；属于计数与生成交叉，不是通用开放计数基准上的独立计数模型。 | ICCV 2025（生成交叉） | [作者代码](https://github.com/mlpc-ucsd/YOLO-Count) |

<a id="video-counting"></a>
### 2026：开放提示、细粒度意图与视频计数

| 论文 | 主要内容（中文释义） | 刊会 / 年份 | 代码核验 |
|---|---|---|---|
| [CountGD++: Generalized Prompting for Open-World Counting](https://arxiv.org/abs/2512.23351) | 将正/负文本和视觉提示、伪示例组合为更通用的开放世界提示策略，提升复杂目标指定能力。 | CVPR 2026 | [官方实现](https://github.com/niki-amini-naieni/CountGDPlusPlus) |
| [Boosting Quantitive and Spatial Awareness for Zero-Shot Object Counting (QICA)](https://openaccess.thecvf.com/content/CVPR2026/papers/Zhang_Boosting_Quantitive_and_Spatial_Awareness_for_Zero-Shot_Object_Counting_CVPR_2026_paper.pdf) | 针对 CLIP 零样本计数中的数量感知与空间定位不足，提出数量-空间感知的特征聚合方案。 | CVPR 2026 | 论文称代码可用；论文/检索所指仓库 [zhangda1018/QICA](https://github.com/zhangda1018/QICA) 当前不可访问（404），故不计为已公开可复现代码。 |
| [Open-World Object Counting in Videos (CountVid)](https://ojs.aaai.org/index.php/AAAI/article/view/37214) | 把开放世界计数扩展到视频：给定文本或示例，逐帧定位并跟踪后统计视频中出现过的唯一目标，而非简单累加每帧实例。 | AAAI 2026（视频） | [官方代码与 VideoCount 数据集](https://github.com/niki-amini-naieni/CountVid) |
| [CountEx: Fine-Grained Counting via Exemplars and Exclusion](https://arxiv.org/abs/2602.19432) | 用正示例表示“计什么”、负示例/文本表示“排除什么”，针对相似类别或属性的细粒度目标计数；包含 CoCount 基准。 | ECCV 2026 | [官方实现与 CoCount](https://github.com/bbvisual/CountEx) |
| [Depth-Guided Video Object Counting in Crowded Scenes](https://arxiv.org/abs/2608.06236) | 将深度与 RGB 融合，结合文本/视觉提示、跨帧去重和 RGB-D 视频数据集，面向拥挤遮挡视频中的开放类别计数。 | ACM MM 2026（视频） | [作者官方实现](https://github.com/streamer-AP/DG-Net)；[RGBD-VideoCount 数据集](https://huggingface.co/datasets/aerospace123/RGBD-VideoCount) |
| [RT-Counter: Real-Time Text-Guided Open-Vocabulary Object Counting](https://arxiv.org/abs/2606.17561) | 以视觉原型文本化和 Weaving Transformer 改善文本—目标对齐与推理速度；论文报告 FSC-147 上 112.48 FPS。 | arXiv 2026 预印本 | [作者代码](https://github.com/Jason-Mar1/RT-Counter) |
| [MambaCount: Efficient Text-guided Open-vocabulary Object Counting with Spatial Sparse State Space Duality Block](https://arxiv.org/abs/2606.17650) | 将文本引导开放词汇计数与稀疏状态空间模块结合，目标是以较低计算成本保留空间结构和密集实例定位能力。 | arXiv 2026 预印本 | 截至检索日未找到可访问的官方代码仓库。 |
| [Test-Time Training for Robust Text-Guided Open-Vocabulary Object Counting (Dual-TTT)](https://arxiv.org/abs/2606.17601) | 研究测试时适应，以缓解文本指定类别变化时的分布偏移和开放词汇计数鲁棒性问题。 | arXiv 2026 预印本 | 截至检索日未确认到公开官方代码。 |
| [Count Anything](https://arxiv.org/abs/2605.30846) | 提出跨域文本计数模型与 CLOC 基准，涵盖通用场景、遥感、农业、组织病理、细胞显微和微生物；以稀疏/密集双计数器输出实例点。 | arXiv 2026 预印本 | [作者代码、模型与配置](https://github.com/Mengqi-Lei/count-anything)；CLOC 涵盖遥感和农业，但并非仅面向这两个领域。 |
| [Count Anything at Any Granularity](https://arxiv.org/abs/2605.10887) | 提出多粒度开放世界计数：视觉示例配合细粒度文本/负提示来指定身份、属性、实例或类别等不同层次；同时发布 KubriCount 并提出 HieraCount。 | arXiv 2026 预印本 | [项目页/KubriCount](https://verg-avesta.github.io/KubriCount/) 公开数据合成/生成资源；本轮未确认 HieraCount 模型训练代码公开。 |
| [TPECount: Text-guided Patch-level Exemplar Selection for Zero-Shot Counting](https://doi.org/10.1016/j.engappai.2026.113986) | 利用文本提示进行 patch 级示例选择，改善零样本计数中目标特征的检索与空间定位。 | Eng. Appl. Artif. Intell. 2026 | [论文所列作者代码](https://github.com/aHui3/TPECount)公开。 |
| [Towards Generalizable Object Counting via Dual-Prompted Cross-Modality Fusion Network (DCFNet)](https://doi.org/10.1016/j.inffus.2025.103837) | 融合文本与框提示，采用跨模态提示和语义/空间交互以提升开放世界计数泛化。 | Information Fusion 2026 | [论文所列作者代码](https://github.com/wzzhai/DCFNet)公开。 |
| [PD-count: Prompt-driven Zero-shot Object Counting with Dynamic Frequency Transformation](https://doi.org/10.1016/j.eswa.2026.131295) | 结合提示条件视觉—语言特征和动态频域变换，改善零样本密度图预测。 | ESWA 2026 | 本轮未找到可确认的作者官方代码仓库。 |
| [DualCount: Structurally Consistent Density and Point Modeling for Zero-Shot Object Counting](https://link.springer.com/book/10.1007/978-3-032-37335-9?page=1) | 将密度图与实例点联合建模，通过实例质量守恒和质心对齐约束减少背景泄漏与密度质量分配错误。 | ECCV 2026 | 论文已见 Springer ECCV 2026 论文集；截至检索日未找到可确认的作者代码仓库。 |
| [SAM3Count: Zero-Shot Open Vocabulary Counting in Images and Videos](https://openreview.net/pdf?id=t3NZw67uAM) | 使用 SAM3 对文本指定类别做图像/视频零样本计数，并支持大图切块；为 CVPR 相关 workshop 工作，不是 CVPR 主会论文。 | CVPRW 2026 | [作者仓库](https://github.com/Joan947/SAM3Count)公开推理/演示组件，完整训练代码标注待发布；属**部分实现**。 |
| [The MixCount Dataset: Bridging the Data Gap for Open-Vocabulary Object Counting](https://arxiv.org/abs/2605.18063) | 针对同图多类、易混目标计数数据不足，构建合成混合目标图像与细粒度标注基准；论文侧重数据/训练资源，不是单一计数器。 | arXiv 2026 预印本 | [MixCount 数据集](https://huggingface.co/datasets/CorentinDumery/MixCount)公开；未确认到可访问的官方模型/生成代码仓库。 |

<a id="remote-sensing-counting"></a>
## 二、遥感与航拍目标计数

此类工作常见难点是超大幅面、小目标、尺度变化、地理域偏移和极少标注。除标明开放词汇的 RS-OVC 外，下表多数是闭集、跨域或少样本计数，不能直接当成“文本开放类别计数”。

| 论文 | 主要内容（中文释义） | 刊会 / 年份 | 代码核验 |
|---|---|---|---|
| [Counting from Sky: A Large-Scale Data Set for Remote Sensing Object Counting and a Benchmark Method](https://doi.org/10.1109/TGRS.2020.3020555) | 发布大规模遥感目标计数数据集与基线，建立卫星/航拍视角下的密度估计评测。 | IEEE TGRS 2021 | [作者代码与数据](https://github.com/gaoguangshuai/Counting-from-Sky-A-Large-scale-Dataset-for-Remote-Sensing-Object-Counting-and-A-Benchmark-Method) |
| [IS-Count: Large-Scale Object Counting from Satellite Images with Covariate-Based Importance Sampling](https://ojs.aaai.org/index.php/AAAI/article/view/21462) | 面向卫星图像大规模计数，使用协变量重要性采样减轻训练样本分布与目标区域分布偏差。 | AAAI 2022 | [官方代码](https://github.com/sustainlab-group/IS-Count) |
| [Object Counting for Remote-Sensing Images via Adaptive Density Map-Assisted Learning (ADMAL)](https://doi.org/10.1109/TGRS.2022.3208326) | 通过自适应密度图辅助训练高分辨率遥感目标计数器，针对目标密集与空间分布变化优化计数。 | IEEE TGRS 2022 | [作者代码与预训练模型](https://github.com/gcding/ADMAL-pytorch) |
| [Distillation Remote Sensing Object Counting via Multi-Scale Context Feature Aggregation](https://doi.org/10.1109/TGRS.2021.3125249) | 通过多尺度上下文特征聚合与知识蒸馏，压缩遥感计数模型并保留稠密目标表征。 | IEEE TGRS 2022 | 未找到可访问的作者官方模型代码。 |
| [PSGCNet: A Pyramidal Scale and Global Context Guided Network for Dense Object Counting in Remote-Sensing Images](https://doi.org/10.1109/TGRS.2022.3153946) | 以金字塔尺度特征和全局上下文引导密度预测，处理遥感图像中尺度跨度大的密集对象。 | IEEE TGRS 2022 | [作者代码](https://github.com/gaoguangshuai/PSGCNet) |
| [Global Multi-Scale Information Fusion for Multi-Class Object Counting in Remote Sensing Images](https://doi.org/10.3390/rs14164026) | 融合全局与多尺度特征，面向遥感图像中的多类别计数。 | Remote Sensing 2022 | 未找到可访问的作者官方模型代码。 |
| [Object Counting in Remote Sensing via Triple Attention and Scale-Aware Network](https://doi.org/10.3390/rs14246363) | 结合三重注意力与尺度感知模块，增强背景复杂场景下多尺度目标的密度估计。 | Remote Sensing 2022 | 未找到可访问的作者官方模型代码。 |
| [Density Map-based Vehicle Counting in Remote Sensing Images with Limited Resolution](https://doi.org/10.1016/j.isprsjprs.2022.05.004) | 针对有限分辨率遥感图像中的车辆密集/粘连问题构建密度计数方法。 | ISPRS JPRS 2022 | [RSVC2021 仓库](https://github.com/YinongGuo/RSVC2021-Dataset)仅为数据/数据生成资源，不是本文模型代码。 |
| [Cross-Region Building Counting in Satellite Imagery using Counting Consistency](https://doi.org/10.1007/s00521-023-08923-0) | 以计数一致性应对不同区域卫星影像的域偏移，面向跨区域建筑物数量估计。 | Neural Comput. Appl. 2023 | [作者代码](https://github.com/intelligentMachines-ITU/domain-Adaptive-Building-Counting) |
| [Remote Sensing Object Counting Through Regression Ensembles and Learning to Rank](https://doi.org/10.1109/TGRS.2023.3266884) | 集成回归与排序学习改善密集遥感图像中目标数估计及误差稳定性。 | IEEE TGRS 2023 | [作者代码](https://github.com/huangyongbobo/eFreeNet) |
| [A Lightweight Multiscale Feature Fusion Network for Remote Sensing Object Counting](https://doi.org/10.1109/TGRS.2023.3238185) | 以轻量多尺度特征融合兼顾遥感密集计数精度与计算开销。 | IEEE TGRS 2023 | 未找到可访问的作者官方模型代码。 |
| [NWPU-MOC: A Benchmark for Fine-grained Multi-category Object Counting in Aerial Images](https://arxiv.org/abs/2401.10530) | 构建多类别航拍计数基准与数据集，支持车辆、船舶等多类目标的细粒度评估。 | IEEE TGRS 2024 | [数据集、基准与代码](https://github.com/lyongo/NWPU-MOC) |
| [Few-Shot Object Counting With Dynamic Similarity-Aware in Latent Space (DSALVANet)](https://doi.org/10.1109/TGRS.2024.3350383) | 在潜在空间建立动态相似性度量，以少量目标示例适配航拍图像中的新类别/新场景。 | IEEE TGRS 2024 | [作者代码](https://github.com/kadvinj/DSALVANet) |
| [Hierarchical Kernel Interaction Network for Remote Sensing Object Counting](https://doi.org/10.1109/TGRS.2023.3348870) | 通过层级核交互捕获多尺度空间上下文，改善遥感对象密度图和计数预测。 | IEEE TGRS 2024 | 未找到可访问的作者官方模型代码。 |
| [DOPNet: Dense Object Prediction Network for Multi-Class Object Counting and Localization in Remote Sensing Images](https://doi.org/10.1109/TGRS.2024.3349702) | 联合预测密度与目标位置，面向多类别遥感对象计数和定位。 | IEEE TGRS 2024 | [作者代码](https://github.com/Ceoilmp/DOPNet) |
| [Balanced Density Regression Network for Remote Sensing Object Counting](https://doi.org/10.1109/TGRS.2024.3402271) | 通过平衡密度回归缓解密度标注/样本分布偏斜，提升遥感密集计数。 | IEEE TGRS 2024 | [作者代码](https://github.com/HotChieh/BDRNet) |
| [Uncertainty-aware Continuous Implicit Neural Representations for Remote Sensing Object Counting](https://proceedings.mlr.press/v238/xu24k.html) | 使用连续隐式表示和不确定性估计建模密度场，减少栅格密度预测对目标尺度的限制。 | AISTATS 2024 | [作者代码](https://github.com/SiyuanXu-tamu/UNIC) |
| [ResCount: A Residual Feature Fusion Network for Ship Counting in Remote Sensing Images](https://doi.org/10.1109/LGRS.2024.3462444) | 面向遥感船舶图像融合残差特征，以密度预测完成船只计数。 | IEEE GRSL 2024 | 未找到可访问的作者官方模型代码。 |
| [Remote Sensing Object Counting With Online Knowledge Learning](https://arxiv.org/abs/2303.10318) | 用在线知识学习适应遥感图像中的变化目标与场景分布，降低新场景持续适配的标注负担。 | IEEE TGRS 2025 | 未找到可访问的官方实现；论文记录：[arXiv](https://arxiv.org/abs/2303.10318)。 |
| [Counting Beyond Domains: A Cross-Domain Benchmark and Method for Remote Sensing Object Counting](https://doi.org/10.1109/TGRS.2025.3622599) | 建立跨域遥感计数评测并提出跨域适配方案，面向地域、传感器与影像风格变化。 | IEEE TGRS 2025 | [作者代码](https://github.com/jwang-rs/CBD-pytorch) |
| [Input-Regulated Remote Sensing Counting With Region Understanding](https://doi.org/10.1109/TGRS.2025.3639196) | 以图驱动输入调节器筛选有用特征，并通过动态区域理解增强少标注遥感计数的判别性。 | IEEE TGRS 2025 | 本轮未确认公开官方代码；[作者机构论文页](https://researchers.mq.edu.au/en/publications/input-regulated-remote-sensing-counting-with-region-understanding/)。 |
| [Cross-Domain Density Map-Generated Ship Counting Network for Remote Sensing Images](https://doi.org/10.1109/LGRS.2024.3510093) | 通过域适配与密度图生成提升不同分布遥感场景中的船舶计数。 | IEEE GRSL 2025 | 未找到可访问的作者官方模型代码。 |
| [Mamba-MOC: Multi-Category Object Counting in Remote Sensing Images Based on Mamba](https://doi.org/10.1109/IGARSS55030.2025.11243409) | 将 Mamba 状态空间模块用于遥感多类别计数，建模大幅面影像中的长程上下文。 | IGARSS 2025 | 未找到可访问的作者官方模型代码。 |
| [EdgeCount: Efficient Remote Sensing Object Counting via Edge-Guided Feature Learning](https://doi.org/10.1109/TCVST.2024.3469933) | 以边缘引导特征强化小目标轮廓，研究遥感对象计数的精度与效率。 | IEEE TCSVT 2025 | 未找到可访问的作者官方模型代码。 |
| [Scale-Invariant Implicit Neural Representations for Remote Sensing Object Counting](https://doi.org/10.1109/CVPRW67362.2025.00217) | 以尺度不变连续隐式表示估计遥感目标密度；属于 EarthVision workshop 论文而非 CVPR 主会。 | CVPRW EarthVision 2025 | 未找到可访问的作者官方模型代码。 |
| [See What We Cannot See: A Geo-guided Reasoning Benchmark for Object Counting under Adverse Earth Observation Conditions (GROC)](https://openaccess.thecvf.com/content/CVPR2026/html/Wang_See_What_We_Cannot_See_A_Geo-guided_Reasoning_Benchmark_for_CVPR_2026_paper.html) | 构建地理引导推理基准，评估遥感/地球观测图像在恶劣成像条件下的目标计数与空间推理。 | CVPR 2026 | 截至检索日未找到可访问的作者代码仓库。 |
| [SCOUT-Count: Stylization with covariance-whitening and uncertainty for domain-generalized remote sensing object counting](https://www.sciencedirect.com/science/article/abs/pii/S0924271626003369) | 以风格扩增、协方差白化与不确定性建模缓解遥感计数的跨地域/跨分辨率域偏移。 | ISPRS JPRS 2026 | [论文所列代码](https://github.com/WindermerePeaks/SCOUT-Count) |
| [RS-OVC: Open-Vocabulary Counting for Remote-Sensing Data](https://arxiv.org/abs/2604.08704) | 将文本和/或视觉条件引入遥感目标计数，使模型无需针对新航拍类别重新训练；与常见遥感闭集计数直接区分。 | ICPR 2026 | [官方 PyTorch 实现](https://github.com/tamirshor7/RS-OVC) |
| [GACENet: Global Adaptive Context Enhancement Network for Remote Sensing Object Counting](https://doi.org/10.1109/TGRS.2026.3679358) | 通过全局自适应上下文增强解决大视场遥感图像中的密度变化与尺度差异。 | IEEE TGRS 2026 | 未找到可访问的作者官方模型代码。 |
| [S2C-Net: Scale-Sensitive Contextual Counting Network for Remote Sensing Images](https://doi.org/10.1109/TGRS.2026.3693659) | 以尺度敏感上下文聚合处理遥感密集计数中的目标尺寸变化。 | IEEE TGRS 2026 | [作者仓库](https://github.com/xuptLHj/S2C-Net)可访问，提供压缩包资源；尚未独立验证训练复现完整性。 |
| [Scale-Aware Gated Routing Distillation Network for Remote Sensing Object Counting (SAGRD)](https://doi.org/10.3390/rs18172939) | 以尺度感知门控路由与蒸馏增强遥感图像多尺度目标计数。 | Remote Sensing 2026 | 未找到可访问的作者官方模型代码。 |
| [HierarchicalGeoCount: Hierarchical Geometric Feature Learning for Zero-Shot Remote Sensing Object Counting](https://doi.org/10.1016/j.jvcir.2026.104793) | 研究零样本遥感计数，以层级几何特征迁移到训练中未见的遥感对象类别。 | J. Vis. Commun. Image Represent. 2026 | 未找到可访问的作者官方模型代码。 |
| [TreeMatch: Tree-Structured Matching for Cross-Domain Object Counting](https://arxiv.org/abs/2606.24786) | 以树结构匹配处理跨域目标计数，包含遥感/航拍场景评测；属于通用方法而非遥感专用模型。 | ECCV 2026 | [作者代码与数据](https://github.com/dgominski/treematch) |
| [COBICount: Counting Objects in the Wild with Contextual Bias Mitigation](https://arxiv.org/abs/2609.39366) | 面向野外复杂背景和域变化的计数研究，包含遥感场景；论文计划发布代码，但截至截止日未找到公开仓库。 | arXiv 2026 预印本 | 未找到可访问的公开官方代码。 |
| [VesselBench-800K: A Large-Scale Benchmark for Vessel Detection and Counting in Satellite Imagery](https://arxiv.org/abs/2609.37003) | 面向卫星船舶检测/计数的大规模数据基准，重点在数据与评测资源。 | arXiv 2026 预印本 | 论文承诺数据/代码资源；所指 [GitHub 仓库](https://github.com/danfenghong/IEEE_TGRS_VesselBench)核验时不可访问，故标为未公开可用。 |

<a id="agricultural-fruit-counting"></a>
## 三、农业果实计数

果实计数的细目（按年、摘要、期刊简称及逐项代码状态）集中维护在[农业果实计数年度表](fruit-counting.md#agricultural-fruit-annual-tables)，避免在跨领域目录中重复整份果园文献清单。该表截至 2026-10-11 收录 74 篇直接计数/田间负载研究；其中花、花簇等生殖负载代理与成熟果实计数有单独标记。新增核验显示，代码“存在”不等于代码“可复现”：下表明确区分模型实现、数据/辅助脚本和未发现公开仓库。

| 论文 | 主要内容（中文释义） | 刊会 / 年份 | 代码核验 |
|---|---|---|---|
| [Benchmarking Dense and Indiscernible Object Counting with Blueberries](https://proceedings.mlr.press/v306/bo26a.html) | ICML 2026 的农业计数代表作：发布 DIOCblueberry 密集蓝莓基准，提出 MaskCount，以 CLIP 伪掩膜、对比学习和边缘感知裁剪应对小目标、遮挡与叶果混淆。 | ICML 2026 | [数据集](https://huggingface.co/datasets/weihao-bo/DIOCblueberry)已发布；截至检索日未找到可访问的官方 MaskCount 模型代码。 |
| [A Dynamic Kalman Filtering Method for Multi-Object Fruit Tracking and Counting in Complex Orchards](https://pmc.ncbi.nlm.nih.gov/articles/PMC12252135/) | 结合改进 YOLO、动态 Kalman 预测和外观关联，在复杂果园视频中持续跟踪并计数果实。 | Sensors 2025 | [论文数据声明所列作者代码](https://github.com/zhaiyaning/Fruit_Tacking) |
| [Apple phenotyping using deep learning and 3D depth analysis: An experimental study on fruitlet sizing during early development](https://www.sciencedirect.com/science/article/pii/S2772375525001972) | 结合 RGB-D 视频和深度估计，对苹果幼果簇计数并测量果径；报告平均计数误差 0.63 个幼果/视频。 | Smart Agric. Technol. 2025 | [作者代码与数据处理流程](https://github.com/checolag/apple-fruitlet-detection-and-sizing) |
| [BerryFlowerNet: A Customized Convolutional Neural Network for Blueberry Flower Cluster Detection and Flowering Stage Prediction with a Field Phenotyping Robot](https://www.mdpi.com/2077-0472/16/11/1159) | 以田间机器人采集蓝莓开花至绿果图像，检测/计数花簇并预测花期，是产量预测中的生殖负载代理。 | Agriculture 2026 | [作者实验室代码与数据](https://github.com/UGA-BSAIL/BerryFlowerNet) |
| [Unified Multi-Level Grape Counting Framework with Low Annotation Cost for Natural Orchard Scenes](https://doi.org/10.3390/app16157500) | UniGC 联合葡萄粒点计数、葡萄串检测/计数与逐串果粒数估计，训练依赖点与框标注。 | Appl. Sci. 2026 | [作者代码与数据](https://github.com/xiaofengxie-dl/UniGC) |
| [Probability map-based grape detection and counting](https://www.sciencedirect.com/science/article/pii/S0168169924005660) | 以概率图联合定位葡萄簇和果粒，并输出整图/逐簇果粒数。 | CEA 2024 | [作者代码](https://github.com/volcanoYcc/Probability-Map-based-Grape-Detection-and-Counting) |
| [Advancing tracking-by-detection with MultiMap: Towards occlusion-resilient online multiclass strawberry counting](https://www.sciencedirect.com/science/article/pii/S0957417424014544) | 多特征在线匹配增强遮挡场景下的草莓多类别跟踪计数。 | ESWA 2024 | [作者代码](https://github.com/Xuehaiz/MultiMap) |
| [Mask-GK: An efficient method based on mask Gaussian kernel for segmentation and counting of grape berries in field](https://www.sciencedirect.com/science/article/pii/S0168169925003928) | 用 mask Gaussian kernel 表示葡萄粒实例，结合田间分割完成果粒计数。 | CEA 2025 | [作者代码](https://github.com/volcanoYcc/Mask-GK) |
| [A precise berry counting method for in-cluster grapes to guide berry thinning](https://www.frontiersin.org/journals/plant-science/articles/10.3389/fpls.2025.1739688/full) | 联合密度估计与果穗分割，估计整图和逐穗葡萄粒数量以支持疏果。 | Front. Plant Sci. 2025 | [作者代码](https://github.com/AWEN975/MVDNet_code) |

<a id="class-agnostic-counting"></a>
## 四、类无关、示例驱动与弱监督计数（开放计数邻近方向）

这些方法可能支持未见类别，但测试时通常需要示例、交互或图像级监督；与“输入新文本即可计数”的严格文本开放词汇定义不同。这里保留代表性工作，避免把 CAC/few-shot 统称为 zero-shot。

| 论文 | 主要内容（中文释义） | 刊会 / 年份 | 代码核验 |
|---|---|---|---|
| [Learning to Count Everything](https://openaccess.thecvf.com/content/CVPR2021/html/Ranjan_Learning_To_Count_Everything_CVPR_2021_paper.html) | 通过少量示例学习跨类别计数，是通用/类无关少样本计数的重要基线。 | CVPR 2021 | [作者代码](https://github.com/cvlab-stonybrook/LearningToCountEverything) |
| [Exemplar-Free Class-Agnostic Counting](https://openaccess.thecvf.com/content/ACCV2022/papers/Ranjan_Exemplar_Free_Class_Agnostic_Counting_ACCV_2022_paper.pdf) | 研究测试时不提供视觉示例的类无关计数，利用 objectness 与重复性推断新类别实例。 | ACCV 2022 | 本轮未确认到稳定可访问的作者代码仓库。 |
| [LOCA: A Low-Shot Object Counting Network with Iterative Prototype Adaptation](https://openaccess.thecvf.com/content/ICCV2023/html/Dukic_A_Low-Shot_Object_Counting_Network_with_Iterative_Prototype_Adaptation_ICCV_2023_paper.html) | 以少量框选示例迭代更新类别原型，逐步适配图像中的目标外观和尺度。 | ICCV 2023 | [作者代码](https://github.com/val-iisc/LOCA) |
| [PseCo: Point, Segment and Count: A Generalized Framework for Object Counting](https://openaccess.thecvf.com/content/CVPR2024/papers/Huang_Point_Segment_and_Count_A_Generalized_Framework_for_Object_Counting_CVPR_2024_paper.pdf) | 统一点、分割和计数监督，以视觉示例适配通用计数。 | CVPR 2024 | [作者代码](https://github.com/Hzzone/PseCo) |
| [DAVE: A Detect-and-Verify Paradigm for Low-Shot Counting](https://openaccess.thecvf.com/content/CVPR2024/html/Pelhan_DAVE_-_A_Detect-and-Verify_Paradigm_for_Low-Shot_Counting_CVPR_2024_paper.html) | 采用先检测候选、再验证目标相似性的低样本计数流程，降低密集场景的重复/漏计。 | CVPR 2024 | [作者代码](https://github.com/jerpelhan/DAVE) |
| [GeCo: A Novel Unified Architecture for Low-Shot Counting by Detection and Segmentation](https://proceedings.neurips.cc/paper_files/paper/2024/file/7a0f8055c838df8e62329a76c7c6403d-Paper-Conference.pdf) | 将检测与分割整合为低样本计数框架，通过示例提示对任意类别计数。 | NeurIPS 2024 | [作者代码](https://github.com/jerpelhan/GeCo) |
| [A Simple-but-Effective Baseline for Training-Free Class-Agnostic Counting](https://openaccess.thecvf.com/content/WACV2025/html/Lin_A_Simple-but-Effective_Baseline_for_Training-Free_Class-Agnostic_Counting_WACV_2025_paper.html) | 通过超像素点提示、语义特征编码、多尺度处理和转导式原型更新，提升无需额外训练的示例驱动类无关计数。 | WACV 2025 | 未在论文/作者页确认到公开官方实现；勿将第三方清单当作代码证据。 |
| [Counting with Ease: Class-Agnostic Counting via One-Shot Detection across Diverse Domains (CACAL)](https://doi.org/10.1016/j.neunet.2025.107961) | 用单个查询示例进行跨域类无关计数与定位，并提出覆盖工业、农业和日常场景的 LOCO 基准。 | Neural Networks 2025 | [同名作者仓库](https://github.com/imMid-Star/CACAL)目前只含 README/License，README称数据仍在整理；未见模型实现或可下载数据，**不计为已开源代码**。 |
| [FocalCount: Towards Class-Count Imbalance in Class-Agnostic Counting](https://arxiv.org/abs/2502.10677) | 关注类无关计数中的类别数量偏置，估计类别数并通过 Focal-MSE 加强对少见类别计数误差的惩罚。 | arXiv 2025 预印本 | 论文写明代码将发布；截至检索日未找到公开仓库。 |
| [Generalized-Scale Object Counting with Gradual Query Aggregation (GeCo2)](https://ojs.aaai.org/index.php/AAAI/article/view/37780) | 逐步跨尺度聚合示例查询，在免切块方案下处理尺度差异大、密集且细小的少样本目标。 | AAAI 2026 | [官方实现](https://github.com/jerpelhan/GECO2) |
| [CountingDINO: A Training-free Pipeline for Class-Agnostic Counting using Unsupervised Backbones](https://openaccess.thecvf.com/content/WACV2026/html/Pacini_CountingDINO_A_Training-free_Pipeline_for_Class-Agnostic_Counting_using_Unsupervised_Backbones_WACV_2026_paper.html) | 使用自监督 DINO 特征和示例原型，在无训练/标注的推理设置下完成类无关计数。 | WACV 2026 | [官方实现](https://github.com/lorebianchi98/CountingDINO) |
| [CountZES: Counting via Zero-Shot Exemplar Selection](https://arxiv.org/abs/2512.16415) | 自动选择无需人工标注的视觉示例，再进行跨场景计数；“zero-shot”指示例自动获取，任务仍属示例条件计数。 | arXiv 2025 预印本 | [作者代码](https://github.com/Muhammad-Ibraheem-Siddiqui/CountZES) |
| [Bootstrapping MLLM for Weakly-Supervised Class-Agnostic Object Counting (WS-COC)](https://arxiv.org/abs/2602.12774) | 用图像级数量监督引导多模态大模型进行类无关计数，采用范围二分对话、图像计数排序与全局/局部融合降低点级标注需求；不是文本开放词汇计数。 | ICLR 2026 | [作者代码](https://github.com/viscom-tongji/WS-COC) |
| [OCCAM: Class-Agnostic, Training-Free, Prior-Free and Multi-Class Object Counting](https://arxiv.org/abs/2601.13871) | 利用 SAM2 与聚类尝试无训练、无示例的多类别类无关计数。 | arXiv 2026 预印本 | 论文给出代码/数据将公开的项目地址，但截至检索日未确认到可用实现：[OCCAM 项目页](https://mikespanak.github.io/OCCAM_counter)。 |
| [Spatially-Aware Class-Agnostic Object Counting (UpCount)](https://arxiv.org/abs/2607.16826) | 通过多层 ViT 特征、空间细化与候选验证改善结构复杂目标的类无关计数。 | arXiv 2026 预印本 | [作者代码](https://github.com/r28112072-rgb/upcount) |

<a id="counting-benchmarks"></a>
## 五、计数基准、推理与生成控制（邻近，不等同专用计数模型）

| 论文 | 主要内容（中文释义） | 刊会 / 年份 | 代码核验 |
|---|---|---|---|
| [Can Current AI Models Count What We Mean, Not What They See? A Benchmark and Systematic Evaluation (PairTally)](https://arxiv.org/abs/2509.13939) | 提出 PairTally：681 张高分辨率图像要求模型区分外观相似的目标子类，评估文本意图/细粒度选择计数，而不只是数显著重复物体。 | DICTA 2025 / arXiv 2025 | [作者基准、数据与评测代码](https://github.com/bbvisual/PairTally_Benchmark)公开；提供多个模型的评测适配器，不是新的计数模型。 |
| [Teaching CLIP to Count to Ten](https://openaccess.thecvf.com/content/ICCV2023/html/Paiss_Teaching_CLIP_to_Count_to_Ten_ICCV_2023_paper.html) | 研究视觉语言模型对物体数量/数词的理解与计数能力，重点是数量推理，不是密度图式的目标实例计数方法。 | ICCV 2023 | 本轮未确认到公开官方代码。 |
| [UNICBench: UNIfied Counting Benchmark for MLLM](https://openaccess.thecvf.com/content/CVPR2026/html/Rong_UNICBench_UNIfied_Counting_Benchmark_for_MLLM_CVPR_2026_paper.html) | 面向多模态大语言模型的统一计数评测基准；用于分析 MLLM 计数能力，不应与专用开放词汇检测/计数器混为一类。 | CVPR 2026 | 本轮未确认到可访问的官方代码仓库。 |
| [Mitigating Noise-Induced Layout Priors for Object Counting in Diffusion Models](https://proceedings.mlr.press/v306/gu26f.html) | 通过调整扩散初始噪声与早期注意力布局，使文生图结果更符合提示中的目标数量；属于计数控制/图像生成，不是对已有图像做实例计数。 | ICML 2026 | [论文所列代码](https://github.com/lxlong1201/Mitigate_Noise_Prior) |

## 按会议快速定位

- **CVPR**：Zero-Shot Object Counting (2023)、PseCo / DAVE (2024)、T2ICount (2025)、CountGD++ / QICA / GROC / UNICBench (2026)。
- **ICCV**：LOCA (2023，少样本)、CountSE / 文本引导局部排序 (2025)、YOLO-Count (2025，生成交叉)。
- **AAAI**：IS-Count (2022，遥感)、VLCounter (2024)、OmniCount (2025)、CountVid (2026，视频)。
- **ACM MM**：CLIP-Count (2023)、SDVPT / TrueCount (2025，开放世界/多模态提示)、Depth-Guided Video Object Counting (2026，RGB-D 视频)。其中 SDVPT 代码已公开但训练/测试功能部分待补；TrueCount 本轮未找到作者官方代码。**NeurIPS**：CountGD、GeCo (2024)。**ECCV**：VA-Count (2024)、CountEx / DualCount / TreeMatch (2026)。
- **ICLR**：本专题核实到 WS-COC (2026)，属于弱监督类无关计数，并非文本提示开放词汇计数。**ICML**：核实到 MaskCount 蓝莓计数 (2026，农业场景)及计数控制/生成论文；截至截止日未确认 ICML 主会发表严格文本开放词汇计数器。**NeurIPS 2026**：截至 2026-10-11 尚无可核验的当年会议论文集，不将预印本提前算作正式发表。
- **WACV / 期刊**：TFCAC (WACV 2025，训练免示例计数)、CACAL (*Neural Networks*, 2025，单示例跨域计数)属于类无关/少样本邻近方向，不应标成文本开放词汇主会模型。
- **遥感期刊/会议**：AAAI、IEEE TGRS、CVPR、ISPRS JPRS 与 ICPR 均有相关工作；其中明确以文本/视觉提示计数未见类别的 RS-OVC 是 ICPR 2026。

以上列表是截至检索日可核验记录的专题汇总，不声称覆盖所有应用领域或所有尚未公开的代码。预印本、会议接收稿与正式出版信息分别标注；后续如论文正式发表、代码开放或链接失效，应以出版商/会议页面和作者仓库更新状态。
