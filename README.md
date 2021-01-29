# Project: Write a Data Science Blog Post (Stack Overflow 2020 Survey)

## This project is part of the UDACITY Nanodegree Data Science Course. 

## Business Understanding

With this in mind, the aim of this article is to analyze the data of the Stack Overflow 2020 survey (the most recent one available) to search for such differences (or similarities). In this article, I define “developed countries” as the ones that are rated as “very high” by the UN in its Human Development Index (HDI). This rating and its definitions are not exempt from discussion: one could question how to factor in countries that make such list but don’t have a significant high tech economy, the fact that HDI is considered a flawed index by some etc. This discussion, however, goes beyond the scope of this analysis. Here, we will take HDI at face-value and focus on highlighting the issues I considered the most relevant for the coding field and try to formulate explanations about them, based on data.

I'm considering that the developed countries are the ones classified as with very high developed by the UN (http://hdr.undp.org/en/content/human-development-index-hdi).

This is a exploratory project, so I'm not using any inferential statistics. The goal here is to explore some questions presented in the survey to see which characteristics are similar or not in the two groups.

The main questions I want to answer are the following: are there differences between the job market for coders in developed and underdeveloped countries when it comes to salaries, work hours, education, years of coding experience and the coding languages used (as these seem to be the most relevant for describing the field)?


Two things should be consider in the analysis. The number of respondents differ, as one should expect, with more coders living in the developed countries. Also the use of a currency with high value in the market (US$) as a parameter for the salary makes that the salary in the underdeveloped countries is much lower.

## Data Understanding

This data consists in file with .csv format with 61 collumns and 64461 rows. It's a mix of numeric, categorical and nominal. This survey exists since 2011, but I'll only use the 2020 data for is the most recent.

In the repository there is a file with the schema of the survey (survey_results_schema.csv) and also the correspondent PDF file of the survey.

## Prepare Data

The first thing i did is to clean the salary data removing any NANs. Another step i took was dividing the dataframe in two: for the developed and underdeveloped countries.
Further cleanin was done using the function language extractor to make the education data more readable.

##



## Evaluation




The results shows that the salaries in the developed countries are much higher. But if we focus on the distribution of salaries inside the groups (with a boxplot) we can see that it is very similar, and both have a great deal of outliers.

The education levels and the over-time worked hours can be analyzed as a hole. Both suggests a disadvantage in the underdeveloped countries: they work more and have less education levels. Combining these results with the results of the years coding we could draw some possible answers (that are not fully answered here). As the coding field is relatively new in the word and is older and more developed in the rich countries the possible answer for the differences could be that the field is still in a younger state in the underdeveloped countries. This could be the reason that, in comparison with the underdeveloped countries, the underdeveloped ones have professionals that work more, are less formal educated and have less years coding: they are young. This hypotheses is reinforced by the mean of the age as it  is higher in the developed countries. But further research is necessary to accept this.




## The data can be found here:
https://drive.google.com/file/d/1dfGerWeWkcyQ9GX9x20rdSGj7WtEpzBB/view?usp=sharing 


## Libraries used:
Pandas

Seaborn

Matplotlib

Warnings

Numpy
