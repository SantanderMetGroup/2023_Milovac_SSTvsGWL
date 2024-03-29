# 2023_Milovac_SSTvsGWL
This repository provides an updated version of the IPCC-WGI reference regions <sup>[1]</sup>, which incorporates a **refinement of the definition of the oceanic regions** as proposed in the article **'Regional Scaling of Sea Surface Temperature with Global Warming Levels in the CMIP6 Ensemble'** by **Milovac et al**. It also contains materials, including **notebooks**, for the reproducibility of the results presented in the article.

<p>
<img style="margin-left: 5rem" align="right" src="Physical-climate-assessment-reference-regions-v4.1/Fig/Fig_Physical-climate-assessment-reference-regions-v4.1.png" alt="drawing" width="520"\>
</p>


* The [Physical-climate-assessment-reference-regions-v4.1](Physical-climate-assessment-reference-regions-v4.1) folder contains the **shapefile** that incorporates refinements to the oceanic regions originally defined in *IPCC-WGI-reference-regions-v4* <sup>[1]</sup>. It also includes a [GeoJSON](https://github.com/SantanderMetGroup/2023_Milovac_SSTvsGWL/blob/main/Physical-climate-assessment-reference-regions-v5/Physical-climate-assessment-reference-regions-v4.1.geojson) version and the coordinates of the polygon vertices. Both the shapefile and the GeoJSON have a resolution of 0.44 degrees between the coordinates forming the polygons.


* The [conda-environment](conda-environment) folder contains the `environment.yml` file with the recipe of the necessary software for running the reproducibility notebooks available in this repository. To obtain a conda environment named `sst-gwl` run the following:

 	 `conda env create -f environment.yml`

* The [notebooks](notebooks) folder provides the notebooks that were used to obtain necessary results, and then to reproduce the figures given in the article. Six scripts can be found: 
  1. [calculate_global_gwls.ipynb](notebooks/calculate_global_gwls.ipynb) calculates global mean differences of sea surface temperature (SST) and sea air temperature (STAS) with respect to global mean temperature, and GWL for each of the 26 global climate model analyzed.

  2. [calculate_regional_gwls.ipynb](notebooks/calculate_regional_gwls.ipynb) calculates regional mean differences (for IPCC-WGI oceanic reference regions <sup>[1]</sup>  and over ocean biomes) of SST and STAS with respect	to global mean temperature, and GWL for each of the 26 global climate model

  3. [calculate_global_statistics.ipynb](notebooks/calculate_global_statistics.ipynb) calculates slope, p value, standard deviation of the slope, and correlation coefficients for the linear and exponential fit

  4. [calculate_regional_gwls.ipynb](notebooks/calculate_regional_gwls.ipynb) calculates slope, p value, standard deviation of the slope, and correlation coefficients for the linear and exponential fit  of the IPCC-WGI reference regions <sup>[1]</sup> over sea surfaces and sea biomes.

  5. [calculate_spatial_statistics.ipynb](notebooks/calculate_spatial_statistics.ipynb) calculates slope, p value, standard deviation of the slope, and correlation coefficients for the linear and exponential fit per each grid cell for the spatial analysis.

  6. [publication_figures.ipynb](notebooks/publication_figures.ipynb) reproduces all the figure from the article.



* In [data](data) folder small size files are located:
  1. [data/masks](data/masks) contains masking files of land-sea contrast  and those used for different regional analyses at different grid resolutions.
  1. [data/polygons](data/polygons) contains *shapefiles* (*.shp) of the polygons defining (1) the regions used in the Sixth Assessment Report of the IPCC and (2) the world's coastlines. This data was taken from the source repository [https://github.com/IPCC-WG1/Atlas](https://github.com/IPCC-WG1/Atlas).
  2. [data/data_info](data/data_info) contains files with the lists of regional names and models used in both high- and low- resolution analyses.
  3. [data/data_txt.tar.gz](data/data_txt.tar.gz) contains all data necessary to be able to run [publication_figures.ipynb](notebooks/publication_figures.ipynb) and to reproduce the figures from the article. Before running the notebook, it is necessary to decompress the file in the same location after cloning the repository.
 

All the heavier data (i.e. annual and seasonal, global and regional means) necessary to run notebooks 1, 2, and 5, and also output from notebooks 3 and 4 are available on [Zenodo](https://zenodo.org/records/10666947) repository.

**This work is licensed under a Creative Commons Attribution 4.0 International License.**

<sup>[1]</sup> Iturbide, M., Gutiérrez, J. M., Alves, L. M., Bedia, J., Cerezo-Mota, R., Cimadevilla, E., Cofiño, A. S., Di Luca, A., Faria, S. H., Gorodetskaya, I. V., Hauser, M., Herrera, S., Hennessy, K., Hewitt, H. T., Jones, R. G., Krakovska, S., Manzanas, R., Martínez-Castro, D., Narisma, G. T., Nurhati, I. S., Pinto, I., Seneviratne, S. I., van den Hurk, B., and Vera, C. S.: An update of IPCC climate reference regions for subcontinental analysis of climate model data: definition and aggregated datasets, Earth Syst. Sci. Data, 12, 2959–2970, https://doi.org/10.5194/essd-12-2959-2020, 2020.
