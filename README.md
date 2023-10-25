# Hydraulic bottom friction and aerodynamic roughness coefficients for mangroves in southwestern Florida, USA
## Journal of Marine Science and Engineering
## 2023

This repository contains the processing codes used in the above-referenced paper. You should clone the conda environment called 'mangrove' prior to running any of the Jupyter Notebooks for point cloud processing. If you have conda installed on your system, use the command:

conda env create -f environment.yml

The point cloud data are too large to be included in the repository so they can be downloaded at:

https://www.dropbox.com/scl/fi/gxl02oz0ea1d96bbt8mdm/mangrove_roughness_raw_pointcloud_data.tar.gz?rlkey=jgbyyzz9fjc7hswdpygab66q1&dl=0

You can extract the point clouds in your local repository but I recommend first adding *.txt and *.gz to your .gitignore file.

The first step is to process the data using PDAL and the pipeline files provided here. After you have installed PDAL (or cloned the conda environment as descirbed above), the command would look like:

pdal pipeline -i pipeline_CKEY_TLS.json
