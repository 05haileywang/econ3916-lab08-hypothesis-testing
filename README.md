# econ3916-lab08-hypothesis-testing

# Hypothesis Testing: Is Job Training Worth It?

## Objective

The objective of this lab was to determine whether participation in a job training program led to higher earnings. I used the LaLonde National Supported Work (NSW) dataset to compare earnings between participants who received job training and those who did not, while examining statistical significance, effect size, and statistical power.

## Methodology

- Loaded the LaLonde NSW dataset, which included 445 individuals, with 185 in the treatment group and 260 in the control group.
- Calculated summary statistics and visualized the distribution of 1978 earnings for both groups.
- Conducted a one-sample t-test and a two-sample Welch's t-test to evaluate differences in average earnings.
- Wrote a `welch_t()` function to manually calculate Welch's t-statistic and verified the results against scipy for the full sample and five demographic subgroups.
- Calculated Cohen's d to measure the size of the treatment effect.
- Conducted a power analysis to evaluate the study's ability to detect an effect and estimate the sample size needed for future studies.
- Tested treatment effects across five demographic subgroups and applied Bonferroni and Benjamini-Hochberg corrections for multiple hypothesis testing.
- Simulated p-value distributions under the null and alternative hypotheses to examine false positives and statistical power.

## Key Findings

The treatment group had average earnings of $6,349.14 in 1978, compared to $4,554.80 for the control group. This represented an average earnings difference of **$1,794.34**.

The two-sample Welch's t-test produced a t-statistic of **2.6741** and a p-value of **0.0079**. Since the p-value was below 0.05, I rejected the null hypothesis and concluded that there was a statistically significant difference in average earnings between the treatment and control groups.

However, Cohen's d was **0.2727**, indicating a relatively small effect size. This suggests that while the program increased earnings on average, the magnitude of the difference was relatively small compared to the variation in earnings.

The power analysis found that the study had **80.8% statistical power** at the observed effect size. To detect an effect size of d = 0.3 with 80% power, approximately 175 participants per group would be needed.

Of the five demographic subgroups tested, **two showed statistically significant treatment effects** before correcting for multiple comparisons. After applying the Bonferroni and Benjamini-Hochberg corrections, only **one subgroup remained statistically significant**.

Finally, the replication crisis simulation found that 34 studies with no real effect and 39 studies with a real effect produced statistically significant results. As a result, **46.6% of significant findings were false positives** in the simulation.

## Conclusion

Overall, this lab showed me why statistical significance alone is not enough to determine whether a program is effective. Although the job training program was associated with significantly higher earnings, the relatively small effect size suggests that the practical impact may be limited. The subgroup analysis also demonstrated how multiple hypothesis testing can lead to misleading conclusions if corrections are not applied. I learned that evaluating statistical power, effect size, and the risk of false positives is important when interpreting research results and making policy decisions.
