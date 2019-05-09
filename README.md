# Final-Project: The Race for Sub-Saharan Africa
An Investigation into the Drivers of Chinese and American Aid to Sub-Saharan Africa


## Research Question: What country characteristics drive US and Chinese Aid? How does Chinese aid to Africa differ from United States Aid? Which countries recieve the most/least aid from each? 
- This research is limited to two open-sourced datasets - both imported from [Enigma Public](https://public.enigma.com)
- As such, there are many variables that are not analyzed. My goal is not to show if hate groups do or do not lead to mass shootings, but to determine if the instances of mass shootings increase or decrease with the number of hate groups in close proximity (ie. are there clusters of hateful influences in certain areas that have proportionally more mass shootings or not)
- Inferences will be made through a simple linear regression (see Python analysis) and through plot.ly (see chart below)
## Data Sources
| Name | Source Identifier | Data | Notes |
|------|------|------|------|
|Mother Jones - Mass Shootings| b71d85e2-248e-461f-bd97-c10638207f9c|[MotherJones](https://www.motherjones.com/politics/2012/12/mass-shootings-mother-jones-full-data/)| [Data Collection Methodology](https://www.motherjones.com/politics/2012/07/mass-shootings-map/)|
|Southern Poverty Law Center - US Hate Groups|5fe9c57c-68ad-4996-91ab-935debe05412|[SPLC](https://splc.demo.socrata.com/dataset/Confederate-Named-Places/cuzb-ma4p)|NA|
## Data Dictionary
- Please refer to .pdf documents in this repository for variable data dictionaries for both datasets. These documents include the variables that were omitted from the original .csv versions (raw data from Enigma Public) to the clean .xlsx versions used for Python analysis. 
- The Python regression analysis merged both datasets at the 'State' variable level. A count function counted the number of instances a hate group or mass shootings were attributed to each state. No additional variable merger took place. 
- The Plot.ly analysis below used the 'latitude_longitude_appended' variables for both datasets to map instances of mass shootings and hate groups respectively. The mass shooting mapping was amplified in area by the number of victims in each shooting (variable: Total_victims).
