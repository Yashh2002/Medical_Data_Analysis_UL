# Medical_Data_Analysis_UL
1. Introduction
Much has been discussed about the risk factors that can aggravate COVID-19 conditions and increase its mortality. 
These include age, sex, weight, and other diseases such as diabetes or kidney failure. While weight is widely 
related to diet, we applied clustering techniques to divide countries according to their diet and compared them 
with the average mortality rate per group, to discover whether there are food categories that affect COVID-19 
mortality, either reducing or increasing it.
2. Research Question
Does diet affect COVID-19 mortality?
Which foods are associated with higher mortality and which with lower COVID-19 mortality?
3. Methodology
3.1. Search for Medical Databases
We accessed Kaggle and selected the Food Supply kcal Data table from the COVID-19 Healthy Diet Dataset.
The motivation of this dataset is to protect health through a healthy diet. With it, it is possible to collect 
information on dietary patterns of countries with lower COVID-19 infection rates.
The chosen table contains the percentage of energy consumption in kilocalories from 23 different food groups 
in 170 countries. The last columns include counts of obesity, malnutrition, and COVID-19 cases as percentages 
of the total population for comparison purposes.
The caloric intake data comes from the Food and Agriculture Organization of the United Nations, and some included 
food groups are alcohol, sweeteners, spices, fish, and plant-based products.
3.2. Pattern Search with Clustering Models
For the development of this project, three different clustering methods were used: K-Means, Mini Batch K-Means, 
and Birch, along with four methods to find the optimal number of clusters: elbow method, Silhouette coefficient, 
Calinski-Harabasz index, and Davies-Bouldin index.
4. Results
4.1. K-Means:
By comparing methods for selecting the number of groups, we found that the optimal number of groups is between 
3 and 4. We decided to use k=4.
Considering the group with the highest average COVID-19 mortality rates as the group with the least healthy diet, 
and the group with the lowest average COVID-19 mortality rates as the group with the healthiest diet, the least 
healthy diet is one where caloric intake includes more alcoholic beverages, nuts, stimulants, and animal products 
including milk, meat, fish, seafood, offal, animal fats, and also more vegetable oils, despite consuming fewer 
plant-based products including cereals, legumes, spices, and starchy roots.
On the other hand, the caloric intake of the group with the healthiest diet has fewer animal products such as milk 
and meat, less alcohol, and more plant-based products such as cereals, legumes, spices, and especially starchy roots. 
Some countries within the group with the worst diet are Albania, Antigua and Barbuda, and Argentina. Examples within 
the healthiest diet group are Angola, Benin, and Cameroon.
4.2. Mini Batch K-Means
When comparing the different methods for selecting the optimal number of groups, it was between 2 and 4. Since 
4 groups appeared more often, we chose 4.
This clustering showed very similar results to the previous one. For example, there is a group for developed countries 
with high obesity, high caloric alcohol consumption, and high COVID-19 deaths (such as the United States), and another 
group for developing countries (much of Latin America) whose caloric intake highlights aquatic products, sweeteners, 
and spices. However, the most underdeveloped countries (African and Asian) were grouped differently, and this time one 
of those groups appeared to have fewer deaths.
4.3. Birch
The optimal number of groups was found to be between 2 and 5. We considered 5 as the best. It should be noted that 
with this method, the elbow method could not be used, so the comparison to obtain the optimal number of groups was 
done with 3 models.
This method showed that the healthiest group has a COVID-19 death rate of .004% while the least healthy group has 
a COVID-19 death rate of .069%. It can be seen that the less healthy groups (0,2) are very similar, but unlike 
the previous models, this one with 5 groups created a new partition of underdeveloped countries.
5. Conclusions
Through the analysis carried out after applying different clustering techniques, we can conclude that diet does 
affect COVID-19 mortality.
In general, those countries that consume more alcohol and animal products (such as meat and milk) and fewer 
plant-based products (such as cereals, legumes, and in some cases fruits) report higher COVID-19 mortality rates, 
while the countries that report lower COVID-19 mortality rates show the opposite. From the above, it can be 
concluded that a healthy diet against COVID-19 is low in alcohol and animal products and high in plant-based products.
Clustering methods could provide other (even more complete) results if the calories consumed were included instead 
of proportions.
