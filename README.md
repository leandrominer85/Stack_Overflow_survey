# Project Stack Overflow 2020 Survey

## This project is part of the UDACITY Nanodegree Data Science Course. 

## Introduction

The aim is to analyse the data of the Stack Overflow 2020 survey (https://insights.stackoverflow.com/survey) to respond the answer the question: What are the differences between the group of coders that lives in the developed countries and the ones that live in the undeveloped ones.

This data consists in file with .csv format with 61 collumns and 64461 rows. It's a mix of numeric, categorical and nominal. This survey exists since 2011, but I'll only use the 2020 data for is the most recent.

In the repository there is a file with the schema of the survey (survey_results_schema.csv) and also the correspondent PDF file of the survey.

## About the analysis

I'm considering that the developed countries are the ones classifield as with very high developed by the UN (http://hdr.undp.org/en/content/human-development-index-hdi).

This is a exploratory project, so I'm not using any inferential statistics. The goal here is to explore some questions presented in the survey to see wich characteristics are similar or noth in the two groups. For this I'm focusing in these data: salary, work hours, education, years coding and the languages used.

Two things should be consider in the analysis. The number of respondents differ, as one shoud expect, with more coders living in the developed countries. Also the use of a currency with high value in the market (US$) as a parameter for the salary makes that the salary in the undeveloped countries is much lower.

The results shows that the salaries in the developed countries are much higher. But if we focus on the distribution of salaries inside the groups (with a boxplot) we can see that it is very similar, and both have a great deal of outliers.

The education levels and the over-time worked hours can be analysed as a group. Both that suggests a disavantage in the undeveloped countries: they work more and have less education levels. Combining these results with the results of the years coding we could draw some possible answers (that are not fully answered here). As the coding field is relativelly new in the word and is older and more developed in the rich countries the possible answer for the differences could be that the field is developing in the undeveloped countries. This could be the reason that in comparison the undeveloped countries have professionals that work more, are less formal educated and have less years coding: they are young. This hypotheses is reinforced as the mean of the age is higher in the developed countries. But this hypotheses needs further research.




## The data can be found here:
https://drive.google.com/file/d/1dfGerWeWkcyQ9GX9x20rdSGj7WtEpzBB/view?usp=sharing 


## Libraries used:
Pandas

Seaborn

Matplotlib

Warnings

Numpy
