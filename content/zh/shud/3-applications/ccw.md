---
title: "Cache Creek流域模拟"
date: 2019-11-22T00:15:07-07:00
draft: false
math: true
# Tags and categories
# For example, use `tags = []` for no tags, or the form `tags = ["A Tag", "Another Tag"]` for one or more tags.
tags: []
categories: []
# Academic page type (do not modify).
type: book
weight: 1
---



### Cache河流域（Cache Creek Watershed）

CCW是北萨克拉门托河上游的一个支流，面积196.4平方公里（下图），海拔高程450米至1800米，平均坡度38% $ L/L $（陡峭地形是对数值方法水文模型的挑战）。

![Location and data for Cache Creek Watershed](/media/app/CacheCreek/sac5_map.png)

根据2000-2017年间，NLDAS-2数据，流域内平均气温12.8度，年降雨量817毫米，然而降雨年内、年际分布不均，属于典型地中海气候——降雨集中在冬天、夏天温度高且 干旱无雨。

![Precipitation and temperature](/media/app/CacheCreek/sac5_PT.png)

### 模拟和调参

Our simulation in CCW covers the period from 2000 to 2007. Because of the Mediterranean climate in this region, the simulation starts in summer to ensure adequate time before the October start to the water year. In our experiment, the first year (2000-06-01 to 2001-06-30) is the spin-up period, the following two years (2001-07-01 to 2003-06-30 ) are the calibration period, and the period from 2003-07-01 to 2007-07-01 is for validation.

The unstructured domain of the CCW (Fig. 1(d)) is built with rSHUD, a R package on GitHub ([rSHUD]( https://github.com/shud-system/rSHUD)). The number of triangular cells is 1147, with a mean area of $ 0.17 km^2$. The total length of the river network is $126.5 km$ and consists of 103 river reaches and in which the highest order of stream is 4. With a calibrated parameter set, the SHUD model tooks 5 hours to simulate 17 years in the CCW, with a non-parallel configuration (OpenMP is disabled on *Mac Pro 2013 Xeon 2.7GHz, 32GB RAM*).

### 结果

Figure below reveals the comparison of simulated discharge against the observed discharge at the gage station of [USGS 11451100](https://waterdata.usgs.gov/ca/nwis/uv/?site_no=11451100).
The calibration procedure exploits the Covariance Matrix Adaptation -- Evolution Strategy (CMA-ES) to calibrate automatically \citep{Hansen2016}. The calibration program assigns 72 children in each generation and keeps the best child as the seed for next-generation, with limited perturbations. The perturbation for the next generation is generated from the covariance matrix of the previous generation. After 23 generations, the calibration tool identifies a locally optimal parameter set.

![The hydrograph in calibration and validation period](/media/app/CacheCreek/sac5_hydrograph_daily.png)

We use the groundwater distribution (Fig. below) to demonstrate the spatial distribution of hydroligcal metrics calculated from the SHUD model.

Figure below illustrates the annual mean groundwater table in the validation period. Because the model fixes a $30 m$ aquifer, the results represent the groundwater within this aquifer only.
 The groundwater table and elevation along the green line on the upper map are extracted and plotted in the bottom figure. The gray ribbon is the $30 m$ aquifer, and the blue line is the location where groundwater storage is larger than zero. The green polygons with the right axis are the groundwater storage along the cross-section.  The groundwater follows the terrain, with groundwater accumulated in the valley, or along relatively flat plains. In the CCW, the groundwater is very deep or does not stay on the steep slope.


![Groundwater spatial distribution map](/media/app/CacheCreek/sac5_rgw.png)

![The groundwater condition along the cross-section line](/media/app/CacheCreek/sac5_sgw.png)

![Water balance in the simulation period](/media/app/CacheCreek/sac5_wb.png)


## 数据公开
本研究的数据已经公开： [![DOI](https://zenodo.org/badge/226413148.svg)](https://zenodo.org/badge/latestdoi/226413148)
 或者 [Github: https://github.com/Model-Intercomparison-Datasets/Cache-Creek](https://github.com/Model-Intercomparison-Datasets/Cache-Creek).
 气象数据占用空间较大，如有需要，请直接联系作者[Lele Shu](mailto:shulele@lzb.ac.cn)。
