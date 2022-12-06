---
layout: default
title: Cleaning
parent: MultiplexMS
nav_order: 3
---

## Cleaning the deconvoluted feature table

In some cases, the deconvolution may lead to a loss of features. Those features are not present in any sample anymore and only 0s are retained. This situation can cause trouble in following analysis steps, such as [NP Analyst](www.npanalyst.org). 

This tab shall help to remove the features quickly from the table and will produce a pruned deconvoluted feature table file with the prefix *cleaned_*.

In addition, this tab allows to remove features that are present in more than a defined percentage of the samples. Those feature might be considered as noise or too abundant and, therefore, unnecessarily inflate the feature presence table.

![](assets/cleaning.PNG)

### The *Cleaning* tab in the companion tool

**Deconvoluted feature table** - File path to the deconvoluted feature table (.csv).

 **Critical threshold** - [optional] Features that are present in more than x% of the samples (x being the critical threshold) are removed from the dataset.

**File destination** - Folder where the cleaned table should be saved.

**Choose format of feature table** - The format of the deconvoluted feature table has to be determined. Are samples oriented in columns (-> features in rows) or are samples in columns (-> features in columns). If the deconvoluted feature table is untouched samples are stored in columns.

**File destination** - Folder where the deconvoluted feature table shall be saved. Feature table will show all sample names in rows, and features in 								 columns. Only feature presence (1) and absence (0) will be shown. 

