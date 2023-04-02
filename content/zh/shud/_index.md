---
title: SHUD建模系统
author: R package build
date: '2021-02-01'
linktitle: 概述
summary: Overview of the SHUD modeling system.
type: book
weight: 999
---

**SHUD模型用户手册:**
[https://shud.xyz/book_cn](https://shud.xyz/book_cn)


## 概述

SHUD (Simulator for Hydrologic Unstructured Domains，水文非结构域模拟器)模型，是一个多时间尺度、多空间尺度、物理性的分布式水文模型，使用有限体积方法（Finite Volume Method）求解水文微分方程的数学模型。此模型可提供跟高时空分辨率的水文模拟，计算能力超过常见的水文模型。SHUD模型中水文变量求解空间由三角形构成（如Delaunay三角形），采用有限体积方法和全域隐式求解法，保证全域和局地水量平衡。

\begin{aligned}
&s(\varphi) \frac{\partial h}{\partial t}=\nabla[-k(\varphi) \cdot \nabla(\varphi+z)] \\
&\frac{\partial h}{\partial t}+\nabla(u h)=q
\end{aligned}

SHUD模拟洪水淹没、水文跟踪、地上地下水交互等等方面拥有其他产流模型完全无法替代的优势。模型已在中国、美国及非洲各地有诸多研究案例

SHUD模型基于对空间水文动态的物理性描述，构建起地表、土壤、地下水和河道水全耦合的水文模型。

SHUD模型是分布式水文模型，水文模拟空间由三角形构成，采用有限体积方法和全域隐式求解法，保证全域和局地水量平衡。
![](/media/shud.png)

## 致谢

以下单位在SHUD模型的发展给予大力支持，在此深表感谢:

- 中国科学院
- 中国科学院西北生态环境资源研究院
- 宾夕法尼亚州立大学（Pennsylvania State University)
- 加州大学戴维斯分校（University of California Davis）
- 美国自然科学基金（National Science Foundation）
- 美国环保署（Environmental Protection Agency）
- 美国国防高级研究计划局（The Defense Advanced Research Projects Agency）
