---
layout: default
title: Cleaning
parent: MultiplexMS
nav_order: 3
---

# MultiplexMS - Demo data instructions
This page is a copy of the demo instructions found in the **MultiplexMS_demo_data** folder. The demo data and instructions can be downloaded [here](https://github.com/liningtonlab/MultiplexMS/releases).

### Step 1. Download the MultiplexMS Companion tool

  1. Using the sample [link](https://github.com/liningtonlab/MultiplexMS/releases) above, download the correct version of the Companion tool for your OS (Win or MacOS). 
  It will be either the *MultiplexMS-Companion-tool_Win.exe* or *MultiplexMS-Companion-tool_MacOS.zip*. 

### Step 2. Open MultiplexMS

  1. Run the MultiplexMS.exe

### Step 3. Preparation Tab

  1. In the MultiplexMS GUI, click on the 'Preparation' tab.

  2. Under 'Path', direct the GUI to the 'demo_sample_list' folder.

  3. Open the 'demo_data_sample_list.csv'.

  4. Under 'File destination', direct the GUI to the 'demo_sample_preparation_grids_and_tables' folder.

  5. Under 'Grid side length r', specify the sample pool size r. **For this exercise, choose 31 as the grid side length**.

  6. Move to the 'Optional Arguments' section of the 'Preparation' tab.

  7. Enable 'Randomize' and write 42 in the 'Seed' field.

  8. Specify an 'Experimental tag' at the end of the exported .csv file. **For this exercise, do not write an experimental tag.**

  9. Select *Start*.

### Step 4. Deconvolution Tab

  1. In the MultiplexMS GUI, click on the 'Deconvolution' tab.

  2. Under 'Folder with initial and rearranged grid(s)', direct the GUI to the 'demo_sample_preparation_grids_and_tables' folder.

  3. Select the 'grids' folder.

  4. Under 'Pooled samples feature table', guide the GUI to the 'demo_sample_MS_data' folder.

  5. Open the 'demo_sample_MS_data.csv'.

  6. Under 'Choose format of feature table', select whether the sample names are in the columns or rows of the MS feature table. **For 'demo_sample_MS_data.csv', select *Samples in columns***.

  7. Under 'File destination' save the deconvoluted MS feature table in the 'demo_deconvoluted_feature_table' folder.

  8. Hit *Start*.

### Step 5. Observe the Deconvoluted Feature Table

  1. In the 'demo_deconvoluted_feature_table' folder, open the 'deconvoluted_feature_table.csv'.

  2. Following the computational deconvolution, some features are not assigned to any sample. These features are retained as '0'.

  3. These MS features can be optionally 'Cleaned'.

### Step 6. Cleaning Tab

  1. In the MultiplexMS GUI, click on the 'Cleaning' tab.

  2. Under 'Deconvoluted feature table', direct the GUI to the newly created 'deconvoluted_feature_table.csv'.

  3. For 'File destination', direct the saved .csv to the same 'demo_deconvoluted_feature_table' folder.

  4. Choose whether the samples are in columns or rows under the 'Choose format of feature table' section. **For 'deconvoluted_feature_table.csv', select *Samples in columns***.

  5. As an optional argument, a 'Critical threshold' can be applied. This will eliminate those MS features that are contained in more than 'Critical threshold' X% of samples.

  6. An experimental tag 'cleaned_' is added to the 'deconvoluted_feature_table.csv'.

  7. Select *Start*.
