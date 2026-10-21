# Hypothesis Testing -- Is Job Training Worth It?

## Objective
I tested whether the NSW job training program raised 1978 earnings and judged how big and how reliable the effect is.

## Methodology
- I loaded the LaLonde NSW job training experiment of 445 people, 185 trainees and 260 controls.
- I ran a one-sample t-test and a two-sample Welch's t-test on 1978 earnings.
- I wrote Welch's t-statistic as a function, welch_t(), and checked it against scipy on the full sample and on five subgroups.
- I computed Cohen's d to judge the size of the effect and not only whether it's significant.
- I ran a power analysis for the power of this study and the sample size needed to detect d = 0.3.
- I tested the treatment effect in 5 overlapping demographic subgroups, then applied Bonferroni and Benjamini-Hochberg corrections.

## Key Findings
- Trainees earned \$1,794.34 more in 1978 than controls (Welch's t = 2.6741, p = 0.0079).
- The Cohen's d of 0.2727 is a small effect, so the difference is significant but not large.
- 2 of the 5 subgroup effects were significant before correction and 1 after Bonferroni.
- My welch_t() function matched scipy's t-statistic on the full sample and on all five subgroups.
