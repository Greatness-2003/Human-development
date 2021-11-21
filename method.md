#### Introduction

Malaria is a global disease that has plagued the nations of Africa for years. It is a major cause of high mortality rates, child deaths, and plays a key role in economic distress, poverty, and underdevelopment. Nigeria is a malaria endemic country in sub-Saharan Africa that has continuously recorded a high burden of malaria morbidity and mortality, especially in the under-5 group (WHO, 2018). Unlike many other sub-Saharan African countries, which have recorded a significant decline in malaria burden, the number of malaria cases in Nigeria increased with about 500,000 in 2017 (WHO, 2018). Although the mortality rate decreased from about 202 deaths per 1,000 live births to 129 deaths per 1,000 live births between 2003 to 2013 in the under-5 group, statistics show that malaria accounts for approximately 30% of all deaths in this part of the population in Nigeria. Resolution no. 3 of the 2030 Agenda for Sustainable Development Goals (SDGs) adopted by the United Nations (UN, 2018), concerns health, the worldwide improvement of which requires reduction of the malaria burden and its associated mortality as outlined by WHO (2019). Nigeria accounts for more than 25% of the world’s malaria burden, more than any other country, with an estimated 59 million cases and 119,000 malaria attributable deaths in 2013. Almost one in five deaths of Nigerian children under five were due to malaria, and malaria contributed to an estimated 11% of Nigerian maternal mortality. Since 2009, a 10% reduction in incidence has been observed following large, donor funded campaigns to distribute LLINs. In addition, a series of performance-based contracts between the World Bank and the Nigerian Interfaith Action Association (NIFAA) has resulted in increased utilization of programs such as IPTp and LLINs.


### Method 1

#### The study data
In the article, “Spatial Distribution and Sociodemographic Risk Factors of Malaria in Nigerian Children Less Than 5 Years Old”, the writers did research to determine the hotspots where malaria is most prevalent and several risk factors of malaria in Nigerian children. The data was made available from the second and the most recent NMIS (2015) on malaria prevalence among children aged under 5 years in Nigeria. The sample represented each state in Nigeria and the result of the sample included a total of 333 clusters across the country, 138 urban clusters and 195 clusters in rural areas and 25 houses were selected in each of the clusters. All women aged 15-49 years in each household were interviewed and, in addition, all children aged 6-59 months from the selected households were tested for malaria and anemia via blood samples (NMC, 2015).

#### The response variables
In this study, the outcome of interest was based on malaria RDT survey results as a binary indicator of the presence of malaria parasites in the child’s blood sample, where 1 signifies the presence of malaria and 0 the opposite. A total of 6,070 eligible children between ages 6 and 59 months that participated in the 2015 NMI survey were included in the analysis.

   ![img52](https://user-images.githubusercontent.com/68754608/142745673-3bdbaee9-a6d5-40d9-be15-8e8fcc432f6a.jpg)




   ![img6](https://user-images.githubusercontent.com/68754608/142745711-d5afbde3-2a47-4b45-960b-a0d531e8b4f6.jpg)

#### The explanatory variables
The explanatory variables were the selected baseline socioeconomic, demographic, and geographic variables obtained at the household and individual levels from the 2015 NMIS. They included sex, age in months, anemic status, mother’s educational level, age, and sex of the head of the household, type of place of residence, household wealth index, use of mosquito indoor residual spray in the past twelve months, use of Long-Lasting Insecticidal Nets (LLINs) during sleep and number of household members. However, the household wealth index was generated using Principal Component Analysis (PCA) from NMIS. The PCA value is estimated based on household’s ownership of consumer goods, household dwelling characteristics, source of drinking water, sanitation facilities such as type of toilet facilities in the household, material for household construction and other factors related to individual household’s socioeconomic status.


#### Statistical modelling
For the geo-referenced data obtained for this study, a logistic regression model as a special case of the Generalized Linear Mixed Models (GLMMs) that include all variables of interest generated spatially auto-correlated residuals (Moran’s I=0.233, P<0.0001). Here, we employed the GLMM framework to fit the under-5 malaria prevalence data using the logit link function as follows: 

   ![img10](https://user-images.githubusercontent.com/68754608/142742371-ff89a67a-d3fa-4273-81c9-987340824aac.jpg)
   
The predicted values from the model were mapped to obtain risk maps for the under-5 malaria infections at the national level. This was achieved by generating the fitted values of the response variable predicted by the S-GLMM fitted to the data, on which we applied ordinary Kriging to infer values at unobserved locations in the proximity of the data points; hence, a spherical semi-variogram model obtained via the Proc Variogram procedure was found suitable for the Kriging (Cressie, 1992). This approach enabled us to model and map the risk of under-5 malaria to identify critical hotspots of malaria clusters. The spatial analysis was carried out using ArcGIS, version 10.6.1 (ESRI, Redlands, CA, USA) and the statistical analysis was implemented using SAS statistical software, version 9.4 (SAS Institute Inc., Cary, NC, USA). The significance level in our analysis was P=0.05.

![img22](https://user-images.githubusercontent.com/68754608/142742400-fee5b434-556a-4c55-a246-b05d11207cdb.jpg)

A map was built showing the several hotspots where malaria is prevalent. The results indicated that Zamfara, Kebbi, Sokoto, Gombe, Adamawa, and Jigawa have the highest risk of under-5 malaria prevalence. There were followed by another 5 states, which including the 6 are all located in the Northern region of Nigeria. The study showed that South-west states had the lowest risk. 

![img25](https://user-images.githubusercontent.com/68754608/142742420-5124a0f5-3a3c-443f-9d85-f197a08a3cad.jpg)



