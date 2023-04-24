# A-B-Testing-Landing-Pages
This project contains an analysis of an A/B test, which is a commonly used method to compare two different versions of a product or service. In this particular case, we are comparing two versions of a page to determine which version leads to more engagement. We will be comparing the conversion rates of two pages.

## Data

The dataset used in this analysis can be found on [Kaggle](https://www.kaggle.com/zhangluyuan/ab-testing). 

- `ab_data.csv`: This file contains information about the two versions of the website and whether a user was assigned to version A or version B.


## Analysis
### Hypothesis

Null Hypothesis: New design landing page does not perform significantly differently than the old one

Alternative Hypothesis: New design landing page performs significantly differently than our old one



### Process
The analysis consists of the following steps:

1. Data Cleaning and Exploration: 
a) The first step is to load the data and clean it up. We explore the data and check for any missing values, duplicates or outliers. Then wrangle the data into a suitable format to conduct the A/B test.

b) Calculate sample size: The precision of our estimated conversion rates is affected by the number of people (or user sessions) we choose to include in each group. We estimate the required sample size using power analysis, which depends on several factors, including the power of the test, the alpha value, and the effect size - how much of a difference we anticipate between the conversion rates.

2. A/B Test Results: Next, we perform the actual A/B test to determine if the results are statistically significant. There are 2 steps to this process.
a) Test normality assumption: 

Wilks test is a way to test if the data has normal distribution or not. According to result of the test it can be decided between Independent Samples t Test and Mann-Whitney U Test. The p-value of the test was less than .05: normality assumptions were violated so we will use the non parametric test: Mann-Whitney U Test

b)Mann-Whitney U Test: used to compare two independent samples to determine whether they have different distributions. It is also known as Wilcoxon Rank-Sum Test. The test works by ranking all observations from both groups and calculating the U statistic, which represents the probability that a randomly chosen observation from one group will be greater than a randomly chosen observation from the other group. 



## Requirements

- Python 3
- Jupyter Notebook
- Pandas
- Numpy
- Matplotlib
- Scipy


