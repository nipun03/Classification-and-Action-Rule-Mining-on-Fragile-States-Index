# Classification and Action Rule Mining on Fragile States Index
In this research project, we are performing experiments on the world ranking, with an aim to understand the impacts of various indicators on the reputation of a state. We also aim for understanding the actions on various indicators and how they affect the reputation as a whole.
The data is taken from Fragile States Index and it is fed to various classifiers and action rule miners. The results of classification and generated action rules are discussed at the end of the report
### Tools used:
The experiments in this project are done using following two tools: WEKA and Lisp Miner.
### Project Phases:
#### Data Selection:
The data selected for this experiment is from Fragile States Index (FSI) and Social Progress Index dataset (SPI).
The attributes of selected data are as follows: <br>
1. Country: Name of the country<br>
2. Year: Year of the data<br>
3. Rank: Rank of the country based on the “Total” attribute. The country with lowest total is ranked 1st. <br>
4. Total: Total of all indicators. The indicators are in the range 0 – 10. <br>
5. C1: Security Apparatus: The Security Apparatus indicator score is assigned by considering security threats to the country. The threats include terrorism, attacks, rebel movements, mutinies, etc.<br>
6. C2: Factionalized Elites: The Factionalized Elites indicator score is assigned by considering the fragments of a country like religion, ethnicity, class, clan, etc. It measures the political transition, struggle and competition.<br>
7. C3: Group Grievance: The Group Grievance considers political and social division among various groups of the society. This indicator scores a country based on the access to various services and resources to these group.<br>
8. E1: Economy: This indicator consider the economic decline for the state. It considers factors such as per-capita income, Gross National Product, Inflation, Productivity, Unemployment Rate, debt, business failures etc. <br>
9. E2: Economic Inequality: The economic inequality indicator scores a country on the basis of its economic inequality across various dimensions. For example, identity groups (race, religion, ethnicity), economic status, education, region etc.<br>
10. E3: Human Flight and Brain Drain: This considers the impact of human displacement on the economy of the country and country’s development. This may involve emigration of workers, labors or other middle working class people.<br>
11. P1: State Legitimacy: This indicator measures a country’s performance on the basis of representativeness and openness of the governing bodies and its relationship with the citizens. The indicators looks at the level of confidence among the citizens, processes and state institutions. <br>
12. P2: Public Services: The public services indicator scores the basic state functions for serving people. This includes but is not limited to, provision of essential services such as transport, electricity, education, health, water and sanitization.<br>
13. P3: Human Rights: This indicator ranks on the basis of observation of fundamental human rights of the people. It looks at the abuse of legal social rights or people groups and institutions.<br>
14. S1: Demographic Pressures: This indicator measures the pressures on the population related to access for various services like health, food supply, safe-water and other life sustaining resources.<br>
15. S2: Refugees and IDPs: It measure the pressure on a state by displacement of large communities due to political, environmental or social reasons. It also considers the refugee inflow.<br>
16. X1: External Intervention: It considers the impact of external entities in the functioning of the state’s governance.<br>
One of the chief task in our experiment is to devise ways to improve the accuracy of our classification and action rule model. For this purpose, the FSI dataset is augmented with additional attributes. The augmented dataset is taken from “Social Progress Index”[4], which is an aggregation of social and environmental indicators for the countries of the world. The data span across three dimensions: Human Needs, Wellbeing and Opportunities.<br>
The attributes that were selected for augmentation are as follows:<br>
**1. Personal Safety:** The dimensions evaluated by Personal Safety are: Homicide Rate, Level of Crime, Traffic Death, Criminality and Political Terror. <br>
**2. Environmental Quality:** The Environmental Quality attribute measures state index based on factors like emission of greenhouse gases, biodiversity and habitat, wastewater treatment and outdoor air pollution.<br>
**3. Tolerance and Inclusion: This attribute include ranks for tolerance of immigrants, homosexuals, discrimination against minorities and community safety.<br>
**4. Press Freedom Index:** This indicator is an evaluation of freedom of expression in private discussion, academia or culture related backgrounds.<br>
**5. Tolerance for immigrants:** It is based on a survey asking individuals whether the area in which they live is safe for immigrants or not.<br>
**6. Discrimination and violence against minorities:** It is an indicator representing group grievances and violence on the grounds of culture, religion and community.
#### Data Assignment:
In the dataset, the decision attribute is “Total”, which only contains continuous numerical values. However, the algorithms for classification and action rules generation require nominal values for the decision. Therefore, as the foremost pre-processing steps, we have classified the “Total” using percentile ranks.
#### Classification of Dataset:
This is doen on Weka using the following classifiers:
-Naive Bayes Classifier
-Bayesnet Classifier
-Hoeffding Tree Classifier
#### Action Rule Mining
Action Rules have been generated using Lisp Miner.

#### Please refer to the report for further reference.
