# Final-Project: The Race for Sub-Saharan Africa
An Investigation into the Drivers of Chinese and American Aid to Sub-Saharan Africa


## Research Questions: (1) What country characteristics (government type, freedom, wealth/poverty) drive US and Chinese Aid? (2) How does Chinese aid to Africa differ from United States Aid by sector? (3) Which countries recieve the most/least aid from each? 
- My hypothesis is that (1) China will give more aid to countries that are more autocratic and have less freedoms, (2) US will give more aid to countries with the greatest need and that are more democratic.
- This research comprised of 5 open-source datasets described below. 

## Data Sources
| Name | Source Identifier | Data | Notes |
|------|------|------|------|
|Polity_IV_Project| Polity IV dataset version 2017 p4v2017 and p4v2017d |[Center for Systemic Peace](http://www.systemicpeace.org/polityproject.html)| [Polity IV Annual Time-Series, 1800-2017](http://www.systemicpeace.org/inscrdata.html)|
|Human_Freedom_Index|Source: Ian Vásquez and Tanja Porčnik, The Human Freedom Index 2018: A Global Measurement of Personal, Civil, and Economic Freedom (Washington: Cato Institute, Fraser Institute, and the Friedrich Naumann Foundation for Freedom, 2018).|[Cato Institute](https://www.cato.org/human-freedom-index-new)|NA|
|The World Bank|Dataset: World Development Indicators: GDP per capita (constant 2010 US$): World Bank, International Program Comparison Database [License](https://datacatalog.worldbank.org/pulbic-licenses#cc-by) |[World Development Indicators](https://databank.worldbank.org/data/source/world-development-indicators/preview/on) [World Bank Terms of Use](http://www.worldbank.org/en/about/legal/terms-of-use-for-datasets)|[Creative Commons Attribution 4.0 International License (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/)|
|AidData_GlobalChineseOfficialFinanceDataset_v1.0| Dreher, A., Fuchs, A., Parks, B.C., Strange, A. M., & Tierney, M. J. (2017). Aid, China, and Growth: Evidence from a New Global Development Finance Dataset. AidData Working Paper #46. Williamsburg, VA: AidData.|[AidData](https://www.aiddata.org/data/chinese-global-official-finance-dataset)|NA|
|OECD   (Note:“This translation was not created by the OECD and should not be considered an official OECD translation. The OECD shall not be liable for any content or error in this translation.”)|OECD (2019), ODA by sector (indicator). doi: 10.1787/a5a1f674-en (Accessed on 08 May 2019)|OECD, 2019,GeoBook: ODA by sector - bilateral commitments by donor and recipient, [OECD URL](https://stats.oecd.org)|[Metadata](https://stats.oecd.org/OECDStat_Metadata/ShowMetadata.ashx?Dataset=DACSECTOR&ShowOnWeb=true&Lang=en)|

## Operationalising Variables
| Concept | Variable Name | Type | Explanation | Source|
|------|------|------|------|------|
|Need| gdp_per_capita| Independent|GDP per capita is gross domestic product divided by midyear population in constant 2010 USD|World Bank national accounts data|
|Freedom|human_freedom_score| Independent| The HFI measures economic freedoms such as: the freedom to trade or to use sound money, the degree to which people are free to enjoy civil liberties—freedom of speech, religion, association, and assembly, indicators on rule of law, crime and violence, freedom of movement, and legal discrimination against same-sex relationships.| Cato Institute|
|Type of Government| polity| Independent|Combined Polity Score: The POLITY score is computed by subtracting the AUTOC score from the DEMOC score; the resulting unified polity scale ranges from +10 (strongly democratic) to -10 (strongly autocratic)| Polity IV Project|
|Aid-China| Total; usd_defl_2014|Dependent|ODA-Like: To qualify as ODA-like, a flow must 1) be official financing, 2) administered with the promotion of the economic development and welfare of developing countries as the main objective (donor intent = development), and 3) be concessional in character with a grant element of at least 25 percent (using a fixed 10 percent rate of discount)|AidData|
|Aid-US|bilat_oda|Dependent|Official development assistance (ODA) is defined by the OECD Development Assistance Committee (DAC) as government aid that promotes and specifically targets the economic development and welfare of developing countries|OECD|

## Data Dictionary
- Please refer to .pdf documents in this repository for variable data dictionaries for both datasets. These documents include the variables that were omitted from the original .csv versions (raw data from Enigma Public) to the clean .xlsx versions used for Python analysis. 
- The Python regression analysis merged both datasets at the 'State' variable level. A count function counted the number of instances a hate group or mass shootings were attributed to each state. No additional variable merger took place. 
- The Plot.ly analysis below used the 'latitude_longitude_appended' variables for both datasets to map instances of mass shootings and hate groups respectively. The mass shooting mapping was amplified in area by the number of victims in each shooting (variable: Total_victims).
