# Results

Here are the basic summary statistics for each survey:

- The mean score of the pre survey is **6.2** and the mean score of the post survey is **6.6902**;
- Standard deviation of the pre survey is **1.595** and of the post survey is **1.658**.

Here's a visual representation:

```{figure} ../Files/Charts/scores_dist.png
---
height: 300px
name: scores-dist
---
Scores distribution chart.
```

The data show that there is some weak improvement in students scores in the second survey, but that difference seems very small, a mere 0.5 points. Still, it could be meaningful.

However, in order to make any such conclusion, we need to run a proper statistical analysis. In this section, I'll conduct a basic hypothesis test and comment on the results. I'll explain the methods and show the formulas, for clarity purposes.

## Hypothesis test

With the null hypothesis being set to $H_0$: *There is no difference between the scores*, and the alternative hypothesis to $H_1$: *There is difference between the scores*, I ran a t-test, which measures if there is significant difference between the means of two sets of data. 

I assumed the data are normally distributed (reasonable assumption for student test data, confirmed somewhat visually too).

I chose the two-sided test one to make it more stringent. One-sided test determines if there's difference between two means *in only one direction* (whether the post survey scores are greater than the post survey), while the two sided one looks for *any difference* (for example, post scores could also be lower than the pre ones).

The t-test is calculated by using the summary statistics (provided above) and the size of each dataset (245 in the case of pre survey and 113 in the case of the post survey).

Te first step is calculating the **standard error (SE)**, which is given by the following formula:

$$ SE = \sqrt{\frac{s_1^2}{n_1} + \frac{s_2^2}{n_2}} $$

Here, $s_1^2$ is the square of the standard deviation of the first dataset (the pre survey), $s_2^2$ is the same for the second dataset (post survey), and $n_1$ and $n_2$ are the sizes of the datasets.

Then, we use the value of the standard error and plug it in the calculation of the **t-statistic**, which is given by this formula:

$$ t = \frac{\bar{X}_1 - \bar{X}_2}{SE} $$

Here, $SE$ is the standard error, $\bar{X}_1$ and $\bar{X}_2$ are the mean score values of both groups. The t-statistic shows how much the two means differ from one another (relative to the variation within the samples). A large absolute value indicates larger difference between the means.  

I got the following results: 

```{card}
- **t-statistic**: -2.668
- **p-value**: 0.0079
```

This shows that there is some small difference between the two means (the negative sign indicates that the score in the pre survey is lower than the score in the post survey). The t-statistics is somewhat 'dimensionless', it is not expressed in any predetermined units, so we cannot say that the difference between the two means is -2.668 (we see above that the difference is close to 0.5), but what we do get from it is a confirmation that there is some *statistically significant* (as indicated by the p-value of 0.0079) difference between the two scores.

```{card}
You can understand p-value as the probability that the difference between student scores in the pre and post survey happened by mere chance.
```

So, we have sound statistical reasons to **reject the null hypothesis and endorse the alternative one**.

Does that mean much?

Well, **yes** and **no** (or not yet, at least). Provided that the surveys were sensitive to the signal enough, we have some evidence that the student critcal thinking abilities are better after a full-semester course in critical thinking. However weak, the signal says that something is making a dent.

However, the signal *is* weak, no doubt. To determine just how weak, I used a statistic called **Cohen's d**, given by this formula:

$$ d = \frac{\bar{X}_1 - \bar{X}_2}{s_p} $$

Here, ${s_p}$ is the pooled standard deviation (weighted average of the two surveys). Cohen's d quantifies the difference between the two means in terms of standard deviations. So, it provides good indication of the magnitude of this difference.

I got a result of:

- **Cohen's d**: 0.301

This value could range anywhere from negative to positive infinity (it's not to be interpreted in the same way as correlation, between -1 and 1) and shows us the amount of effect in either direction; the bigger the absolute value of the number, the bigger the effect. If it's close to 0, it means very little or no effect. 

The meager value of 0.301 tells us that this effect is not very large, it is smaller than one third of one standard deviation.

We can see it visually if we plot the density of the scores:

```{figure} ../Files/Charts/scores_dens.png
---
height: 300px
name: scores-density
---
Density chart.
```

So, there you have it: the results show weak improvement. 

There are a few other things we can do with the data. I'm curious to see if any of the demographic variables correlate with the results. 

I'll try out a few visualizations in the next section so we see that.

