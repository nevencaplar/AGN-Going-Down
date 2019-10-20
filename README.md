# Nonstationarity of AGN variability



This repository contains all of the data and code needed to reproduce conclusion from the paper "Nonstationarity of AGN variability - The only way to go is down!'' which is submitted to ApJL. The main file is `NonStationarity.ipynb` which contains all of the analysis.

## Contents of the repository:

* Folder `Data`: contains all the data needed to reproduce all of results. This includes different AGN catalogs, filter curves and outputs from SQL queries. The only data missing is the catalog of non-variable stars from Stripe 82 - instructions are provided on how to retrieve that data in the notebook.
* Folder `Figures_pdf`: contains all of the figures from the paper and additional figures in pdf format
* Folder `Figures_pdf`: contains all of the figures from the paper and additional figures in png format
* `CatalogCreator_custom.py`: python script to create SQL query for the HSC database
* `NonStationarity.ipynb`: main Jupiter notebook containing all of the routines
* `NonStationarity.py`: module with useful functions for the analysis
* `Nonstationarity_of_AGN_variability__ApJL.pdf`: current version of the manuscript

## Contents of NonStationarity.ipynb:

1. Collecting the data
	1. Finding Ra/Dec coordinate of SDSS QSO
	1. Querying HSC database
	1. Constructing ``fake AGN'' sample (control sample)
	1. Querying HSC database for ``fake AGN''(control sample)
	1. Adding time-separation information
		1. Finding patch information for each AGN
		1. Finding out time difference between observations

2. Analysis of the output from HSC for QSO selected in SDSS
	1. Initial analysis
	1. Median mass, luminosity and. Edd. Ratio
	1. Time difference between observations

3. Analysis of the output from HSC for control sample
4. Analysis of the modeling results
5. Figure 1 from the paper (redshift dependence)
6. Figure 2 from the paper (filter and control sample)
7. Figure 3 from the paper (brightness separation)
8. Figure 4 from the paper (time separation)
9. Figure 5 from the paper (modeling)

## Contents of Data folder:

File used or created in 'NonStationarity.ipynb'. Includes output from queries from catalog, intermediate and final results from the analysis. Find short description below and further description at appropriate places in 'NonStationarity.ipynb' where each of the files is used.

* `194782.csv`: HSC output, query all AGN from SDSS
* `281732.csv`: patch and tract for each AGN observed in HSC
* `281734.csv`: time when each patch and tract was observed in HSC
* `318658.csv`: HSC output, query control sample
* `BrowseTargets.8558.1569111088`: equatorial subsample from Million QSO catalog
* `dmag_HSC_SDSS_AGN_quasar.fits`: filter differences as function of redshift between SDSS and HSC
* `dr7qso.dat`: DR7 AGN catalog
* `matched_array_fake_QSO.npy`: array with control sample, all information from SDSS and HSC
* `matched_array_filtered.npy`: array with AGN, all information from SDSS and HSC
* `matched_array_Stripe82_stars_to_dr7QSO`: Stripe82 stars with similar colors as AGN from DR7
* `position_of_matched_array_Stripe82_stars_to_dr7QSO`: positions (Ra/Dec) of Stripe82 stars with similar colors as AGN from DR7
* `Stripe82stars_likedr7_double_filtered`: Stripe82 stars with similar colors as AGN from DR7, after removing all AGN 
* `time_difference_between_observations_in_g_band_SDSS_mean_HSC.npy`: time separation between observations in SDSS and HSC

In the subfolder Modeling we placed results which are connected with simple modeling effort that is presented in the manuscript.

* Folder `Analysis_results`: summary of light curve behavior for one set of parameters (grid of 2401 parameter choices)
* Folder `Code`: contains code to create summary from pure light curves
* Folder `Individual_LC`: few examples of simulated light curves
* `means_all_LC_redshift_fit.npy` and `means_all_LC_redshift_values.npy`: table which summarizes redshift dependence, as in Figures 1,2,3 and 4, for each choice of modeling parameters

## Contents of Figure folder:

Figures created in `NonStationarity.ipynb`. Find short description below and further description at appropriate places in `NonStationarity.ipynb` where each of the files is created.

* `comaprison_SDSS_HSC_magnitudes`: comparison of SDSS and HSC magnitude for the AGN sample
* `comaprison_stars_AGN_color_color`: comparison of colors for AGN and stars selected to look like AGN
* `comaprison_stars_SDSS_HSC_magnitudes`: comparison of SDSS and HSC magnitude for the control sample
* `coverage_stars_Stripe_82_SDSS_HSC`: positions (Ra/Dec) of the input stars from control sample and position of recovered stars
* `Figure 1-5`: Figures 1,2,3,4 and 5 from the paper
* `mean_time_difference`: histogram of mean time separation between observations
* `median_Edd`: median Eddington ratio for AGN from each brightness bin
* `median_luminosity`: median luminosity for AGN from each brightness bin
* `median_mass`: median mass for AGN from each brightness bin
* `SDSS_HSC_coverage`: positions of the AGN found in SDSS and in HSC 

## Help:

For problems with using the code or installation use GitHub issues page or send us an [email](mailto:ncaplar@princeton.edu).