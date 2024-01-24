---
tags:
- documentation
title: Select Cells and Assign Identity
weight: 20
---

`scSpotlight` allows user to select cells of interest either by category (i.e. `group.by`)
or manually via the lasso tool. After select cells, user will be able to assign
new identity to them. 

## Select by category

After choosing "group.by" information from **category** module, all the
identites of the grouping could be selected from a drop-down menu of 
the **Rename Cluster** module. 
For instance, here were illustrated pbmc3k dataset `seurat_clusters` groups, and overall 
expressions of the *GNLY* gene, which is a "Natrual Kill" (NK) cell marker. We found 
cluster 4 cells specifically express *GNLY*, thus could be assigned to NK cells.
User could select cells of cluster 4 and input a new grouping name (e.g. `celltype`)
in **New Category Name**, and assign cell labels "NK" in **Assign As**.

<video controls width="100%">
  <source src="select_cell_from_category.webm" type="video/webm" />
</video>

Unsupervised clustering result is not always perfect, and user may need to
adjust cell annotation manually. One could activate lasso tools by pressing
<kbd>shift</kbd>, then click and drag the mouse to select cells. The video 
below shows how to select cell of interest with lasso tool and assign new celltype labels.

<video controls width="100%">
  <source src="https://github.com/obenno/scSpotlight/blob/main/vignettes/articles/images/select_rename_cells.webm?raw=true" type="video/webm" />
</video>

