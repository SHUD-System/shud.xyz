---
# Page title
title: 全球水文数据云(GHDC)

# Title for the menu link if you wish to use a shorter link title, otherwise remove this option.
linktitle: 3. 全球水文数据云(GHDC)

# Page summary for search engines.
summary: 全球水文数据云

# Date page published
date: 2020-11-23

# Academic page type (do not modify).
type: book

# Position of this page in the menu. Remove this option to sort alphabetically.
weight: 30

---

![](/ghdc_CN/Figure/logo_cn.png)

## 数据平台介绍

全球水文数据云(Global Hydrologic Data Cloud, GHDC)，是一个快速获取水文建模基础数据，实现快速模型部署的云平台，可实现全球任意流域、任意大陆、任意国家范围快速水文模型部署。用户仅需提供欲建模的流域边界，GHDC即可自动化完成数据前处理，不仅生成建模所需要的基础数据（高程、土地利用、土壤质地、水系等），并能够制备SHUD(Simulator of Hydrologic Unstructured Domains)模型所需要的输入数据。用户可根据需要进行水文模拟、空间分析、数据挖掘等工作。

GHDC中文说明书：[https://shud.xyz/cn/ghdc_cn](https://shud.xyz/cn/ghdc_cn)

![GHDC的工作流程](/ghdc_CN/Figure/GHDC_flow.png)


### 版权和权益
GHDC并不生成数据，仅提供提供数据处理服务。数据版权和权益全部归属于原始数据的作者们。当前平台处理的数据全部为开放版权(Public Domains)的数据产品——允许数据处理、修改和重发布，放弃数据版权权益。本平台不提供未使用开放版权的数据产品的数据处理。例如GLDAS, NLDAS和FLDAS数据都使用了开放版权，本平台可提供数据处理服务；但是部分再分析数据资料未使用开放版权，因此本平台无法提供数据处理服务。 若用户需要未开放版权的数据集的处理任务，请联系网站作者[(shulele@lzb.ac.cn)](mailto:shulele@lzb.ac.cn)商讨。

### 原始数据源
当前可用数据见表：

| 数据分类 | 数据名称 | 数据属性 | 数据版权 | 数据源 | 
|:---------|:---------|:---------|:---------|:---------|
| 高程 | ASTER GDEM |  全球 30m| Public Domain |  |
| 土地利用 | USGS Land Cover  |  全球 1km| Public Domain |  |
| 土壤质地 |  HWSD v1.0 |   全球 1km | Public Domain |  |
| 气象再分析资料 | GLDAS |  全球 0.25度，1950至今| Public Domain |  |
| 气象再分析资料 | FLDAS |  全部部分区域 0.1度，1979至今| Public Domain |  |
| 气象再分析资料 | NLDAS |  美国 0.125度，1979至今 | Public Domain |  |
| 气象再分析资料 | CMFD |  中国 0.1度 | **版权私有** |  |
| 气象再分析资料 | CLDAS |  中国 0.125度 | **版权私有** |  |
| | | | | |

![ASTER Global DEM](/ghdc_CN/Figure/Aster_GDEM.png)
![GLDAS, FLDAS, NLDAS, NCA-LDAS覆盖范围](/ghdc_CN/Figure/ldas-domain.jpg)

## 如何获取数据

1. 提供流域边界，文件格式为ESRI Shapefile。请将Shapefile包含的四个基本子文件(.shp, .shx, .dbf, .shx)打包为.zip文件，并上传。
2. 提供模拟所需要的参数，包含项目名称、模拟年份、最小单元数，最大单元面积，含水层厚度等。
3. 填写邮箱地址，并提交任务。 请查看您的邮箱，GHDC会发送一封邮件；请点击邮箱内的确认链接。点击确认链接之后，GHDC才会启动数据处理任务。
4. GHDC数据处理完成后，会向您的邮箱再发送一封邮件，包含数据下载链接。
5. 请通过数据下载链接下载处理好的数据。
6. 模拟愉快~~~

## 数据引用

每个使用本平台的数据服务的用户都需要给GHDC平台建设者、程序开发者、SHUD模型作者和原始数据作者足够的学术肯定，因此**强烈建议您使用以下引用**。

- 数据服务和SHUD模型
    - Shu, L., Ullrich, P. A., & Duffy, C. J. (2020). Simulator for Hydrologic Unstructured Domains (SHUD v1.0): numerical modeling of watershed hydrology with the finite volume method. Geoscientific Model Development, 13(6), 2743–2762. https://doi.org/10.5194/gmd-13-2743-2020
    - Shu L.，Chang Y.，Wang J.，et al. A brief review of numerical distributed hydrological model SHUD［J］. Advances in Earth Science，2022，37（7）：680-691. DOI：10.11867/j.issn.1001-8166.2022.025.

- NLDAS 
    - Cosgrove, B. A. (2003). Real-time and retrospective forcing in the North American Land Data Assimilation System (NLDAS) project. Journal of Geophysical Research, 108(D22), 8842. https://doi.org/10.1029/2002JD003118

- Landuse, USGS 0.5 km MODIS-based Global Land Cover Climatology
    - Broxton, P.D., Zeng, X., Sulla-Menashe, D., Troch, P.A., 2014a: A Global Land Cover Climatology Using MODIS Data. J. Appl. Meteor. Climatol., 53, 1593-1605. doi: http://dx.doi.org/10.1175/JAMC-D-13-0270.1

## 致谢
本平台的开发受到多个机构的研究经费支持。

- 中国科学院率先行动“BR计划”：数值方法水文模型 
- 中国科学院寒旱区陆面过程与气候变化重点实验室：CLM-SHUD耦合模型研发 
- 青海省防灾减灾重点实验室开放基金项目：布哈河流域径流变化及水循环机理研究 
- 国家冰川冻土沙漠科学数据中心：水文模型自动化建模系统研发 
- 美国能源部(DOE)： Model Integration through Knowledge-Rich Data and Process Composition 
- 美国自然科学基金(NSE)：Knowledge-Guided Machine Learning: A Framework to Accelerate Scientific Discovery 



## 微信群

公众号二维码
![公众号](/ghdc_CN/Figure/gzh_search.png)



使用微信扫描二维码添加管理员，可以加入微信群。

![拉群微信](/ghdc_CN/Figure/shudxyz.jpeg)

