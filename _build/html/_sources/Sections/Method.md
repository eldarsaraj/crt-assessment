# Methodology

The surveys ask two types of questions. 

First, there are **14 demographic questions**, aiming at getting a clearer picture of the student population, as well as allowing control for some variables of importance (such as high-school GPA, age, socio-economic status ... etc).

Second, there are **11 thinking questions** aiming to assess students' ability to think critically about aspects of reality. For example, students were given a statement and asked to identify the central claim (see Figure 2 for an example).

```{figure} ../Files/sample_question.png
---
height: 350px
name: sample-question
---
Example of a thinking question from the survey.
```

Both the pre- and the post-survey used *exactly* 11 thinking questions with the *exactly same format* (with different questions, naturally) so that the comparison between their answers before and after taking the course could be meaningfully made.

Each question has a single correct answer, and each correct answer earns one point. All questions have the same point weight. The points are added and consist the total number of points per each student.

The score for each of the surveys is calculated by taking the mean. The results are compared and analyzed using Neyman-Pierson two-sided hypothesis test, with the null hypothesis that there are no differences between the scores of the two surveys, and the standard p-value of 0.05. I chose the two-sided test since it is quite possible that the results in the second survey are worse than in the first one.