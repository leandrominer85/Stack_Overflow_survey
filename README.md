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
Further cleaning was done using the function language extractor to separate the various languages used and to create a dictionary with their count.

 I'm also dropping the NANs in the Years Coding (both with and without education), as it is less than 1% of the results.

## Top Languages

The top 3 languages are in the exact same order for both groups of countries: JavaScript is the most common, followed by HTML/CSS and SQL comes third. The main differences appear from the 4th most common language and forward. In developed countries, Python appears in such position, but it’s ranked 5th in the underdeveloped ones, whereas Java takes the 4h spot. In developed countries, Java is only the 6th most popular language among coders.

Finally, it’s noticeable that Bash/Shell/PowerShell is the 5th most used language in the developed group, but only appears at the 9th position in underdeveloped countries. This rank is interesting, but the differences between the relative distribution in the developed and underdeveloped countries aren’t that big: the larger is in the one found in Bash/Shell/PowerShell, and it’s only a 3,3% difference.

## Salary

The results show that the salaries in developed countries are much higher than in underdeveloped countries. The average salary is very different: US$ 128243 for the developed countries and US$ 30796 for the underdeveloped. This is expected, as the currency of the underdeveloped countries is less valuable than that of the most developed (since the data is converted to US dollars, as mentioned earlier).

At first glance the distribution is also very different, as the standard deviation shows. And this also seems to be the case in the boxplot (the outliers were removed for better visualization).But if we focus on the distribution of salaries inside the groups (with a boxplot) we can see that it is very similar.

## Education
Data regarding the education data has to be transformed before we can put it in a graph, mainly because the values are long strings.The main difference between developed and underdeveloped countries is found between coders with Bachelor’s degree, that appears with a surplus of over 13% in underdeveloped countries. In developed countries, this is reflected by a larger representation of coders with higher education degrees, in comparison to what’s seen in underdeveloped ones.


# Years Coding

In this part i analysed both the years coding considering the education time and disconsidering the education time. This data is divided into 5 categories. The idea is to somehow to emulate the real-life market division of worker experience. The classes are:
- 0 to 3
- 3 to 5
- 5 to1
- 10 to 20
- above 20 years
For both the years coding with and without education time I’m dropping the NANs values, as it represents less than 1% of the data.

As we can see, there is a large difference between the groups of countries. The underdeveloped ones have younger (in terms of years coding) coders, with the maximum difference seen in the middle category (5–10 years, including education experience), with 13% surplus in comparison with the developed ones. This trend shifts drastically in the two “older” categories, mainly in the last one with a 16% difference in favor of developed countries.
There is a change when we subtract the educational coding experience. The main difference seen in this data is for the younger coders, with an advantage of 13% for underdeveloped countries. But the trend in favor of developed countries having older coders is also present here.
As expected, without education, the years of coding data gets shifted to younger classes. The education seems to have a great impact on the coding experience as the data of the underdeveloped countries shows that with the max of 5 years of experience with education there is 21% of the coders. If we take out the education this group go up to 60% (with 42% in the developed countries for this level of education).

If we look at the average age of the respondents of each group, it is noticeable that the coders in underdeveloped countries are younger than those of the developed ones: 28.89 years old in underdeveloped, against 33.17 years in developed ones.


# Working Hours

The general trend in this shows us that the underdeveloped countries have a larger proportion of their coders working more than the normal, including having the larger difference in the group with more working hours.


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
