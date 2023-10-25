# Hydraulic bottom friction and aerodynamic roughness coefficients for mangroves in southwestern Florida, USA
## Journal of Marine Science and Engineering
## 2023

This repository contains the processing codes used in the above-referenced paper. You should clone the conda environment called 'mangrove' prior to running any of the Jupyter Notebooks for point cloud processing. If you have conda installed on your system, use the command:

```bash
conda env create -f environment.yml
```

The point cloud data are too large to be included in the repository so they can be downloaded at:

<https://www.dropbox.com/scl/fi/gxl02oz0ea1d96bbt8mdm/mangrove_roughness_raw_pointcloud_data.tar.gz?rlkey=jgbyyzz9fjc7hswdpygab66q1&dl=0>

You can extract the point clouds in your local repository but I recommend first adding *.txt and *.gz to your .gitignore file.

The first step is to process the data using PDAL and the pipeline files provided here. After you have installed PDAL (or cloned the conda environment as descirbed above), the command would look like:

```bash
pdal pipeline -i pipeline_CKEY_TLS.json
```

If you would like to skip these steps and get access to the processed point clouds used for analysis in the paper, you can download them at:

<https://www.dropbox.com/scl/fi/pe7f4p8v2ie74kg1s7r05/mangrove_roughness_processed_pointcloud_data.tar.gz?rlkey=cdu0h59wbvneuvh5zdysqyzsg&dl=0>

Then, you can run the Jupyter Notebooks to calculate z0 from the processed point clouds (the ones ending in .xyzch):
- z0_from_TLS-CKEY_max.ipynb
- z0_from_TLS-IEPK_max.ipynb
- z0_from_TLS-PKEY_max.ipynb

The Leave-One-Out Cross-Validation procedure for training the random forest with and without the mangrove sites is in Mangrove_LOOCV.ipynb.

Lastly, the notebook used to plot the point cloud figures is z0_Figures.ipynb.
