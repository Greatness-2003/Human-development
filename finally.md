### Introduction and Central Research Question
Malaria is a global disease that has plagued the nations of Africa for years. It is a major cause of high mortality rates, child deaths, and plays a key role in economic distress, poverty, and underdevelopment. Nigeria is a malaria-endemic country in sub-Saharan Africa that has continuously recorded a high burden of malaria morbidity and mortality, especially in the under-5 group (WHO, 2018). Unlike many other sub-Saharan African countries, which have recorded a significant decline in malaria burden, the number of malaria cases in Nigeria increased by about 500,000 in 2017 (WHO, 2018). Although the mortality rate decreased from about 202 deaths per 1,000 live births to 129 deaths per 1,000 live births between 2003 to 2013 in the under-5 group, statistics show that malaria accounts for approximately 30% of all deaths in this part of the population in Nigeria. Resolution no. 3 of the 2030 Agenda for Sustainable Development Goals (SDGs) adopted by the United Nations (UN, 2018), concerns health, the worldwide improvement of which requires reduction of the malaria burden and its associated mortality as outlined by WHO (2019). Nigeria accounts for more than 25% of the world’s malaria burden, more than any other country, with an estimated 59 million cases and 119,000 malaria attributable deaths in 2013. Almost one in five deaths of Nigerian children under five were due to malaria, and malaria contributed to an estimated 11% of Nigerian maternal mortality. Since 2009, a 10% reduction in incidence has been observed following large, donor-funded campaigns to distribute LLINs. In addition, a series of performance-based contracts between the World Bank and the Nigerian Interfaith Action Association (NIFAA) has resulted in increased utilization of programs such as IPTp and LLINs.
Most of the research regarding malaria is done towards determining the regions in Nigeria where malaria is most prevalent. The question I have is whether maps can also be used to determine how malaria can be alleviated. The main goal of any malaria analysis should be its prevention. And I have noticed so far that research has ignored that essential part and focused instead on identifying it. This is a useful factor since we can’t stop it if we don’t know where it is. 

### Research So Far
In my methods research, I identified two methods, GLMM and Bayesian which were used to determine the areas of Nigeria where malaria is most prevalent. They both made use of logistic regression but of different forms. The GLMM method concluded that malaria is most prevalent in northern Nigeria, while the Bayesian methods which employed only environmental factors decided that the south had more prevalence. I will not make an argument for which I think is right because I believe that in a way, they both are. From looking at the results, I decided that malaria can be broadly classified under two categories: the malaria-endemic and the epidemic-prone regions. I think that this research could be taken further. Malaria manifests in diverse ways in various places. It can be both endemic and epidemic.
My research proposal will take these above methods a step further by identifying endemic and epidemic hotspots in Nigeria. 

### Study Data
I plan to create some sort of fusion between the two methods. This includes taking both environmental and non-environmental variables and fitting them to a logistic regression model and determining which of them fall under endemic and epidemic. 
As usual, data collection is the first step. For the non-environmental variables, I intend to use the data collection method applied in the article, “Spatial Distribution and Sociodemographic Risk Factors of Malaria in Nigerian Children Less Than 5 Years Old”.  The sampling frame for the data is the 2006 National Population and Housing Census (NPHC) of the Federal Republic of Nigeria, of which a total population of 140,431,790 people was recorded (NMC, 2015). A two-stage probability sampling strategy will be implemented for the data collection. At the first stage, 9 cluster Enumeration Areas (EAs) were selected from each stratum (NMC, 2015). The sample represented each state in Nigeria and the result of the sample included a total of 333 clusters across the country, 138 urban clusters and 195 clusters in rural areas. In the second stage, an equal probability sampling was adopted, where 25 houses were selected in each of the clusters. This is what I shall apply in my research. 
Non-environmental explanatory variables will be the selected baseline socioeconomic, demographic, and geographic variables obtained at the household and individual levels from the 2015 NMIS. These include sex, age, anemic status, educational level, age, and sex of the head of the household, type of place of residence, household wealth index, use of mosquito indoor residual spray in the past twelve months, use of Long-Lasting Insecticidal Nets (LLINs) during sleep and number of household members. This information will be collected via interview. However, the household wealth index was generated using Principal Component Analysis (PCA) from NMIS. The PCA value is estimated based on the household’s ownership of consumer goods, household dwelling characteristics, source of drinking water, sanitation facilities such as type of toilet facilities in the household, material for household construction, and other factors related to the individual household’s socioeconomic status.

+ + + + ![img6](https://user-images.githubusercontent.com/68754608/145633463-e273f4ec-0f1e-405a-a2d4-7af836577c67.jpg)
+ + + ***Map of Nigeria showing surveyed locations of under-5 malaria prevalence including the 7,745 households selected from 333 clusters randomly displaced 2 km for urban clusters and 10 km for rural clusters***

Environmental factors such as normalized difference vegetation index (NDVI), the enhanced vegetation index (EVI), the leaf area index (LAI), the amount of rainfall, the land surface temperature for day and night (LSTday and LSTnight), respectively, land use/land-cover (LULC), elevation and distance to the nearest water body, will also be collected as they were done in the article, “Estimating Malaria Burden in Nigeria: A Geostatistical Modelling Approach.” The variables LST, NDVI, EVI, LAI and land-cover were downloaded from the Moderate Resolution Imaging Spectroradiometer (MODIS), from the U.S. Geological Survey (USGS) Land Processes Distributed Active Archive Center (LP DAAC).

![306-Article Text-1244-2-10-20151104_page-0003](https://user-images.githubusercontent.com/68754608/145633248-1d8f2a2f-6c90-47a0-b60d-a98b83ac4967.jpg)
***Sources and resolution of remote sensing data***

### Methodology
I intend to use logistic regression in its simplest form. This logistic regression will be multi-class, multi predictors, with the two classes being endemic and epidemic. Put in predictors and output the labels. Python 3 will be the major platform for this work. Using libraries like pandas, numpy, sklearn to accomplish. I will start with putting all the known predictors (environmental and non-environmental variables), along with the target labels, 0 and 1, representing endemic and epidemic respectively, in a pandas dataframe. After that, I will run a split the data into training and testing data sets using the train_test_split function from sklearn. Then I will fit logistic regression to the X and y train data using *log_reg.fit()* and then predict on the test data using *log_reg.predict()*. I will check the accuracy of my model and if it is not up to par, I will use the KFold cross-validation on the data to build a better model. Using 20 folds, I will use the *KFold()* function on my X and y values. Of course, I intend to do all the above with scaled data using the *StandardScaler* function from sklearn.
I expect that the places with environmental variables like high rainfall and closeness to water bodies will be classified under the endemic, while those with the bulk of the non-environmental variables like poverty, lack of education will fall under epidemic. This conclusion largely helps those working towards the elimination of malaria as different solutions will be administered to the different areas. Personally, I believe that endemic regions require preventative measures which are mainly behavioral changes, such as avoiding storing water in open cans outdoors and clearing of bushes around dwelling places. This will greatly affect the mosquito population as they will no longer be breeding grounds for them, and a reduction of mosquitoes leads to a decline in malaria cases. As for the epidemic regions, measures such as surveillance, indoor spraying of insecticides, widespread use of ITNs would help immensely. 
I hope to test this theory on a select number of places for about 1-2 years. I believe that if my measures are put to place in the right areas, those places will see a significant decrease in malaria. 

### Bottlenecks
I do not expect many issues with the project although some bottlenecks that we may come across are the lack of data in some regions of Nigeria. Borno state, for example, due to the activities of terrorist activities happening there, does not have reliable data of the population as people are scared to venture there. Other issues I expect to encounter are cultural and religious issues. Some groups in the North, for example, believe women should not be counted in a census, nor interviewed. This could warp the data collection process. Other bottlenecks could include poor supply management systems, administrative bureaucracy, poor implementation of policy, and unharmonized coordination and implementation of multiple interventions.

### Budget
I will be using a budget of $100000. The expenses are not overly complicated. All the work can be done on a laptop, aside from the data collection process, which will require little money as there is already enough data from other reliable sources. The chunk of the budget will go towards paying, feeding, transporting, and accommodating the researchers for the 2 years of the research. I intend to allocate $80000 to this. Internet and generator expenses will follow, as there is an unreliable power supply in Nigeria. This will take up about $4000. I also intend to test the results of my research on a small sample of people. This might take 1-2 years to see the effect. LLNS, insecticides, will be bought. This will take up to $3000. After the research is done, I intend to draft a paper on it, and if approved, will publish the paper. I will allocate $2000 to this venture. Lastly, I will pay myself $5000. 

### Limitations and Objections
Some objections I foresee regarding my project include the fact that models may not always be correct, and I could end up wasting money testing a wrong hypothesis. Then again, there is no such thing as a perfect model, and there will always be discrepancies. If I train and test my model sufficiently, it should perform well above average. 
Another limitation I could expect will be the inability to test my research in some places in the North that are under siege from terrorists and as such may be impossible and dangerous to access.


### Discussion
After applying my methodology and applying it in real-time, I intend to build maps of the endemic and epidemic hotspots in Nigeria. These maps will be useful to future health researchers and guide health organizations in their fight against malaria, both in Nigeria and the world at large. The maps will ensure that funds and materials like LLNS are allocated properly and used where they will have the most effects. 
For the epidemic areas, surveillance, indoor spraying of insecticides would help control malaria. In the endemic areas, widespread use of ITNs, behavioral changes, such as avoiding storing water in open cans outdoors and clearing of bushes around dwelling places would help. Planners can also assess the possible health impacts of measures aimed at improving food security through the promotion of large-scale irrigation and wetland management projects. Road construction companies should be requested to fill up construction ponds (burrow pits) once they are no longer needed. 
Finally, the maps constructed will also guide public health researchers in identifying appropriate study environments for intervention trials as well as assist with the identification of populations potentially benefiting from new interventions.
