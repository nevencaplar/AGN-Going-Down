# Nonstationarity of AGN variability

#### work in progress

This repository contains all of the data and code needed to reproduce conclusion from the paper ``Nonstationarity of AGN variability - The only way is down'' which is to be submitted to ApJL. The main file is ``NonStationarity.ipynb'' which contains all of the analysis.

### Contents:

Folder Data: contains all the data needed to reproduce the result. This included different AGN catalogs, filter curves and outputs from SQL queries.
Folder Figures_pdf: contains all of the figures from the paper and additional figure in pdf format
Folder Figures_pdf: contains all of the figures from the paper and additional figure in png format
CatalogCreator_custom.py: python script to create SQL query for the HSC database
NonStationarity.ipynb: main Jupiter notebook containing all of the routines
NonStationarity.py: module with useful functions for the analysis
Nonstationarity_of_AGN_variability__ApJL.pdf: current version of the manuscript

### Contents of NonStationarity.ipynb:

1. Collecting the data
1.1 Finding Ra/Dec coordinate of SDSS QSO
1.2 Querying HSC database
1.3 Constructing ``fake AGN'' sample
1.4 Querying HSC database for ``fake AGN''
1.5 Adding time-separation information
1.5.1 Finding patch information for each AGN
1.5.2 Finding out time difference between observations

2. Analysis of the output from HSC for QSO selected in SDSS
2.1. Initial analysis
2.2. Median mass, luminosity and. Edd. Ratio
2.3. Time difference between observations

3. Analysis of the output from HSC for fake QSO selected in SDSS
4. Figure 1 from the paper (redshift dependence)
5. Figure 2 from the paper (filter and control sample)
6. Figure 3 from the paper (brightness separation)
7. Figure 4 from the paper (time separation)


## Help:

For problems with using the code or installation use GitHub issues page or send us an [email](mailto:ncaplar@princeton.edu).