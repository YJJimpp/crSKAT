crSKAT: Interval-censored Competing Risks Sequence Kernel Association
Test
================

<!-- README.md is generated from README.Rmd. Please edit that file -->
<!-- badges: start -->
<!-- badges: end -->

The crICSKAT package is designed to implement the crICSKAT
(Interval-Censored Sequence Kernel Association Test accounting for
competing risks) and the interval-censored Burden test while accounting
for competing risks. This package is particularly useful for making
inferences on sets of features in genetic association studies, such as
all SNPs in a gene or pathway.

# Getting Started

    git clone https:

Interval-censored data is a category of failure time data, also known as
time-to-event data, that is frequently encountered in contemporary
genetic datasets such as the UK Biobank (UKB) and St. Jude Lifetime
Cohort Study (SJLIFE). While many individuals are familiar with
right-censored data, which is a type of interval-censored data,
interval-censored data is not precisely known but is only known to fall
within a specific range or interval (such as between 0 and 10, between
15 and 18, or between 30 and infinity).

The follow-up information for individuals in the UK Biobank (UKB) was
gathered using questionnaires and sample assays conducted during visit
assessments, which were subsequently linked to their medical records.
Consequently, providing longitudinal data with time-stamped phenome-wide
diagnosis information presents a challenge. Therefore, for some
diseases, the onset can only be determined to lie within an interval
between two assessments or before the first assessment, rather than
being precisely observed, resulting in interval-censored failure times.

Competing risks occur when an individual may experience multiple events
that could lead to failure, and these events may compete with each other
to cause the failure. This means that the occurrence of one event may
affect or impede the likelihood of another event happening. For
instance, during the study period, some individuals may have passed away
due to other causes, rendering them unable to experience the fracture
event or survive until the end of the study period.

There exist some ad-hoc approaches for handling interval-censored data,
such as converting the occurrence of the event into a binary outcome and
utilizing binary outcome techniques (e.g., logistic regression), or
estimating the occurrence time to fall in the middle of the interval and
using right-censored survival analysis methods. Nevertheless, when
competing outcomes are present, utilizing interval-censored methodology
that accounts for these competing risks frequently results in improved
operating characteristics, such as better control of the Type I error
rate or increased power.

<!-- ## Installation -->
<!-- You can install the development version of crICSKAT from [GitHub](https://github.com/) with: -->
<!-- ``` r -->
<!-- # install.packages("devtools") -->
<!-- devtools::install_github("YJJimpp/crICSKAT") -->
<!-- ``` -->
<!-- ## Example -->
<!-- This is a basic example which shows you how to solve a common problem: -->
<!-- ```{r example} -->
<!-- library(crICSKAT) -->
<!-- ## basic example code -->
<!-- ``` -->
<!-- What is special about using `README.Rmd` instead of just `README.md`? You can include R chunks like so: -->
<!-- ```{r cars} -->
<!-- summary(cars) -->
<!-- ``` -->
<!-- You'll still need to render `README.Rmd` regularly, to keep `README.md` up-to-date. `devtools::build_readme()` is handy for this. You could also use GitHub Actions to re-render `README.Rmd` every time you push. An example workflow can be found here: <https://github.com/r-lib/actions/tree/v1/examples>. -->
<!-- You can also embed plots, for example: -->
<!-- ```{r pressure, echo = FALSE} -->
<!-- plot(pressure) -->
<!-- ``` -->
<!-- In that case, don't forget to commit and push the resulting figure files, so they display on GitHub and CRAN. -->
