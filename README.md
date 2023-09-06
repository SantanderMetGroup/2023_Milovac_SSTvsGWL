# 2023_Milovac_SSTvsGWL
This repository contains the notebooks that were used to obtain necessary results, and then to reproduce the figures given in the article  **"Regional scaling of sea surface temperature with global warming levels in the CMIP6 ensemble"**.

In the **notebooks** folder 6 scripts can be found: 
1. [calculate_global_gwls.ipynb](.notebooks/calculate_global_gwls.ipynb) calculates global mean differences of sea surface temperature (SST) and sea air temperature (STAS) with respect to global mean temperature, and GWL for each of the 26 global climate model analyzed.

2. [calculate_regional_gwls.ipynb](.notebooks/calculate_regional_gwls.ipynb) calculates regional mean differences (for IPCC regions <sup>[1]</sup> over sea surfaces and sea biomes) of SST and STAS with respect 	to global mean temperature, and GWL for each of the 26 global climate model

3. [calculate_global_statistics.ipynb](.notebooks/calculate_global_statistics.ipynb) calculates slope, p value, standard deviation of the slope, and correlation coefficients for the linear and exponential fit

4. [calculate_regional_gwls.ipynb](.notebooks/calculate_regional_gwls.ipynb) calculates slope, p value, standard deviation of the slope, and correlation coefficients for the linear and exponential fit  the IPCC regions <sup>[1]</sup> over sea surfaces and sea biomes.

5. [calculate_spatial_statistics.ipynb](.notebooks/calculate_spatial_statistics.ipynb) calculates slope, p value, standard deviation of the slope, and correlation coefficients for the linear and exponential fit per each grid cell for the spatial analysis.

6. [publication_figures.ipynb](.notebooks/publication_figures.ipynb) reproduces all the figure from the article.

To obtain conda environment named `sst-gwl` use enviroment.yml file:

	conda env create -f environment.yml

In **data** folder small size files are located:
1. *data/masks* contains masking files of land-sea contrast  and those used for different regional analyses.
2. *data/data_info* contains files with the lists of regional names and models used in both high- and low- resolution analyses. 

All the heavier data (i.e. annual and seasonal, global and regional means) necessary to run notebooks 1, 2, and 5, and also output from notebooks 3 and 4 are available on Zenodo (link to be provided)

**This work is licensed under a Creative Commons Attribution 4.0 International License.**

<sup>[1]</sup> Iturbide, M., Gutiérrez, J. M., Alves, L. M., Bedia, J., Cerezo-Mota, R., Cimadevilla, E., Cofiño, A. S., Di Luca, A., Faria, S. H., Gorodetskaya, I. V., Hauser, M., Herrera, S., Hennessy, K., Hewitt, H. T., Jones, R. G., Krakovska, S., Manzanas, R., Martínez-Castro, D., Narisma, G. T., Nurhati, I. S., Pinto, I., Seneviratne, S. I., van den Hurk, B., and Vera, C. S.: An update of IPCC climate reference regions for subcontinental analysis of climate model data: definition and aggregated datasets, Earth Syst. Sci. Data, 12, 2959–2970, https://doi.org/10.5194/essd-12-2959-2020, 2020.
