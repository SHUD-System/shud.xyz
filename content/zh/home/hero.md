---
widget: hero
headless: true
weight: 1
title: SHUD水文模拟系统
hero_media: hero.png
cta:
  label: 三维模型
  url: https://www.shud.xyz/gallery/shud3d
cta_alt:
  label: '模型说明书'
  url: https://www.shud.xyz/Book_CN/

cta_note:
  label: >-
    <a class="js-github-release" href="https://github.com/SHUD-System/SHUD" data-repo="SHUD-System/SHUD">模型源代码<!-- V --></a>
design:
  background:
    gradient_end: 'LightBlue'
    gradient_start: 'DeepSkyBlue'
    text_color_light: true
advanced:
  css_class:
math: true  
---

SHUD(Simulator for Hydrologic Unstructured Domains)是地表地下耦合的数值方法水文模型(Surface-Subsurface Integrated Hydrologic Model with Numeric Method)，是多尺度、多过程、高时间分辨率、灵活空间分辨率、地表-地下紧密耦合、有限体积法求解的分布式水文模型。

**空间结构**：非结构三角网格组成流域，三角形单元为最小计算单元，在垂直方向上分为地表、未饱和层以及饱和层；单元间差异性即反映水文参数的空间异质性。

**时间步长**：可变时间步长。模型自适应搜寻满足收敛条件的时间步长。内部迭代步长为1秒~10分钟。

SHUD具有物理过程清晰、时间分辨率高、空间表达更接近真实、数值求解效率高、模型适应性强、扩展性强等显著优势，并在世界多地的洪水预报、水资源评价、土地利用影响评价、湖泊生态、农业经济、以及学科交叉耦合等科研应用上得到验证。
SHUD模型已在北美、亚洲和非洲的23个流域得到应用，流域尺度覆盖0.08 $km^2$ 至70,000 $km^2$ 面积范围，空间分辨率从米至公里级；时间尺度上可实现天至百年长度的连续模拟。
