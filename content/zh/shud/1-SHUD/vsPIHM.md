---
# Page title
title: 站在巨人肩上

# Title for the menu link if you wish to use a shorter link title, otherwise remove this option.
linktitle: 1.2 对比PIHM

# Page summary for search engines.
summary: 与PIHM模型的对比

# Date page published
date: 2020-11-23

# Academic page type (do not modify).
type: book

# Position of this page in the menu. Remove this option to sort alphabetically.
weight: 19

---

## 站在巨人肩上

SHUD的源代码是全新书写的，但其基本的认知模型来自Duffy(1996)提出的“二态耦合平衡”，其数学模型借鉴PIHM（Penn State Integrated Hydrological Model)。SHUD的出现得益于PIHM模型的突破和经验积累。

### PIHM模型简史

Duffy于1996年构建了计算土壤水和地下水动态的“二态耦合平衡”模型(Duffy, 1996)；该模型中，垂直方向分为饱和与非饱和层，局地水量平衡公式耦合计算水的交换。“二态耦合平衡”模型在简化水文动态的同时，保留了自然中时空尺度对产流的响应。 之后Brandes 和Duffy 等 (1998) 继承了“二态耦合平衡”模型并使用FEMWATER实现了数值方法计算山坡-河流尺度上水双向交互。 2004年，曲轶众(Qu 2004)在算法中加入了蒸散发过程和河道计算，并发布了Penn State Integrated Hydrologic Model (PIHM)——**PIHM v1.0**，是PIHM发展中最重要的里程碑，从此PIHM成为流域模拟的通用研究工具应用在不同尺度的流域中。

此后， Kumar， Bhartt和Duffy (Kumar et al., 2009; Kumar and Duffy, 2009) 又相继开发了PIHM v2.0和PIHMgis。 PIHM v2.0增强了模型中陆面过程和土地利用影响水文过程的计算过程。Gopal Bhartt 开发了生成PIHM输入、读取输出和分析结果的软件PIHMgis。PIHMgis分别出现了PIHMgis v2.3和v3.0两个常用版本，PIHMgis v2.3使用了QGIS内核，因此在部分平台上更新困难。 PIHMgis v3.0的支持性更好，可支持Mac或Windows操作系统。Leonard (2013) 开发了HydroTerre平台，为PIHM和其他水文模型提供基础的空间和时间数据。 PIHMgis和HydroTerre的出现极大的推动了PIHM模型在全美和全球的应用。

受益于PIHM模型的诸多优势，PIHM家族出现了若干耦合模型。 例如，Flux-PIHM将NOAH陆面过程模型与PIHM模型耦合，更精确的计算陆面与大气的能量交换、 蒸散发和积雪 (Shi et al., 2015, 2014)。张宇等(Zhang et al. 2016) 开发了LE-PIHM, 模型万年尺度由水文过程造就的地形地貌变化。 RT-PIHM 和 RT-Flux-PIHM(Bao, 2016; Bao et al., 2017)实现了化学反应与PIHM水文过程的耦合。由石宇宁领导的研究正试图将各种PIHM相关模型作为模块统一建立多模块PIHM系统（Multi-Module PIHM， MM-PIHM， https://github.com/PSUmodeling/MM-PIHM）。 除此之外，仍有多个与PIHM耦合的研究正在进行，如与湖泊、农业、经济的耦合研究。

在PIHM模型快速发展的同时，Kumar (Kumar et al., 2009)，在PIHM v2.0基础上设计了 Finite volume-based Integrated Hydrologic Modeling (FIHM)模型，使用二阶精度和三维流动模拟水文过程。

下图展示了PIHM模型的发展和分支。

![Figure_tree](/media/Figure_tree.png)
Figure 1: PIHM和SHUD模型的发展和分支。 PIHMgis和rSHUD分别是支持PIHM和SHUD的数据前后处理工具。 PIHMgis使用C++写成，rSHUD使用R.

### SHUD与PIHM的区别

SHUD模型是PIHM的一个继承者，继承了1996年由Duffy提出的二相耦合概念模型，并且继承了部分PIHM 1.0和2.0的应用经验。之后作者修改了模型中空间结构、物理过程、算法以及编程语言，SHUD模型已经与PIHM在模型物理结构、文件格式和计算方法上不再兼容，因此使用新名称对模型进行命名，以体现新模型自身特点。

SHUD与PIHM的区别：

1. SHUD使用C++面向对象编程，将计算封装起来，避免内存泄露等PIHM常见问题。
2. SHUD使用了不同的坡面与河道的交互。PIHM中河道与两个三角形坡面相邻，带来了四个问题：1. 河道的长度极大的影响和模型的计算单元数量，用户不得不在简单河道和计算单元数量之间做权衡。2. 平原地区的河道绵延曲折，导致大量微小三角形单元和非结构三角形，使得模型计算容易突破库容常数而使得模型变慢。3. 容易出现局部积水点（sink），个别积水点就可以极大的拖慢整个流域的求解速度。 4. 为解决以上问题，模型用户需要反复手动对河流形状进行修改，降低了模型的可重复性和效率。SHUD的河道覆盖在三角形单元之上，坡面和河道水量交换给予河道水位和地下水、地表水的坡度计算，整体计算效率显著提升。
3. SHUD模型中计算入渗、地下水补给和河流交互的公式与PIHM不同。公式的采用基于经验和模型设计时效的需求。未来将会就此进行模型对比，展示两个计算模式的差异。
4. SHUD模型确保了计算中的水量平衡。

在技术层面SHUD模型：

- 支持CVODE 5.0及以上版本
- 支持OpenMP并行计算
- 采用和与PIHM不同的数据结构和算法
- 支持可读性强的输入和输出文件
- 统一的时间序列数据操作
- 指定步长输出模型状态，作为后续模型运行的初始条件。
- 自动检查模型的输入数据和参数的有效性
- 加入模型调试选项，监控每一步长内的非法值和内存操作。
