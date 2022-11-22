---
# Page title
title: 模型简介

# Title for the menu link if you wish to use a shorter link title, otherwise remove this option.
linktitle: 1.1 模型简介

# Page summary for search engines.
summary: 介绍SHUD模型的结构和特点

# Date page published
date: 2021-01-23

# Academic page type (do not modify).
type: book

# Position of this page in the menu. Remove this option to sort alphabetically.
weight: 10

---


##	SHUD模型的基本结构
SHUD模型利用非结构三角网格表达模拟区域的水平方向空间异质性。模型同时支持规则三角形和Delaunay不规则三角形（Triangular Irregulate Network），但因为流域空间的不规则特点，Delaunay不规则三角形更便于表达。空间上每个三角形单元视为最小坡面计算单元，单元内水文参数具有一致性。
坡面单元在垂直方向上分为三层：地表，未饱和层和饱和层。地表计算植被截留、积雪、下渗和的表

SHUD模型基于Duffy(1996) “两态耦合平衡”认知模型将土壤水层分为未饱和和饱和层，并使用局部平衡公式计算水的流动。

## SHUD模型的特征与优势

-	SHUD模型是一个物理性分布式水文模型，精确描述流域水文物理过程。物理性模型可用于无观测流域的模拟研究。
-	SHUD很好的表达了流域中的空间异质性。水文空间异质性的表达有利于耦合模型研究，例如详细的描述了水从山坡回流的路径，有利于生物化学、污染物运动、地貌变迁、湖泊生态等等方面的耦合研究。
-	SHUD是全耦合模型，在每一时间不步长所有水文状态量都要满足基本求解器的收敛性要求，保证了水文便利在空间上的连续性、一致性和收敛性。
-	SHUD模型使用CVODE 5.0+(Hindmarsh et al., 2005) 作为常微分方程求解器。 CVODE由劳伦斯利弗莫尔国家实验室开发和维护。
-	SHUD可使用灵活的时间和空间步长，适应多种尺度的模拟需求。
-	SHUD支持高空间时间分辨率的洪水模拟，也支持长时间序列的气候和土地利用变化研究。
-	SHUD是开源模型，任何人（非商业用途）都可使用、修改此模型。

## SHUD模型应用

模型地图

### 中国
#### 黑河
#### 黄河源区
#### 宁夏省
#### 岩画村，宁夏

### 美国
#### Conestoga Watershed， 宾夕法尼亚
#### Sacramento Watershed, 加尼福尼亚
#### Sunapee Lake, 新罕布什尔
#### Mendota Lake， 威斯康辛
#### 休斯敦洪水，德克萨斯


### 非洲
#### Pongo， 南苏丹
#### 埃塞俄比亚
