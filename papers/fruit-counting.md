# 果实计数目录：农业应用与跨领域计数（2021–2026）

[返回三方向论文总览](README.md) · [跨模态检索目录](../README.md) · [微表情识别目录](micro-expression-recognition.md)

[跨领域计数专题：开放计数、遥感计数与类无关计数](counting-research.md)

**检索截止：2026-10-11。** 下方年度折叠表统一收录农业果实计数，以及遥感/航拍、开放词汇/开放世界、类无关/少样本、视频和相关评测论文；类别标签写在摘要开头。跨类别论文只在一个发表年份表格中保留一条，不重复计数。跨领域方法不等于已在果园数据上验证，类别边界与代码核验详见[计数专题说明](counting-research.md)。

## 研究方向分类

| 方向 | 表格标记 | 研究范围与核验 |
| --- | --- | --- |
| 农业/田间果实 | `【农业果实】` 或原有范围 A/B/P | 果园、田间、温室果实/果簇/浆果计数、负载估计与花/幼果代理。 |
| 遥感/航拍 | `【遥感计数】` | 卫星、航空和无人机目标计数；仅检测、无计数评估的不纳入。完整边界：[遥感专题](counting-research.md#remote-sensing-counting)。 |
| 开放词汇/开放世界 | `【开放计数】` | 文本、视觉示例或多模态提示指定未见类；纯文本、示例提示分别区分。详见[开放计数专题](counting-research.md#open-vocabulary-counting)。 |
| 类无关/少样本 | `【类无关/少样本】` | 依赖视觉示例、交互或弱监督的通用计数，不等同于文本零样本。详见[类无关计数专题](counting-research.md#class-agnostic-counting)。 |
| 视频/基准/邻近 | `【视频计数】`、`【计数基准】`、`【计数推理】` | 年度表中保留并明确标注视频唯一目标、基准和生成控制等相邻工作。 |

<a id="datasets-by-direction"></a>
## 各方向常用数据集与下载状态

**核验日期：2026-10-11。** 下表根据本目录收录论文及其官方项目页整理，给出可复用的数据集入口；并非每篇论文都使用本表全部数据。`可直接下载`表示官方托管页提供数据文件或下载入口；`部分公开/有条件`表示需要账号、遵守许可、从原始数据源重建，或部分标注/测试集受限；`未确认`表示目前没有核验到稳定的公开数据包。代码仓库存在，不代表数据集本身公开。

**方向直达：** [农业果实](#dataset-agriculture) · [遥感/航拍](#dataset-remote-sensing) · [开放词汇/指代表达](#dataset-open) · [类无关/少样本](#dataset-class-agnostic) · [视频/序列](#dataset-video)

<a id="dataset-agriculture"></a>
### 农业果实计数、估产与三维计数

| 数据集 | 对应论文/任务 | 下载状态与入口 |
| --- | --- | --- |
| **MinneApple** | 苹果检测、单图计数/密度估计；本目录中的苹果果园计数工作常用基准。 | **可直接下载。** [明尼苏达大学数据仓库项目页](https://rsn.umn.edu/projects/orchard-monitoring/minneapple)；[计数补丁集](https://conservancy.umn.edu/bitstream/handle/11299/206575/counting.tar.gz?sequence=1&isAllowed=y)、[检测集](https://conservancy.umn.edu/bitstream/handle/11299/206575/detection.tar.gz?sequence=2&isAllowed=y)、[测试数据](https://conservancy.umn.edu/bitstream/handle/11299/206575/test_data.zip?sequence=16&isAllowed=y)；[作者代码](https://github.com/nicolaihaeni/MinneApple)。 |
| **ACFR Orchard / Multi-Fruit** | 苹果、芒果、杏仁等果园图像；检测、树上果数估计及产量相关研究。 | **可直接下载（按页面许可使用）。** [悉尼大学 ACFR 数据页](https://data.acfr.usyd.edu.au/ag/treecrops/2016-multifruit/)。该资源是果园多果种图像集，不应等同于统一的密度图计数基准。 |
| **BlueberryDCM** | 蓝莓冠层图像中的果实检测、成熟度识别和计数；对应 2024 年蓝莓计数论文。 | **可直接下载。** [Zenodo 数据记录](https://zenodo.org/records/14002517)（BlueberryDCM.7z）；[论文配套代码](https://github.com/vicdxxx/BlueberryDetectionAndCounting)。数据页记录的是 140 张 RGB 图像及框标注，使用时以该版本说明为准。 |
| **DIOCblueberry** | ICML 2026 蓝莓密集、遮挡及叶片干扰计数；含点计数与示例框标注。 | **可直接下载。** [Hugging Face 数据集页](https://huggingface.co/datasets/weihao-bo/DIOCblueberry)；页面提供数据预览与文件访问。 |
| **MetaFruit** | 多物种果实负载估计；对应 *Multi-Species Fruit-Load Estimation Using Deep Learning Models*，覆盖五类果实。 | **公开但需 Kaggle 账号/遵守平台条款。** [MetaFruit 数据集页](https://www.kaggle.com/datasets/jiajiali/metafruit)。论文使用的数据版本和标注口径应以论文及 Kaggle 页面为准。 |
| **FruitNeRF Real / Synthetic** | 多视角果实重建、跨视角去重与三维果实计数；FruitNeRF / FruitNeRF++。 | **可直接下载，体积较大。** [Zenodo 数据记录](https://zenodo.org/records/10869455)：真实数据约 19.1 GB、合成数据约 7.8 GB；[项目代码](https://github.com/meyerls/fruitnerf)。 |

本目录收录的苹果、柑橘、猕猴桃、番茄等不少田间论文使用作者自采果园/温室图像或视频。若论文/作者页没有公开数据声明，本表不把它们标成“不可下载”，而是视为**未确认公开**；这类数据通常需联系论文作者获取。

<a id="dataset-remote-sensing"></a>
### 遥感/航拍目标计数

| 数据集 | 对应论文/任务 | 下载状态与入口 |
| --- | --- | --- |
| **RSOC / Counting from Sky** | 遥感图像多类目标密度估计与计数；本目录收录的 Counting from Sky 基准及后续遥感计数研究。 | **部分公开。** [作者数据/代码仓库](https://github.com/gaoguangshuai/Counting-from-Sky-A-Large-scale-Dataset-for-Remote-Sensing-Object-Counting-and-A-Benchmark-Method)提供建筑子集下载入口；其他子集部分依赖 DOTA 源数据及仓库提供的文件清单。建筑子集：[百度网盘](https://pan.baidu.com/s/19hL7O1sP_u2r9LNRsFSjdA)，提取码 `nwcx`。 |
| **NWPU-MOC** | 航拍车辆、船舶等细粒度多类别计数；对应 TGRS 2024 基准及后续遥感计数论文。 | **可下载，需按镜像要求访问。** [作者官方仓库及数据说明](https://github.com/lyongo/NWPU-MOC)；[Google Drive 数据入口](https://drive.google.com/file/d/1AHOBAzOag0jlH3cLjukXdMYsCJhYaiOi/view?usp=drive_link)，仓库另列百度网盘镜像。 |
| **RSVC2021** | 有限分辨率遥感车辆密度计数；用于数据生成/评测的影像与密度图资源。 | **部分公开/需按说明重建。** [作者数据生成仓库](https://github.com/YinongGuo/RSVC2021-Dataset)。这是数据与生成脚本入口，不是对应论文的模型代码包；可能需要准备其依赖的源影像。 |
| **CARPK / PUCPR+** | 无人机视角车辆计数；常作为航拍密集计数和类无关计数迁移评测集。 | **可下载，需遵守数据许可。** [作者项目页及下载入口](https://lafi.github.io/LPN/)。这是车辆计数基准，不是农田作物或果实计数数据。 |
| **GROC** | CVPR 2026 地球观测恶劣天气/成像条件下的地理辅助计数与推理基准。 | **公开下载，部分标签受限。** [Hugging Face 数据集](https://huggingface.co/datasets/jwang-rs/GROC)（页面标注数据约 42.9 GB）；[作者项目/代码](https://github.com/jwang-rs/GROC)。测试标签未全部公开，需按项目说明联系作者。 |
| **DOTA / DIOR / FAIR1M（RS-OVC 使用）** | RS-OVC 等开放词汇遥感计数方法将目标检测数据转换为计数/点标注评测。 | **源数据可分别获取，但不是专门计数集。** [DOTA 官方页](https://captain-whu.github.io/DOTA/dataset.html)、[DIOR OpenDataLab](https://opendatalab.com/OpenDataLab/DIOR)、[FAIR1M 国家对地观测数据页](https://www.noda.ac.cn/datasharing/datasetDetails/666fe818d67b985a5113eb26)；再运行 [RS-OVC 转换与实验流程](https://github.com/tamirshor7/RS-OVC)。各数据集许可和申请条件独立。 |

<a id="dataset-open"></a>
### 开放词汇、零样本与指代表达计数

| 数据集 | 对应论文/任务 | 下载状态与入口 |
| --- | --- | --- |
| **FSC-147** | 通用类无关/少样本计数的核心基准，也常用于文本开放计数和零样本方法评测。 | **可下载。** [作者官方仓库及图像下载说明](https://github.com/cvlab-stonybrook/LearningToCountEverything)；[FSC-147 图像](https://drive.google.com/file/d/1ymDYrGs9DSRicfZbSCDiOu0ikGDh5k6S/view?usp=sharing)、[密度图/标注镜像](https://archive.org/details/FSC147-GT)。 |
| **FSC-147-D** | 在 FSC-147 上增加文本描述/目标名称，用于文本条件开放计数（如 CounTX）。 | **标注可从项目仓库获取；图像复用 FSC-147。** [CounTX 作者仓库](https://github.com/niki-amini-naieni/CounTX)；[项目页](https://robots.ox.ac.uk/~vgg/research/countx/)。 |
| **FSC-133** | 从 FSC-147 清洗、重构得到的通用计数训练/评测版本；用于开放类别与少样本方法。 | **可按仓库说明获取。** [Learning to Count Anything 项目及数据说明](https://github.com/ActiveVisionLab/LearningToCountAnything)。 |
| **REC-8K** | CVPR 2024 指代表达计数：按属性、动作、上下文表达指定同类中的目标。 | **部分公开。** [作者代码、标注与预处理说明](https://github.com/sydai/referring-expression-counting)；仓库提供标注/数据准备脚本，但部分原始图像受上游数据许可限制，需从原数据集下载后重建。 |
| **ZSC-8K** | ICCV 2025 LGCount 文本零样本计数基准。 | **标注/生成脚本随项目提供，图像依赖上游数据源。** [LGCount 官方仓库](https://github.com/zaqai/LGCount)；按其 `util/generate_npy.py` 和数据说明准备。未核验到独立、完整的图像压缩包。 |
| **PairTally** | 细粒度意图计数基准，测试文本指定的目标子类是否被准确区分。 | **可按项目页下载。** [作者基准与评测仓库](https://github.com/bbvisual/PairTally_Benchmark)。 |
| **CoCount** | ECCV 2026 CountEx 基准，针对相似类的正例/排除式细粒度计数。 | **可直接下载。** [CoCount Hugging Face 数据集集合](https://huggingface.co/collections/BBVisual/cocount)；[训练集页面](https://huggingface.co/datasets/BBVisual/CoCount-train)及其他拆分见集合页。 |
| **MixCount** | 多类别混合场景的开放词汇计数数据集，含细粒度标注。 | **可直接下载。** [Hugging Face 数据集页](https://huggingface.co/datasets/CorentinDumery/MixCount)。 |
| **CLOC** | Count Anything 跨域开放计数，覆盖通用、遥感、农业、病理、细胞与微生物等领域。 | **部分公开。** [项目页](https://mengqi-lei.github.io/count-anything-projectpage/)说明数据/标注与可再分发子集；[作者仓库](https://github.com/Mengqi-Lei/count-anything)。部分图像来自受原始许可约束的数据集，需依照说明从源头获取并重建。 |

<a id="dataset-class-agnostic"></a>
### 类无关/少样本计数

| 数据集 | 对应论文/任务 | 下载状态与入口 |
| --- | --- | --- |
| **FSC-147 / FSC-133** | 视觉示例条件下的通用计数、跨类少样本泛化；也被开放词汇方法复用。 | **可下载。** 入口见上方 [FSC-147](#dataset-open) 与 [FSC-133](#dataset-open) 条目。不同论文可能采用原始版、清洗版或不同划分，复现实验时需核对 split。 |
| **MCAC** | 多数据集类无关计数，带类别/中心/框/遮挡等信息，评估跨场景和跨类别泛化。 | **可直接下载。** [MCAC 官方项目页与数据包](https://mcac.active.vision/)；[数据 ZIP](https://www.robots.ox.ac.uk/~lav/Datasets/MCAC/MCAC.zip)。 |
| **CARPK / PUCPR+** | 少样本/类无关方法迁移至航拍车辆计数的评测。 | **可下载，车辆域。** 入口见上方 [CARPK / PUCPR+](#dataset-remote-sensing) 条目。 |

<a id="dataset-video"></a>
### 视频与跨帧去重计数

| 数据集 | 对应论文/任务 | 下载状态与入口 |
| --- | --- | --- |
| **NeSTCount** | 2026 多物种移动相机田间序列计数，含葡萄柚、Sugar Belle、番茄和 Valencia 橙；用于跨帧去重、遮挡及移动视角评估。 | **数据包可下载，约 10.3 GB；原始帧有条件。** [Zenodo 数据记录](https://zenodo.org/records/21636487)提供公开数据文件；部分 raw frames 未随包分发，须按记录说明向作者申请。 |
| **CaseStudy / SensitivityAnalysis** | 苹果果园多序列视频/图像计数和扫描条件敏感性研究。 | **可下载。** [CaseStudy（Zenodo）](https://zenodo.org/records/7384297)；[SensitivityAnalysis（Zenodo）](https://zenodo.org/records/7383338)。下载体积较大，具体文件和真值版本见各记录页。 |
| **VideoCount / TAO-Count** | CountVid 的开放世界视频计数与唯一目标跨帧跟踪；TAO-Count 等公开视频源用于视频评测。 | **代码与部分标注可从作者仓库取得；原视频受上游条款约束。** [CountVid 官方仓库](https://github.com/niki-amini-naieni/CountVid)，依照 README 从对应源数据下载视频。 |
| **RGBD-VideoCount** | RGB-D 拥挤视频中的深度辅助计数与跨帧去重。 | **可直接下载。** [Hugging Face 数据集](https://huggingface.co/datasets/aerospace123/RGBD-VideoCount)；[论文配套代码](https://github.com/streamer-AP/DG-Net)。 |

**快速选集建议：** 做果园单图计数可先看 MinneApple、BlueberryDCM、DIOCblueberry；做跨品种负载估计可看 ACFR 与 MetaFruit；做多视角/三维计数可看 FruitNeRF；做遥感计数可从 RSOC、NWPU-MOC 或 GROC 入手；开放计数通常从 FSC-147 起步，再按任务选择 REC-8K、CoCount 或 MixCount；视频果园计数优先检查 NeSTCount 和苹果序列数据。不同数据集的标注粒度（框、点、密度图、视频轨迹）、许可、划分与计数口径并不统一，不能仅凭数据集名称直接横向比较。

每年仅保留一张四列表格（题目、中文摘要、刊会简称、代码）；以下年度数已计入所有类别。年度表中农业果实原有 **74 篇**完整保留；其它方向不再放在年度表外重复展示。代码状态按作者/论文关联仓库核验，数据集资源不冒充模型代码。

<a id="agricultural-fruit-annual-tables"></a>
## 2021–2026 各类别计数论文：逐年表

## 纳入标准与标记

- **A｜直接计数**：论文输出并评估果实/果簇/浆果数量；包括检测后计数、跨帧去重、密度图、点监督、实例分割和多视角/3D 计数。
- **B｜田间负载/估产**：对单株、果园或采收区的果实负载/数量估计有直接验证；可能进一步用计数做产量回归。
- **P｜生殖负载代理**：花、花簇、花蕾或幼果计数，用于疏花疏果或早期产量预测；不是成熟果实计数。
- **邻近/排除**：只做果实检测、成熟度识别或一般产量回归，且未核验到果实数量评估的，不列入主表；在文末列出边界案例。

年份按期刊卷期/会议论文年份归类；在线优先发表年份与卷期年不一致时单独注明。代码状态“未核验”表示未在论文或作者页面确认到官方代码，不等同于断言代码不存在。数据集链接不当作代码链接。

## 2021

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


## 2022

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


## 2023

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


## 2024

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


## 2025

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


## 2026（截至 2026-10-11）

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


## 边界案例：不纳入主表或仅作邻近参考

- **只做果实检测/成熟度识别**：若论文只报 mAP、检测/分割精度，没有果数误差、数量估计或计数实验，则不算直接计数。例如部分绿柑橘检测、番茄成熟度检测、果实尺寸/采摘点定位工作。即便标题写有“fruit detection”，也不自动纳入。
- **[FGfuse-Net: A frequency guided dual-branch fusion model for multi-stage maturity tomato detection and counting](https://www.sciencedirect.com/science/article/pii/S2772375526004144)**，*Smart Agricultural Technology* 14, 102194 (2026), DOI [10.1016/j.atech.2026.102194](https://doi.org/10.1016/j.atech.2026.102194)：题名包含 counting，但目前核验到的摘要/亮点主要是检测性能，未确认独立计数误差结果，因此暂列邻近，不计入主表数量。
- **[A Seamless Deep Learning Approach for Apple Detection, Depth Estimation, and Tracking Using YOLO Models Enhanced by Multi-Head Attention Mechanism](https://www.mdpi.com/2073-431X/13/3/83)**，*Computers* 13(3), 83 (2024), DOI [10.3390/computers13030083](https://doi.org/10.3390/computers13030083)：主要做检测、深度与跟踪；未确认独立果数评估，故不作为直接计数论文。
- **[MFFT: an improved method for stable ID tracking and counting of multi-class mango segmentation with multi-feature fusion in complex occlusion scenarios](https://www.sciencedirect.com/science/article/pii/S0168169926007441)**，*CEA* 253, 112149 (2026-10)：出版商页面目前可见，摘要报告计数相对误差 4.30%、生物量估计误差 4.49%，并给出 Google Drive 代码和数据；但页面只精确到 2026 年 10 月，未显示具体上线日，因此无法判断是否在 2026-10-11 截止日前正式上线。作为**截止日边界记录**保留，不计入截至日主表。[Code + 数据（Google Drive）](https://drive.google.com/file/d/1UzvgiqlXn-C2aJZsHmcLAWSYaVYA0bnH/view?usp=sharing)
- **[Adapting SAM3 for 3D fruit counting with cross-view contrastive learning and Hough voting](https://www.sciencedirect.com/science/article/pii/S0168169926009233)**，*CEA* 112325：页面显示为 2026 年 12 月，晚于本次截止日，排除；虽有作者公开代码 [SAM3-3DFruit](https://github.com/kkk0216/SAM3-3DFruit)，不代表论文已在截止日前发表。
- **年份口径说明：** *A precise berry counting method for in-cluster grapes to guide berry thinning* 按期刊卷期/DOI 年列在 2025；其在线发表日期为 2026-01-09。按卷期口径的主表归类不变，若按首次在线日期筛选则应视为 2026。
- 苹果花、花簇、花蕾、幼果论文列在主表但标为 **P**，因为它们对疏花疏果/早期负载有用，却不能与成熟果实计数混为一类。

## 2026 果园估产综述（背景阅读；不计入原始研究篇数）

<details>
<summary>农业果实计数与果园估产 · 2 篇</summary>

| 论文题目 | 摘要（中文释义） | 刊会简称 | 代码 |
| --- | --- | --- | --- |
| [A review: research progress on intelligent technologies for orchard yield monitoring](https://www.frontiersin.org/journals/plant-science/articles/10.3389/fpls.2026.1879872/full) | 总结 RGB/RGB-D、LiDAR、多/高光谱、UGV/UAV 与目标检测、实例分割、多目标跟踪、点云和多模态融合，将果数/负载监测作为产量监测中间环节。 | Front. Plant Sci. | — |
| [Research progress on precision orchard yield estimation based on multi-source information perception sensors](https://www.frontiersin.org/journals/plant-science/articles/10.3389/fpls.2026.1759956/full) | 依 PRISMA 思路综述机器视觉、光谱遥感、多源融合与果园平台；指出融合有助提升稳健性，但遮挡、数据异质性和跨场景适配仍是难点。 | Front. Plant Sci. | — |

</details>


## 覆盖范围结论

本轮检索所得论文主要分布在 CEA、Smart Agricultural Technology、Plant Phenomics、Agronomy、Biosystems Engineering、农业机器人/传感期刊及作者预印本。CV 旗舰会议中，核验到的是 **CVPR Workshop Vision4Ag** 的苹果遮挡/低帧率计数工作，而不是 CVPR 主会论文；本轮定向检索没有找到可核验的 ICCV、ACM MM 主会直接农业果实计数论文。这个结论是本次检索范围内的观察，不应理解为证明相关论文绝对不存在。

方法趋势上，2021–2022 年较多为单图检测、颜色/传统视觉与初步跟踪；2023–2024 年逐渐出现密度图/点监督、概率图、跨帧去重、UAV 在线采集和多视角 3D；2025–2026 年研究进一步转向多物种泛化、遮挡鲁棒、RGB-D/三维场景、边缘部署、成熟度联合计数和果园级负载图。代码可复现性仍不均衡：本表仅对能由论文/作者信息核验到的官方实现打了 Code 链接，其余明确写“未核验”。
