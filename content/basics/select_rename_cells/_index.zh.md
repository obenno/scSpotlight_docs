---
tags:
- documentation
title: 选择细胞和注释类型
weight: 20
---

通常的单细胞分析中会基于无监督分群的结果选择有相应marker表达的分群
注释为对应的细胞类型, 如特异表达CD3D的为T cell. 实际应用过程中
无监督分群的结果有时并不完美, 需要手动选择细胞进行注释. scSpotlight允许
用户使用两种方案选择感兴趣的细胞.

## 根据category选择

在右侧边栏的**Category**模块选择细胞分群信息(如`seurat_cluster`)后, 
用户可以从**Rename Cluster**模块的**Select Cells from Category**下拉
菜单中选择相应的细胞分群(如选择1, 2, 对应了`seurat_cluster`中的cluster1和cluster2).
选择后右下脚会出现提示反映所选择的细胞数量. 用户可以在**New Category Name**
中输入需要新增的分组信息名称(如`celltype`), 在**Assign As**中输入所选
细胞对应的细胞类型(如 `T cell`), 那么所选细胞就会在`celltype`分组中被
注释为`T cell`, 其他的细胞注释为`unknown`.

<video controls width="100%">
  <source src="select_cell_from_category.webm" type="video/webm" />
</video>

## 手动选择

用户可以按住<kbd>shift</kbd>键启用套索工具选择感兴趣的细胞, 然后使用和上述一样的
方法注释所选细胞.

<video controls width="100%">
  <source src="https://github.com/obenno/scSpotlight/blob/main/vignettes/articles/images/select_rename_cells.webm?raw=true" type="video/webm" />
</video>
