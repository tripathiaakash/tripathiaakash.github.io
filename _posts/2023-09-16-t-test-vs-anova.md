---
layout: post
title: "t-test vs ANOVA (Analysis of Variance)"
date: 2023-09-16 10:55:40 +0000
category: statistics
---

### Motivation: Why should you bother?

Sometimes we need to compare certain statistics of a parameter of a population. For example, we might need to:

1. compare the mean heights of males vs females in a country, or
2. compare the accuracy of two or more ML classifiers classifying a patient as positive or negative, or
3. compare the mean earnings of people in different age-groups, such as 0-18, 18-25, 25-35, and so on.

In order to do so, we need to collect samples from the population such as measure the heights of a few males and females or build some classifiers and calculate their accuracies for different data samples, or get the earnings of people in different age groups through some survey. Now, when we have the data we can plot the distribution of the sample set and calculate the sample statistic from these samples - mean heights of males and females, mean accuracies of different classifiers, mean earnings of different age groups.

However, just comparing these means will not help make a conclusion because these are sample statistics and not the population statistic i.e. we didn't take everyone belonging to the concerned population while collecting samples. Nevertheless, there are ways by which we can make conclusions about the population just from the sample. These ways or methods belong to the field of Statistical inference. In this blog post, we will go through two such methods: t-test and ANOVA.

### T-test

T-test is a method that helps to conclude if two populations (or more specifically, a parameter of two populations) are statistically different from each other. From above, we can see that t-test can help us make conclusion about the first two examples.

Just like all statistical tests, t-test also follows some assumptions about the samples/data. These assumptions are:

1. Samples are independent from each other i.e. one sample should not affect the value of another sample.
2. Sample distributions must be approximately normal or must have >30 samples per group (in cases of non-normality).

And, just like any statistical test, t-test uses a test statistic to make a conclusion about the difference between two groups. This test statistic is called t value.

### ANOVA - Analysis of variance

ANOVA is a test that helps us make a conclusion if three or more groups of populations have statistically different parameter. For the examples in the Motivation section, we can see that ANOVA can help us in the third example.

Test statistic for ANOVA is F value.