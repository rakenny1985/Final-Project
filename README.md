# Final-Project: The Race for Sub-Saharan Africa
An Investigation into the Drivers of Chinese and American Aid to Sub-Saharan Africa


## Research Question: What country characteristics drive US and Chinese Aid? How does Chinese aid to Africa differ from United States Aid? Which countries recieve the most/least aid from each? 
- This research is limited to two open-sourced datasets - both imported from [Enigma Public](https://public.enigma.com)
## Operationalising Variables
| Concept | Variable Name | Type | Explanation | Source|
|------|------|------|------|------|
|Wealthy vs Poor Country| gdp_per_capita| Independent|GDP per capita is gross domestic product divided by midyear population in constant 2010 USD|World Bank national accounts data|
|Freedom|human_freedom_score| Independent| The HFI measures economic freedoms such as: the freedom to trade or to use sound money, the degree to which people are free to enjoy civil liberties—freedom of speech, religion, association, and assembly, indicators on rule of law, crime and violence, freedom of movement, and legal discrimination against same-sex relationships.| Cato Institute|
|Type of Government| polity| Independent|Combined Polity Score: The POLITY score is computed by subtracting the AUTOC score from the DEMOC score; the resulting unified polity scale ranges from +10 (strongly democratic) to -10 (strongly autocratic)| Polity IV Project|
## Data Sources
| Name | Source Identifier | Data | Notes |
|------|------|------|------|
|Mother Jones - Mass Shootings| b71d85e2-248e-461f-bd97-c10638207f9c|[MotherJones](https://www.motherjones.com/politics/2012/12/mass-shootings-mother-jones-full-data/)| [Data Collection Methodology](https://www.motherjones.com/politics/2012/07/mass-shootings-map/)|
|Southern Poverty Law Center - US Hate Groups|5fe9c57c-68ad-4996-91ab-935debe05412|[SPLC](https://splc.demo.socrata.com/dataset/Confederate-Named-Places/cuzb-ma4p)|NA|
## Data Dictionary
- Please refer to .pdf documents in this repository for variable data dictionaries for both datasets. These documents include the variables that were omitted from the original .csv versions (raw data from Enigma Public) to the clean .xlsx versions used for Python analysis. 
- The Python regression analysis merged both datasets at the 'State' variable level. A count function counted the number of instances a hate group or mass shootings were attributed to each state. No additional variable merger took place. 
- The Plot.ly analysis below used the 'latitude_longitude_appended' variables for both datasets to map instances of mass shootings and hate groups respectively. The mass shooting mapping was amplified in area by the number of victims in each shooting (variable: Total_victims).
