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



design:
  background:
            # Name of image in `assets/media/`.
    image: bg.png
            # Darken the image? Range 0-1 where 0 is transparent and 1 is opaque.
    image_darken: 1
            #  Options are `cover` (default), `contain`, or `actual` size.
    image_size: cover
            # Options include `left`, `center` (default), or `right`.
    image_position: center
            # Use a fun parallax-like fixed background effect on desktop? true/false
    image_parallax: true
            # Text color (true=light, false=dark, or remove for the dynamic theme color).
    text_color_light: false
    #    gradient_end: 'LightBlue'
    #    gradient_start: 'DeepSkyBlue'
    #    text_color_light: true
  css_class: fullscreen
advanced:
  css_class: fullscreen
math: true  
---

SHUD(Simulator for Hydrologic Unstructured Domains)是地表地下耦合的数值方法水文模型，是多尺度、多过程、高时间分辨率、灵活空间分辨率、地表-地下紧密耦合、有限体积法求解的分布式水文模型。

**空间结构**：非结构三角网格组成流域，三角形单元为最小计算单元，在垂直方向上分为地表、未饱和层以及饱和层；单元间差异性即反映水文参数的空间异质性。

**时间步长**：可变时间步长。模型自适应搜寻满足收敛条件的时间步长。内部迭代步长为1秒~10分钟。

SHUD具有物理过程清晰、时间分辨率高、空间表达更接近真实、数值求解效率高、模型适应性强、扩展性强等显著优势，并在世界多地的洪水预报、水资源评价、土地利用影响评价、湖泊生态、农业经济、以及学科交叉耦合等科研应用上得到验证。

模型已在北美、亚洲和非洲的23个流域得到应用，流域尺度覆盖0.08 $km^2$ 至70,000 $km^2$ 面积范围，空间分辨率从米至公里级；时间尺度上可实现天至百年长度的连续模拟。

SHUD模型团队坚持开放道路，最新模型源代码可由github获取[https://github.com/SHUD-System/SHUD](https://github.com/SHUD-System/SHUD)。
