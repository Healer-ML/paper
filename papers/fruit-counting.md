# 农业/田间果实计数论文调研（2021–2026）

[返回三方向论文总览](README.md) · [跨模态检索目录](../README.md) · [微表情识别目录](micro-expression-recognition.md)

**检索截止：2026-10-11。** 本表聚焦农业田间、果园、葡萄园、温室及采收作业场景中的果实计数，重点覆盖 2024–2026。检索采用多轮关键词检索与引文追溯，并逐项核对出版商论文页、作者/实验室论文页或 arXiv 原文；代码链接仅在论文、作者页或明确的作者 GitHub 仓库核验后列出。

## 纳入标准与标记

- **A｜直接计数**：论文输出并评估果实/果簇/浆果数量；包括检测后计数、跨帧去重、密度图、点监督、实例分割和多视角/3D 计数。
- **B｜田间负载/估产**：对单株、果园或采收区的果实负载/数量估计有直接验证；可能进一步用计数做产量回归。
- **P｜生殖负载代理**：花、花簇、花蕾或幼果计数，用于疏花疏果或早期产量预测；不是成熟果实计数。
- **邻近/排除**：只做果实检测、成熟度识别或一般产量回归，且未核验到果实数量评估的，不列入主表；在文末列出边界案例。

年份按期刊卷期/会议论文年份归类；在线优先发表年份与卷期年不一致时单独注明。代码状态“未核验”表示未在论文或作者页面确认到官方代码，不等同于断言代码不存在。数据集链接不当作代码链接。

## 2021

| 论文题目 | 摘要（中文释义） | 刊会简称 | 代码 |
| --- | --- | --- | --- |
| [Fruit detection and load estimation of an orange orchard using the YOLO models through simple approaches in different imaging and illumination conditions](https://www.sciencedirect.com/science/article/pii/S0168169921005500) | 用 YOLO 在自然橙园图像中检测并汇总果数，比较成像与光照条件，验证果数和估产相关性。（范围：A/B） | CEA | 未核验 |
| [Design, development, and performance evaluation of a robot for yield estimation of kiwifruit](https://www.sciencedirect.com/science/article/pii/S0168169921001502) | 履带式田间机器人沿猕猴桃棚架采图，用视觉检测与回归估计果数。（范围：A/B） | CEA | 未核验 |
| [Estimation of Fruit Load in Australian Mango Orchards Using Machine Vision](https://www.mdpi.com/2073-4395/11/9/1711) | 多视角机器视觉评估澳大利亚芒果园树级/园级负载，并与包装线实际数量比较，讨论负载制图和采收规划。（范围：B） | Agronomy | 未核验 |
| [Attempting to Estimate the Unseen—Correction for Occluded Fruit in Tree Fruit Load Estimation by Machine Vision with Deep Learning](https://www.mdpi.com/2073-4395/11/2/347) | 用冠层可见图像特征学习遮挡修正因子，减少不可见果实造成的负载低估；在 880 棵树上与包装线计数比较。（范围：B） | Agronomy | 未核验 |
| [Reliability of a commercial platform for estimating flower cluster and fruit number, yield, tree geometry and light interception in apple trees under different rootstocks and row orientations](https://www.sciencedirect.com/science/article/pii/S0168169921005366) | 验证商用果园传感平台对苹果花簇、果数、产量和树体参数的估计可靠性。（范围：A/B） | CEA | — |
| [End-to-End Automatic Berry Counting for Table Grape Thinning](https://doi.org/10.1109/ACCESS.2020.3048374) | 面向鲜食葡萄疏果，提出端到端葡萄粒计数网络并用于单穗浆果数量估计。（范围：A） | IEEE Access | 未核验 |

## 2022

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

## 2023

| 论文题目 | 摘要（中文释义） | 刊会简称 | 代码 |
| --- | --- | --- | --- |
| [Apple orchard production estimation using deep learning strategies: A comparison of tracking-by-detection algorithms](https://www.sciencedirect.com/science/article/abs/pii/S0168169922008213) | 系统比较苹果园视频中的检测-跟踪组合及其果数/产量估算表现。（范围：A/B） | CEA | 未核验 |
| [NDMFCS: An automatic fruit counting system in modern apple orchard using abatement of abnormal fruit detection](https://www.sciencedirect.com/science/article/pii/S0168169923004246) | YOLOv4-tiny 检测、异常检测剔除和树干跟踪身份分配组成完整苹果计数流程。（范围：A） | CEA | 未核验 |
| [Twice matched fruit counting system: An automatic fruit counting pipeline in modern apple orchard using mutual and secondary matches](https://www.sciencedirect.com/science/article/pii/S1537511023001885) | 利用互匹配与二次匹配降低跨帧 ID 切换和重复计数，给出现代苹果园果数估计。（范围：A） | Biosyst. Eng. | 未核验 |
| [Real-time tracking and counting of grape clusters in the field based on channel pruning with YOLOv5s](https://www.sciencedirect.com/science/article/pii/S0168169923000509) | 剪枝轻量化 YOLOv5s 并结合视频跟踪，实现田间葡萄串实时计数。（范围：A） | CEA | 未核验 |
| [Semi-supervised Counting of Grape Berries in the Field Based on Density Mutual Exclusion](https://www.sciopen.com/article/10.34133/plantphenomics.0115) | 半监督密度图计数，设计密度互斥约束以缓解浆果密集重叠。（范围：A） | Plant Phenomics | [Code](https://github.com/youth-tang/CDMENet-main) |
| [Instance Segmentation and Berry Counting of Table Grape before Thinning Based on AS-SwinT](https://www.sciopen.com/article/10.34133/plantphenomics.0085) | Swin Transformer 实例分割葡萄粒，并回归单穗果数，用于疏果前评估。（范围：A） | Plant Phenomics | 未核验 |
| [Tomato cluster detection and counting using improved YOLOv5 based on RGB-D fusion](https://www.sciencedirect.com/science/article/pii/S0168169923001291) | 融合 RGB-D 检测番茄簇，并以 ByteTrack 与计数区域消除重复；机器人实测平均计数准确率 95.1%。（范围：A） | CEA | 未核验 |
| [An efficient online citrus counting system for large-scale unstructured orchards based on the unmanned aerial vehicle](https://onlinelibrary.wiley.com/doi/10.1002/rob.22147) | 无人机在线采集非结构化果园图像，跟踪并计数柑橘，针对跟踪失误设计非均匀分布计数器。（范围：A） | J. Field Robot. | 未核验 |
| [Tree-level citrus yield prediction utilizing ground and aerial machine vision and machine learning](https://www.sciencedirect.com/science/article/pii/S2772375522000429) | 融合无人机树体特征与地面单/双侧柑橘计数，建立树级产量预测。（范围：B） | SAT | 未核验 |
| [Seeing the Fruit for the Leaves: Robotically Mapping Apple Fruitlets in a Commercial Orchard](https://arxiv.org/abs/2308.07512) | 机器人從果树两侧扫描并构建商业苹果园幼果地图，评估幼果可见性和计数。（范围：P/A） | IROS | 未核验 |
| [UAV Photogrammetry-Based Apple Orchard Blossom Density Estimation and Mapping](https://www.mdpi.com/2311-7524/9/2/266) | 用无人机影像和摄影测量点云估计苹果花密度并制图，服务于早期负载管理。（范围：P） | Horticulturae | 未核验 |

## 2024

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

## 2025

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

## 2026（截至 2026-10-11）

| 论文题目 | 摘要（中文释义） | 刊会简称 | 代码 |
| --- | --- | --- | --- |
| [Low-annotation apple flower counting: A color-SAM enhanced and uncertainty-guided semi-supervised framework](https://www.sciencedirect.com/science/article/pii/S2643651526000270) | Color-SAM 与不确定性引导半监督密度估计用于少标注苹果花计数。（范围：P） | Plant Phenomics | [Code](https://github.com/haohuihui5019/USCount-Net) |
| [Accurate counting of small and dense Chinese cherry in natural orchard via fruit-oriented perception and sharpening network](https://www.sciencedirect.com/science/article/abs/pii/S0168169926005041) | FOPSN 密度图计数网络针对小目标、黏连和自然果园复杂背景优化。（范围：A） | CEA | 未核验 |
| [YOLO11-SBS: leveraging ACE and ORCM to gauge robust and accurate apple counting in complex orchards](https://www.frontiersin.org/journals/plant-science/articles/10.3389/fpls.2026.1841916/full) | 改进 YOLO11 在复杂果园图像中检测并统计苹果，重点关注遮挡和背景干扰。（范围：A） | Front. Plant Sci. | 未核验 |
| [Automated oil palm fruit counting using deep learning for reliable yield estimation in natural background](https://www.sciencedirect.com/science/article/pii/S2772375526006015) | 对自然背景下油棕鲜果串图像进行检测计数，比较 YOLOv5s、YOLOv8n 与 Mask R-CNN，并报告计数误差。（范围：A/B） | SAT | 未核验 |
| [Agrosense v2: An AI-enabled system for precision orchard sensing and tree-level monitoring](https://www.sciencedirect.com/science/article/pii/S0168169926003923) | 真实柑橘园集成树识别、地理定位和果实检测计数，将树上/地面果数汇总为树级时空信息。（范围：A/B） | CEA | 未核验 |
| [Research on Greenhouse Eggplant Fruit Detection and Tracking-Based Counting Using an Improved YOLOv5s-DeepSORT](https://www.mdpi.com/2077-0472/16/2/253) | 改进 YOLOv5s-DeepSORT 对温室茄子视频跟踪并按计数区统计。（范围：A） | Agriculture | 未核验 |
| [Tomato Maturity Classification and Fruit Counting Based on RGB and Multispectral Images](https://www.mdpi.com/2076-3417/16/7/3227) | 检测-跟踪去重后按 RGB/多光谱特征识别成熟度并统计不同成熟阶段的番茄数量。（范围：A） | Appl. Sci. | 未核验 |
| [Simultaneous Maturity Recognition and Yield Counting of Truss and Individual Tomatoes Using Improved YOLOv8-EME and Optimized ByteTrack Tracker](https://www.mdpi.com/2311-7524/12/10/1199) | YOLOv8-EME 与优化 ByteTrack 同时识别番茄串、单果成熟度并分别计数。（范围：A） | Horticulturae | 未核验 |
| [A lightweight multi-view detection and counting method for real-time cherry tomato yield estimation using greenhouse inspection robots](https://www.sciencedirect.com/science/article/pii/S2772375526004843) | 面向巡检机器人的轻量检测-跟踪-计数-补偿管线，使用多视角信息减少遮挡导致的漏计。（范围：A/B） | SAT | 未核验 |
| [Video-based fruit detection and tracking: effects of scanning conditions on fruit load estimation](https://doi.org/10.1016/j.compag.2026.112330) | 在 420 棵苹果树上比较 RGB-D 相机、扫描距离、日期和单/双侧扫描对视频计数、采收真值与负载图的影响。（范围：A/B） | CEA | 未核验 |

## 边界案例：不纳入主表或仅作邻近参考

- **只做果实检测/成熟度识别**：若论文只报 mAP、检测/分割精度，没有果数误差、数量估计或计数实验，则不算直接计数。例如部分绿柑橘检测、番茄成熟度检测、果实尺寸/采摘点定位工作。即便标题写有“fruit detection”，也不自动纳入。
- **[FGfuse-Net: A frequency guided dual-branch fusion model for multi-stage maturity tomato detection and counting](https://www.sciencedirect.com/science/article/pii/S2772375526004144)**，*Smart Agricultural Technology* 14, 102194 (2026), DOI [10.1016/j.atech.2026.102194](https://doi.org/10.1016/j.atech.2026.102194)：题名包含 counting，但目前核验到的摘要/亮点主要是检测性能，未确认独立计数误差结果，因此暂列邻近，不计入主表数量。
- **[A Seamless Deep Learning Approach for Apple Detection, Depth Estimation, and Tracking Using YOLO Models Enhanced by Multi-Head Attention Mechanism](https://www.mdpi.com/2073-431X/13/3/83)**，*Computers* 13(3), 83 (2024), DOI [10.3390/computers13030083](https://doi.org/10.3390/computers13030083)：主要做检测、深度与跟踪；未确认独立果数评估，故不作为直接计数论文。
- **[MFFT: an improved method for stable ID tracking and counting of multi-class mango segmentation with multi-feature fusion in complex occlusion scenarios](https://www.sciencedirect.com/science/article/pii/S0168169926007441)**，*CEA* 253, 112149 (2026-10)：出版商页面目前可见，摘要报告计数相对误差 4.30%、生物量估计误差 4.49%，并给出 Google Drive 代码和数据；但页面只精确到 2026 年 10 月，未显示具体上线日，因此无法判断是否在 2026-10-11 截止日前正式上线。作为**截止日边界记录**保留，不计入截至日主表。[Code + 数据（Google Drive）](https://drive.google.com/file/d/1UzvgiqlXn-C2aJZsHmcLAWSYaVYA0bnH/view?usp=sharing)
- **[Adapting SAM3 for 3D fruit counting with cross-view contrastive learning and Hough voting](https://www.sciencedirect.com/science/article/pii/S0168169926009233)**，*CEA* 112325：页面显示为 2026 年 12 月，晚于本次截止日，排除；虽有作者公开代码 [SAM3-3DFruit](https://github.com/kkk0216/SAM3-3DFruit)，不代表论文已在截止日前发表。
- 苹果花、花簇、花蕾、幼果论文列在主表但标为 **P**，因为它们对疏花疏果/早期负载有用，却不能与成熟果实计数混为一类。

## 2026 果园估产综述（背景阅读；不计入原始研究篇数）

| 论文题目 | 摘要（中文释义） | 刊会简称 | 代码 |
| --- | --- | --- | --- |
| [A review: research progress on intelligent technologies for orchard yield monitoring](https://www.frontiersin.org/journals/plant-science/articles/10.3389/fpls.2026.1879872/full) | 总结 RGB/RGB-D、LiDAR、多/高光谱、UGV/UAV 与目标检测、实例分割、多目标跟踪、点云和多模态融合，将果数/负载监测作为产量监测中间环节。 | Front. Plant Sci. | — |
| [Research progress on precision orchard yield estimation based on multi-source information perception sensors](https://www.frontiersin.org/journals/plant-science/articles/10.3389/fpls.2026.1759956/full) | 依 PRISMA 思路综述机器视觉、光谱遥感、多源融合与果园平台；指出融合有助提升稳健性，但遮挡、数据异质性和跨场景适配仍是难点。 | Front. Plant Sci. | — |

## 覆盖范围结论

本轮检索所得论文主要分布在 CEA、Smart Agricultural Technology、Plant Phenomics、Agronomy、Biosystems Engineering、农业机器人/传感期刊及作者预印本。CV 旗舰会议中，核验到的是 **CVPR Workshop Vision4Ag** 的苹果遮挡/低帧率计数工作，而不是 CVPR 主会论文；本轮定向检索没有找到可核验的 ICCV、ACM MM 主会直接农业果实计数论文。这个结论是本次检索范围内的观察，不应理解为证明相关论文绝对不存在。

方法趋势上，2021–2022 年较多为单图检测、颜色/传统视觉与初步跟踪；2023–2024 年逐渐出现密度图/点监督、概率图、跨帧去重、UAV 在线采集和多视角 3D；2025–2026 年研究进一步转向多物种泛化、遮挡鲁棒、RGB-D/三维场景、边缘部署、成熟度联合计数和果园级负载图。代码可复现性仍不均衡：本表仅对能由论文/作者信息核验到的官方实现打了 Code 链接，其余明确写“未核验”。
