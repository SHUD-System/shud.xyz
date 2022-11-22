---
title: SHUD模型水文分析工具箱（rSHUD，R包)


# View.
#   1 = List
#   2 = Compact
#   3 = Card
view: 2

# Optional header image (relative to `static/media/` folder).
header:
  caption: ""
  image: ""
---

rSHUD源代码完全公开，可通过GitHub获取最新代码：[https://github.com/SHUD-System/rSHUD](https://github.com/SHUD-System/rSHUD)

## rSHUD功能：
1. 空间数据分析和操作。处理矢量和栅格数据，建立非结构三角网络。
2. 读/写SHUD模型的输入文件
3. 读取SHUD模型输出文件
4. 自动化模型调参
5. 水文数据时间序列分析
6. 二维三维数据可视化
7. GIS空间数据分析和统计
8. 获取公开的数据服务器数据，如气象在分析资料、美国地质调查局河流数据、modis遥感数据等等。


## 安装
在R环境中，直接运行以下代码，R的安装器将会安装完整的rSHUD到您的电脑。 安装成功一次即可。无需每次使用都更新代码；但当rSHUD代码更新后，建议重新使用以下命令重新安装。
```
install.packages("devtools")
devtools::install_github("SHUD-System/rSHUD")
```

## 提醒:
rSHUD安装需要使用`RTriangle`，但当前CRAN上的版本无法满足要求（截止2019年12月），请使用以下代码安装符合需要的RTriangle包：
```
install.packages("devtools")
devtools::install_github("shulele/RTriangle", subdir="pkg")
```
