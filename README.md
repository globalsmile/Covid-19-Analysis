# Covid-19 Analysis with Excel

<img align="right" alt="Covid-19 virus" width="1000" height = "400" src="https://raw.githubusercontent.com/keziahuchechi/Covid19-Dataset-Analysis/main/Project%20Pictures/pexels-cdc-3992933.jpg">

---


# Table of Contents

- [Introduction](https://github.com/globalsmile/Covid-19-Analysis#introduction)
- [Problem Statement](https://github.com/globalsmile/Covid-19-Analysis#Problem-Statement)
- [Data Sourcing](https://github.com/globalsmile/Covid-19-Analysis#Data-Sourcing)
- [Data Transformation](https://github.com/globalsmile/Covid-19-Analysis#Data-Transformation)
- [Data Modeling](https://github.com/globalsmile/Covid-19-Analysis#Data-Modeling)
- [Data Visualization](https://github.com/globalsmile/Covid-19-Analysis#Data-Visualization)
- [Data Analysis](https://github.com/globalsmile/Covid-19-Analysis#Data-Analysis)
- [Insights](https://github.com/globalsmile/Covid-19-Analysis#Insights)
- [Shareable link](https://github.com/globalsmile/Covid-19-Analysis#Shareable-Link)


---

# Introduction

The global lockdown was due to the COVID19 Pandemic and since then, a whole lot of things have changed. How bad was the COVID19 prevalence in Africa? 


---

# Problem Statement

The goal of this analysis is to perform an exploratory data analysis on the datset and uncover findings.

---

# Data Sourcing

The Dataset can be found here at [JHU CSSE COVID-19 Data](https://github.com/CSSEGISandData/COVID-19) and available at:


---

# Data Transformation

Data transformation was done in Power Query and the datasets were loaded into Microsoft Excel Power Pivot for modeling.

The covid-19 dataset was imported into power query in three main categories or tables:

- `Confirmed`
- `Death` 
- `Recovered` 

- Each table contains identical columns and rows
- Each table had `936 columns and 199+ rows`

Data Cleaning for the datasets was done in power query as follows:

- The number of columns was removed from the "source" tab to enable refreshing of the data in real time.
- All first rows were promoted to headers
- The data format was changed from wide to long data by unpivoting the date columns
- The new columns were appropriately renamned and their types changed
- Finally, the three tables were merged as one  and named `ConsolidatedData`


The tabulation below shows the `ConsolidatedData` table with it column names and their description:
| Column Name | Description |
| ----------- | ----------- |
| Province/State | Describes the province or state of the observation |
| Country/Region | Describes the province or state of the observation |
| Lat | Describes the latitude of the observation |
| Long | Describes the longitude of the observation |
| Date | Represents the date of the observation |
| Confirmed | Represents the number of confirmed cases |
| Death | Represents the number of death cases |
| Recovered | Represents the number of recovered cases |

To ensure the accuracy of the dates in the `Date` column of  the `ConsolidatedData`  table, a date table was created for referencing using the M-formula:

`{Number.From(List.Min(ConsolidatedData[Date]))..Number.From(List.Max(ConsolidatedData[Date))}`

Here is a breakdown of what the formula does:

For the dataset, we want the start date to reflect the earliest that we have in the data: January 22, 2020 .

`Year`,` Month`,  and `Day` columns were extracted from the date table

The date table was named `Calender`.

---

# Data Modeling

After the dataset was cleaned and transformed, it was ready to be modeled(using Power Pivot).

- The `Calender` table was marked as the official date table in the dataset.
- A one-to-many (*:1) relationship was created between the `ConsolidatedData` and the Calender tables using the date column in each of the tables

---

# Data Visualization

Data visualization for the datasets was done using Microsft Excel:

- The `Dashboard` worksheet: Shows the total number of confirmed cases,  total number of death cases, rate, etc .

Figure 1 shows visualizations from `Dashboard` worksheet

| Figure 1 |
| ----------- |
| ![image](https://media-exp1.licdn.com/dms/image/C4D22AQEHYmGxOgYrzg/feedshare-shrink_1280/0/1655553835254?e=1663200000&v=beta&t=CodhZHZ6Yy26wSaKzaTPHOcQyumbH0E_Rv9rKESNSzk) |

---

# Data Analysis

Measures used in visualization are:

- Total number of confirmed cases = `SUM(ConsolidatedData[Confirmed])`
- Total number of death cases = `SUM(ConsolidatedData[Death])`
- Rate = [Total number of death cases] / [Total number of confirmed cases]


As shown from [Data Visualization](https://github.com/globalsmile/Covid-19-Analysis#Data-Visualization), It can be deducted that from Jan 2020 - June 2022:

- The total number of confirmed cases is over `150 million`
- The total number of confirmed cases is over `2 million`
- The death rate is about `1.76%`

---

# Insights

As shown by [Data Visualization](https://github.com/globalsmile/Covid-19-Analysis#Data-Visualization), It can be deducted that:

- The United States has the highest prevalence of Covid-19
- The North Korea has the lowest prevalence of Covid-19

---

# Shareable Link

You can interact with the report here: 

https://badmus67-my.sharepoint.com/:x:/g/personal/mohammed_badmus67_onmicrosoft_com/EYLsT2Hp54lIky-m1kBSzIYBzoJ5ur600UlshnPetJT8bw?e=AoyVHG
