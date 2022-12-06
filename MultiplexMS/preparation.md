---
layout: default
title: Preparation
parent: MultiplexMS
nav_order: 1
---

## Preparation of pooled samples tables

### The sample list

The sample list is a simple UTF-8 formatted CSV file (comma-delimited values) or tab-delimited .txt file that contains all the names of the samples that will be analyzed in a multiplexed fashion. If you created a list in Excel, choose <u>File</u> &rarr; <u>Save As</u> &rarr; save as type <u>CSV UTF-8 (Comma delimited) (.csv)</u>.The names will be used to create the tables that indicate how to pool the samples, but will also show up in the deconvoluted feature table. The respective table could look like this:

<img src="assets/sample_list.PNG" style="zoom:67%;" />

No header is needed and the sample names just need to be listed consecutively. Since randomization is an
optional step later on, the order of the list is not necessary of importance. However, if specific knowledge about the similarity of the sample's composition exists, ordering the samples to maximize dissimilarity between potentially mixed samples is encouraged.



### The *Preparation* tab in the companion tool

![](assets/preparation.PNG)

**Path** - Sample list CSV has to be selected

**File destination** - Folder where *grid*s and *preparation_tables* folder are created

**Grid side length *r*** - Side length of the squared grid that is created behind the scenes.
									 Default is 10, resulting in virtual 10 by 10 grid, where 20 pooled samples
                                     are created. Each pooled sample would contain 10 samples.

**Randomize** - The sample list can randomized to create random initial grids. 
					     This step might be helpful to decrease the chance of mixing samples with potential
  					   chemical overlap.

**Seed** - In case randomization is desired, assigning a seed (integer value) allows to reproduce the
             randomization results.

**Experiment tag** - A text that is added to the file name. Special characters ('!@#$%^&*()-+?=,<>) are not allowed.



### The *grids* and *preparation_tables* folders

Two folders are created by the *Preparation* function of the companion tool - the *grids* and the *preparation_table* folders. There is no need to temper with the *grids* folder and especially the files within this folder, since they are used by the *Deconvolution* function later on. However, renaming the folder poses no problem. The files inside the *grids* folder must not be renamed. 

The grids come as a pair of two - an initial and rearranged grid. A typical file looks like this:

![](assets/initial_grid.PNG)

Shown is the initial grid for a randomized series of samples and a grid side length of 10.

The *preparation_tables* folder contains the files with pooled sample layout. It is ordered in the way that each pooled sample is represented by a column, containing X samples (10 in the lower example). The header (eg grid_1_row_1_initial) indicate the pooled sample names. Those names need to be present in the pooled samples feature table later for *Deconvolution* function.

![](assets/preparation_table.PNG)



### Placeholder samples

In case the sample count requires placeholder samples to fill up the virtual square grids, placeholder samples will also show up in the preparation table. We recommend to use the typical solvent (mix) that is used to prepare the samples for the LC-MS run, whenever a placeholder shows up. This shall guarantee that all pooled samples are at the same level of dilution.

