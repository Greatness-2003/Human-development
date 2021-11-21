#### Introduction

Malaria is a global disease that has plagued the nations of Africa for years. It is a major cause of high mortality rates, child deaths, and plays a key role in economic distress, poverty, and underdevelopment. Nigeria is a malaria endemic country in sub-Saharan Africa that has continuously recorded a high burden of malaria morbidity and mortality, especially in the under-5 group (WHO, 2018). Unlike many other sub-Saharan African countries, which have recorded a significant decline in malaria burden, the number of malaria cases in Nigeria increased with about 500,000 in 2017 (WHO, 2018). Although the mortality rate decreased from about 202 deaths per 1,000 live births to 129 deaths per 1,000 live births between 2003 to 2013 in the under-5 group, statistics show that malaria accounts for approximately 30% of all deaths in this part of the population in Nigeria. Resolution no. 3 of the 2030 Agenda for Sustainable Development Goals (SDGs) adopted by the United Nations (UN, 2018), concerns health, the worldwide improvement of which requires reduction of the malaria burden and its associated mortality as outlined by WHO (2019). Nigeria accounts for more than 25% of the world’s malaria burden, more than any other country, with an estimated 59 million cases and 119,000 malaria attributable deaths in 2013. Almost one in five deaths of Nigerian children under five were due to malaria, and malaria contributed to an estimated 11% of Nigerian maternal mortality. Since 2009, a 10% reduction in incidence has been observed following large, donor funded campaigns to distribute LLINs. In addition, a series of performance-based contracts between the World Bank and the Nigerian Interfaith Action Association (NIFAA) has resulted in increased utilization of programs such as IPTp and LLINs.


### Method 1

#### The study data
In the article, “Spatial Distribution and Sociodemographic Risk Factors of Malaria in Nigerian Children Less Than 5 Years Old”, the writers did research to determine the hotspots where malaria is most prevalent and several risk factors of malaria in Nigerian children. The data was made available from the second and the most recent NMIS (2015) on malaria prevalence among children aged under 5 years in Nigeria. The sample represented each state in Nigeria and the result of the sample included a total of 333 clusters across the country, 138 urban clusters and 195 clusters in rural areas and 25 houses were selected in each of the clusters. All women aged 15-49 years in each household were interviewed and, in addition, all children aged 6-59 months from the selected households were tested for malaria and anemia via blood samples (NMC, 2015).

#### The response variables
In this study, the outcome of interest was based on malaria RDT survey results as a binary indicator of the presence of malaria parasites in the child’s blood sample, where 1 signifies the presence of malaria and 0 the opposite. A total of 6,070 eligible children between ages 6 and 59 months that participated in the 2015 NMI survey were included in the analysis.

   + + + ![img52](https://user-images.githubusercontent.com/68754608/142745673-3bdbaee9-a6d5-40d9-be15-8e8fcc432f6a.jpg) 
 
 *Map of Nigeria (the study area) based on the 2006 population census, indicating 333 clusters (37 states, including the Federal
Capital Territory (FCT) under the 6 geopolitical regions).*




   + + + ![img6](https://user-images.githubusercontent.com/68754608/142745711-d5afbde3-2a47-4b45-960b-a0d531e8b4f6.jpg)

*Map of Nigeria showing surveyed locations of under-5 malaria prevalence including the 7,745 households selected from 333
clusters randomly displaced 2 km for urban clusters and 10 km for rural clusters for confidentiality reasons.*

#### The explanatory variables
The explanatory variables were the selected baseline socioeconomic, demographic, and geographic variables obtained at the household and individual levels from the 2015 NMIS. They included sex, age in months, anemic status, mother’s educational level, age, and sex of the head of the household, type of place of residence, household wealth index, use of mosquito indoor residual spray in the past twelve months, use of Long-Lasting Insecticidal Nets (LLINs) during sleep and number of household members. However, the household wealth index was generated using Principal Component Analysis (PCA) from NMIS. The PCA value is estimated based on household’s ownership of consumer goods, household dwelling characteristics, source of drinking water, sanitation facilities such as type of toilet facilities in the household, material for household construction and other factors related to individual household’s socioeconomic status.


#### Statistical modelling
For the geo-referenced data obtained for this study, a logistic regression model as a special case of the Generalized Linear Mixed Models (GLMMs) that include all variables of interest generated spatially auto-correlated residuals (Moran’s I=0.233, P<0.0001). Here, we employed the GLMM framework to fit the under-5 malaria prevalence data using the logit link function as follows: 

   + + + + + + + + +  ![img10](https://user-images.githubusercontent.com/68754608/142742371-ff89a67a-d3fa-4273-81c9-987340824aac.jpg)
   
The predicted values from the model were mapped to obtain risk maps for the under-5 malaria infections at the national level. This was achieved by generating the fitted values of the response variable predicted by the S-GLMM fitted to the data, on which we applied ordinary Kriging to infer values at unobserved locations in the proximity of the data points; hence, a spherical semi-variogram model obtained via the Proc Variogram procedure was found suitable for the Kriging (Cressie, 1992). This approach enabled us to model and map the risk of under-5 malaria to identify critical hotspots of malaria clusters. The spatial analysis was carried out using ArcGIS, version 10.6.1 (ESRI, Redlands, CA, USA) and the statistical analysis was implemented using SAS statistical software, version 9.4 (SAS Institute Inc., Cary, NC, USA). The significance level in our analysis was P=0.05.

   + + + + +  ![img22](https://user-images.githubusercontent.com/68754608/142748650-b8407d3d-64cb-48c1-ab3d-863306d34b71.jpg)

*Scatter plot of under-5 malaria prevalence. Blue dots represent negative malaria test outcomes and red dots represent positive
outcomes.*

A map was built showing the several hotspots where malaria is prevalent. The results indicated that Zamfara, Kebbi, Sokoto, Gombe, Adamawa, and Jigawa have the highest risk of under-5 malaria prevalence. There were followed by another 5 states, which including the 6 are all located in the Northern region of Nigeria. The study showed that South-west states had the lowest risk. 

+ + + + + + ![img25](https://user-images.githubusercontent.com/68754608/142742420-5124a0f5-3a3c-443f-9d85-f197a08a3cad.jpg)

*Risk map of under-5 malaria infection as predicted by the spatial generalized linear mixed model for the 6 geopolitical regions of Nigeria. The colorimetric scale represents the number of infected under-5 children per km2.*

### Method 2

#### Malaria prevalence and environmental data
The study in this article “Estimating Malaria Burden in Nigeria: A Geostatistical Modelling Approach.” Geospatial health” was done to determine the prevalence of malaria in Nigerian states based solely on environmental factors such as normalized difference vegetation index (NDVI), the enhanced vegetation index (EVI), the leaf area index (LAI), the amount of rainfall, the land surface temperature for day and night (LSTday and LSTnight), respectively, land use/land-cover (LULC), elevation and distance to the nearest water body.
The fieldwork was carried out from March 1 to June 30, 2007 and was aimed at obtaining unpublished malaria prevalence data from various Nigerian sources. The data collection was done in phases according to Nigeria’s six geopolitical zones. Longitude and latitude co-ordinates were determined for each parasitological survey using the Geonames geographical database. Environmental predictors were extracted from RS sources at spatial and temporal resolutions.

#### Statistical modelling
Logistic regression was fitted to malaria prevalence to identify significant demographic (age) and environmental covariates using STATA v. 9.0. Covariates with a significance level below 0.15 were fitted into Bayesian geostatistical logistic models using WinBUGS v. 1.4. To consider spatial heterogeneity, location-specific random effects were integrated in the logistic models, assuming that they were distributed according to a multivariate normal distribution with variance-covariance matrix parameterizing the correlation structure in the data as an exponential function of distance. Let Ni be the number of children tested at location si, i =1…, n, Yi the number of those found with malaria parasites in a blood sample and Xi = (Xi1, Xi2...,Xip)T the vector of p associated environmental predictors observed at location si. 
For the regression coefficients, a noninformative uniform prior distribution with bounds-∞ and ∞, was adopted. For the spatial parameters σ2, σ2 k, ρ, and ρk we adopted inverse gamma and gamma prior distributions, respectively, with parameters chosen to have means equal to 1 and variances equal to 100. The model was used to predict malaria risk throughout Nigeria. This approach treats the malaria risk at a new location as random and calculates its predictive posterior distribution, which not only provides a single risk estimate, but also gives a whole range of likely values together with their probabilities to be the true values at a specific location. This makes it possible to estimate the prediction error, a substantial advantage over the classical Kriging methods. We estimated the predictive posterior distributions at prediction locations by simulation.

#### Result
The malaria risk maps constructed from the spatial model indicates that malaria varies with a 20% prevalence in some states and 70% in others. The highest prevalence was found in Niger Delta states, Rivers and Bayelsa, and the northeastern and northwestern regions of the country. The north however, had more places with low prevalence.

+ + + + + + ![img20](https://user-images.githubusercontent.com/68754608/142748357-0f11d2a3-d838-4ca1-8211-ed099fc29e1a.jpg)

*Malaria prevalence at the various survey locations in Nigeria.*                     
                     
+ + + + + + ![img21](https://user-images.githubusercontent.com/68754608/142748374-efe9e3b4-15e5-482b-86d2-b27eaa21778a.jpg)

*Median of the malaria prevalence across Nigeria*


### Conclusion
The results of these two articles were widely different with one claiming more prevalence in the north while the other in the south. I believe the reason for this disparity is largely attributed to the fact that the second study used environmental factors only while the first one was broader, incorporating several factors including socioeconomic, geographic factors. Of course, if the basis of the study is things like water bodies, then the south will definitely be at the forefront. This makes the study a bit biased. For this reason, I agree more with the first study, which states that the North has more cases. 
