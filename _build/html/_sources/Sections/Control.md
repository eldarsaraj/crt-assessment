# Correlations and control

Let's see first if there's any meaningful correlation between demographic variables and the score. I'll plot it first so we can see it visually, and then I'll calculate correlation for some of them if we see anything interesting.

```{figure} ../Files/Charts/correlation.png
---
height: 600px
name: correlation
---
Scores by each variable.
```

Here we see that a few interesting things. First, it seems that male students had a better score in the post survey than the female ones. Similar difference in improvement is seen in students who work part-time, students with GPA of 3.0, and students who said they were 'fairly motivated' to learn critical thinking. Interestingly, the difference in improvement is the greatest in students whose parents don't have high-school degree.

The chart for age was to big to fit with the other ones, so I reproduce it below:

```{figure} ../Files/Charts/age.png
---
height: 400px
name: age
---
Scores by age.
```

The biggest difference in improvement here can be seen in two age groups, the 19-20 year olds, and 23-24 year olds. I'm not sure how relevant age is here, so I'll try to control for these other variables and run a t-test again.

# T-test with control

Here are the results on the subsample selected on the basis of the criteria of higher correlation:

```{card}

- **Male Students**: t-statistic = -1.79672, p-value = 0.074505
- **Part-time Working Students**: t-statistic = -2.46794, p-value = 0.014987
- **Students with GPA 3.0**: t-statistic = -3.0503, p-value = 0.00314
- **Fairly Motivated Students**: t-statistic = -3.0887, p-value = 0.002409
- **Students whose Parents have No High School Degree**: t-statistic = -3.0871, p-value = 0.00290

```

We see here that, on average, we get a similar result as with the entire sample, but that the positive difference is greatest in some cases: students with high GPA, fairly motivated students, and students whose parents don't have high-school degree. As a reminder, the t-statistic tells us how much the scores from pre and post surveys differ (the negative sign indicates that the pre score is lower).

We might be tempted to conclude that teaching critical thinking to these students might make the most difference (and perhaps that's correct), but I'd caution against rushing to that conclusion since the subsample this t-test was run on was even smaller than our original (already small) sample. Still, it might serve as interesting food for thought.

I'll finish the report by discussing the limitations of this kind of research and proposing a few possible steps in the future.

