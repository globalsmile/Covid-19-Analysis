# Project NAME: Covid-19-Global Report

---
# Project Objective: 
COVID-19 (The coronavirus disease), a communicable respiratory disease broke in 2019 and has spread to the far ends of the world infecting humans, both young and old. Different countries implemented lockdowns in order to contain the disease and to prevent further spreading while finding medical solution to cure the infected. Over days,months, years and still counting, there are reports of people confirmed to be infected and dead as a result of the outbreak. Accolades to the medical practitioners who have made recovery mostly possible. However, there are data of these reports of cases, deaths and recovery which are available on daily basis. While aspiring to be a data analyst, I have been able to learn to analyse these data- kudos to NG30dayoflearning. This analysis is just to provide an insight into the data provided for different countries.

---
# Data Sourcing:
The data used is being scraped from COVID-19 github data- https://aka.ms/30DLCOVID19GitHubData while the analysis is done with microsoft excel.

---
# Data Transformation:
The data is being loaded from web with its source code copied into Microsoft Excel- in order from confirmed, deaths to recovered cases. It was transformed into Power Query. Changed the query name, edited the source to remove the column load limit in order to enable update. Made first row as column header and select state/province, country/region, long, lat then unpivot other columns. Deleted Attribute, changed data types and renamed columns from value to confirmed. I duplicated the query and then changed the source with deaths and recovery in other to apply the previous changes then renamed their columns to death and recovered. Also renamed the query name as appropriate. On home tab, I merged query as new for confirmed and death by clicking soen on provincce, country and date. Combined recovered and renamed as consolidated data. Removed unwanted columns such as long, lat, province etc. Changed the data type for date and worked on pivot tables and charts. Then created a dashboard.

---
# Findings and Recommendations:

Total number of confirmed cases is  150,795,238,246 
![image](https://user-images.githubusercontent.com/106287208/174332892-7615b400-ff11-44dc-89f2-05954417a6e5.png)
, while the Total Deaths is 6268173

![image](https://user-images.githubusercontent.com/106287208/174332568-b778172b-ca38-428a-bbc7-7b314d45336f.png)


