# PWC Power BI Virtual Work Experience - Call Centre Trends
![PwC Power BI Virtual Case Experience (1)](https://www.tcn.com/wp-content/uploads/2022/02/Call-Center-Analytics.png)

## Table of Contents :

- [Problem Statement](https://github.com/mshukla94/Call-Trend-Analysis/edit/main/README.md#problem-statement-)
- [Datasource](https://github.com/mshukla94/Call-Trend-Analysis/edit/main/README.md#datasource-)
- [Data Preparation](https://github.com/mshukla94/Call-Trend-Analysis/edit/main/README.md#data-preparation)
- [Data Modelling](https://github.com/mshukla94/Call-Trend-Analysis/edit/main/README.md#data-modeling)
- [Data Analysis (DAX)](https://github.com/mshukla94/Call-Trend-Analysis/edit/main/README.md#data-analysis-dax)
- [Data Visualization Dashboard](https://github.com/mshukla94/Call-Trend-Analysis/edit/main/README.md#data-visualization-dashboard-)
- [Insights](https://github.com/mshukla94/Call-Trend-Analysis/edit/main/README.md#insights-)


## Problem Statement :
In this project Create a dashboard in Power BI for the call center manager that reflects all relevant Key Performance Indicators (KPIs) and metrics in the dataset.

Possible KPIs include (but not limited to):

- Overall customer satisfaction
- Overall calls answered/abandoned
- Calls by time
- Average speed of answer
- Agent’s performance quadrant -> average handle time (talk duration) vs calls answered

## Datasource :

Dataset used for this task was presented by [PwC](https://www.pwc.ch/en/careers-with-pwc/students/virtual-case-experience.html)

Call Centre Trends Dataset: [Call Centre Trends](https://github.com/mshukla94/Call-Trend-Analysis/blob/main/01%20Call-Center-Dataset.xlsx)

## Data Preparation:

Completed the Data transformation in Power Query and the dataset loaded into Microsoft Power BI Desktop for modeling.

Call Centre Trends dataset is given table name:

- `Call Center trends dataset` which has `10 columns and 5000 rows` of observation

Data Cleaning for the dataset was done in the Power Query editor as follows:

- Removed Unnecessary columns
- Removed Unnecessary rows
- Each of the columns in the table were validated to have the correct data type

## Data Modeling:

The dataset was then cleaned and transformed, for it to be ready for data modeling.

- The `Sheet1` tables as show below:

-![Data Structure](https://github.com/mshukla94/Call-Trend-Analysis/blob/main/Dataset%20Structure.JPG)

## Data Analysis (DAX):

Measures used in visualization are defined as below:

- Avg Speed Answer = `CALCULATE(AVERAGE(Sheet1[Speed of answer in seconds]), FILTER(Sheet1, Sheet1[Speed of answer in seconds]>0))`

- Avg Satisfaction = `CALCULATE(AVERAGE('Sheet1'[Satisfaction rating]), 'Sheet1'[Satisfaction rating] IN { 2, 3, 4, 5, 1 })`

- Call Answered = `CALCULATE(COUNT(Sheet1[Answered (Y/N)]), FILTER(Sheet1, Sheet1[Answered (Y/N)]="Y" ))`


## Data Visualization (Dashboard) :

Data visualization for the data analysis (DAX) was done in Microsoft Power BI Desktop:

| Call Centre Trends (Overview) |
| ----------- |
| ![PWC Task - Call Centre Dashboard](https://github.com/mshukla94/Call-Trend-Analysis/blob/main/Call%20Trend%20Analysis%20v2.PNG) |


## Insights :

As shown by Data Visualization, It can be deduced that:

- Most of the satisfaction ratings from each call are 3 and 4.
- The average satisfaction rating has decreased over the span of three months. January brought the highest satisfaction rating and march the lowest.
- The percentage of issue resolved in January was the highest, with a dip in February. It increased again in march.
- The majority of calls come in the morning.
- The average speed of answer by Joe is the highest.
- The call resolution rate of Jim is the highest, even though the average speed of his answers is lower compared to those of Joe, Martha and Dan. The call answered by - him are also higher than the average number of calls answered.
- Becky's speed of answer is the lowest among all, and her rate of calls resolved is higher. She is in the 5th position in the call resolution rate. 
- Martha has the highest  speed of answered in the sec

---
