# Final-Project: The Race for Sub-Saharan Africa
An Investigation into the Drivers of Chinese and American Aid to Sub-Saharan Africa


## Research Questions: (1) What country characteristics (government type, freedom, wealth/poverty) drive US and Chinese Aid? Secondary questions: How does Chinese aid to Africa differ from United States Aid by sector? (3) Which countries recieve the most/least aid from each? 
- My hypotheses looks to test assumptions about the reasons China and the US commit aid to Sub-Saharan Africa.  (1) Assumption: China gives more aid to countries that are more autocratic and have less freedoms, (2)Assumptio: US gives more aid to countries with the greatest need and that are more democratic.
- This research comprised of 5 open-source datasets described below. 
## Why Should You Care?
China and the US are now in full-blown competition on the global stage. The two superpowers have different visions of Trade, cybersecurity, economic development. Global norms are likely to change based on which country gains the most influence. Sub-Saharan Africa is still highly underdeveloped. However with its large UN voting bloc, abundance of natural resources and a growing young middle class, this region is set to take off. The US has seemingly ignored the continent under the Trump Administration, while China has ramped up its engagement. While aid is only one component of relations between states, it's an interesting idicator of engagement levels and how those have changed over time. Soft Power is still relevant in today's global landscape. 

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

## Source Validation
| Source | Face Validity |Content Validity|
|------|------|------|
|OECD|OECD is an IO with 36 member countries that are "committed to democracy and market economy". It is a statistical agency that publishes comparative stats on global economic indicators|ODA is a uniform measure for OECD countries; the OECD database tracks these and sorts them into subcatagories by working with their Credit Reporting System|
|World Bank|World Bank Open Data has been used widely across various forums for world development indicator tracking and analysis; they are one of the most powerful IOs in the world|GDP per Capita is a commonly used indicator of the country level production. It is not a perfect indicator of need as it does not describe a wealth gap such as the GINI index. However for this analysis it is a good measure for "need" as it helps rank countries by economic power|
|Polity IV Project|The Polity IV Project has been used as a measurement tool for large number of research projects trying to find a continuous measure of autocractic or democratic tendencies over time|The Polity index is not a perfect measure - their manual states it: "should be treated and interpreted with due caution Its primary utility is in investigative research which should be augmented by more detailed analysis".|
|Cato Institute Human Freedom Index|Cato partners with other think tanks to produce the analysis. It's human freedom index has been a reported measure of freedom for four editions|No content validity|
|AidData Chinese ODA|AidData analyses have been used widely in international development research|Additional validation performed by comparing to a reserach paper validation that compared AidData to Malawi reported aid recieved by project|

## Data Management
- My data management plan was created using [dmptool](https://dmptool.org/plans). A PDF Copy is located in the Data Management folder in this Repository. 
- My data managment workflow diagram was created using [Draw.io](https://draw.io/). A PDF Copy is located in the Data Management folder in this Repository. 

## Data Dictionary
- Please refer to .pdf and word documents in this repository for variable data dictionaries for all datasets. There are original .pdf files for variable dictionaries when available from data source as well.  
- Cleaning instructions can be found in the repository under Other Docs. This document is a log of all manual excel modifications made prior to automate Python coding. 
- Automated Python Code is locates as separate files in the repository. They are separated based on task and research question of focus. They are named accordingly. 
- Below Plot.ly Map was created using Plot.ly's web interface. The original data with Geo Coordinates is located in the Raw folder under AidData_oda-like_flows.csv. The cleaned version is located under the Clean folder as Zam_flow_rk_edit.xlsx. The plot is primarily for my own interest and not a materially significant piece of this analysis. 

