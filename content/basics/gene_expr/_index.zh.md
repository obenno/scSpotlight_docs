---
title: 查看基因表达
tags: ["documentation", "gene expression", "marker"]
categories: ["Introduciton"]
weight: 6
---

完成了细胞分群后, 单细胞分析中最频繁的需求应该就是查看基因表达了. scSpotlight
支持同时查看多个基因的[Seurat::FeaturePlot](https://satijalab.org/seurat/reference/featureplot), 也支持交互式展示的单个基因表达情况.

## 多基因表达

用户在右侧边栏**Feature Expression**模块可以输入多个基因的名字(symbol), 主界面
的细胞分群图会自动更新为这些基因表达的FeaturePlot.

![](featurePlot.png)

用户可以展开信息栏查看输入基因的[Seurat::DotPlot](https://satijalab.org/seurat/reference/dotplot)结果, 可以对照FeaturePlot和DotPlot
确认每个cluster的细胞类型, 例如下图中的cluster 2特异表达*MS4A1* (CD20), 可以确认为
B cell.

![](featurePlot_dotPlot.png)

## 单基因表达

用户在FeaturePlot中双击感兴趣的基因可以切换为单基因的表达. 类似Dotplot, 对于单个基因
可以在信息面板中查看这个基因的表达的小提琴图([Seurat::VlnPlot](https://satijalab.org/seurat/reference/vlnplot)), 方便直观的确认这个
基因在各个cluster中的表达情况.


<video controls width="100%">
  <source src="individual_gene_expr.mp4" type="video/webm" />
</video>

