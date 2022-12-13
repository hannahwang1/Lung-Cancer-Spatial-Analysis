# Spatial Distribution and Association of the Relative Risk of Lung Cancer Incidence by Census Tracts Between 2013-2017 Across New York State (NYS) with Particulate Matter (PM) 2.5 microns and Adult Smoking Rates at the County Level

This is a cross-sectional analysis of the state-wide population-based dataset from the New York State Cancer Registry (NYSCR), which provides incident lung cancer observed and expected cases aggregated at the census-tract level for the diagnosis years from 2013-2017. The analysis aims to investigate whether clustering is statistically significant or whether it is likely to be a chance occurrence or is simply a reflection of the distribution of the population at risk. In other words, does the observed spatial pattern differ significantly from the null hypothesis of complete spatial randomness?

## Datasets

•	United States Census Bureau "2010 TIGER/Line Shapefiles” from https://www.census.gov/cgi-bin/geo/shapefiles/index.php.

•	2013-2017 NYSCR Cancer Incidence by Census Tract publicly-use dataset provided courtesy of NYS Dept. of Health (NYSDoH) as a SAS datafile.

•	2019 County Health Rankings and Roadmaps for NYS -- https://www.countyhealthrankings.org/app/new-york/2019/downloads -- contains aggregated measures of PM 2.5 and adult smoking rates at the county-level collated from other primary sources of data: 

    •	The original source of the air pollution data is the Environmental Public Health Tracking Network, in which air particulate matter is the average daily density of fine particulate matter in micrograms per cubic meter (PM2.5) from 2014

    •	The original source of % of adults who are current smokers is the individual-level Behavioral Risk Factor Surveillance System survey from 2016

## Lessons Learned

•	Three different local methods of cluster detection were utilized to analyze spatial clustering in diagnoses of lung cancer in NYS to allow for comparison and contrasts of the spatial autocorrelation results across techniques. 

•	Spatial analytical methods were used when studying local clustering to ensure different aspects of spatial patterns are identified and to check whether the results from different analyses are consistent. 

•	Local Moran’s I, Getis-Ord Gi, and Kulldorff’s spatial scan statistics identified the location and extent of statistically significant clusters or spatial patterns of the relative risk of lung cancer incidence over the period of 2013-2017, which defined as the number of cases of cancer observed divided by the population-adjusted and age-adjusted number of cases expected in each census tract. 

•	Autocorrelation statistics for aggregated data provided an estimate of the degree of spatial similarity observed among neighboring values of an attribute over a study area. Expected incidence or cases was the number of people in a given census tract that would be expected to develop cancer within a five-year period if the census tract had the same rate of cancer as the State as a whole. 

•	The cancer rate for the entire state along with the age structure and the number of people in a census tract were used to estimate the expected incidence. 

•	The clusters detected by SaTScan were smaller than those generated from local Moran’s I. SaTScan determines whether there is clustering or not and then gives the location, size of the cluster. LISAs provides a full map with each region colored by how similar its value is to the values of its neighbors. With the second technique, I was able to predict clustering and outliers, but this will also lead to multiple comparisons and inaccurate results. 

•	In terms of choosing an appropriate analysis tool for a certain study, it is not always a right or wrong answer but depends on which model is a good fit to the objectives – whether the research focuses more on central clustering or neighborhood features/outliers. 
