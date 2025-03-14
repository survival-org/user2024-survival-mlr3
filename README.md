
<!-- README.md is generated from README.Rmd. Please edit that file -->

# user2024-survival-mlr3

<!-- badges: start -->

[![](https://img.shields.io/badge/useR!2024-Tutorial-blue?style=flat)](https://sched.co/1c8vg)
<!-- badges: end -->

This introductory tutorial is designed to equip participants with
practical skills and knowledge for performing survival analysis using
machine learning techniques. Survival analysis, a fundamental
statistical method in biomedical and clinical research, focuses on
analyzing time-to-event data, such as the time to disease progression or
patient survival. In this tutorial, attendees will work with clinical
and gene expression data to build, train, and test survival models. They
will learn how to leverage R’s `{mlr3}` ecosystem for efficient model
development, incorporating sophisticated machine learning models such as
penalized linear models and random forests to enhance the accuracy of
the survival predictions. Participants will also explore survival
metrics and model validation techniques to assess the quality and
reliability of their models in the context of real-world data. Whether
you’re new to survival analysis or seeking to enhance your skills, this
workshop offers valuable insights and hands-on experience for tackling
challenging clinical and biomedical questions.

## Learning Goals

- Understand the foundations of Survival Analysis and its applications
  in clinical and high-dimensional research.
- Develop skills in using the `{mlr3}` framework for survival analysis,
  allowing you to build and evaluate predictive models.
- Explore the various survival prediction types and survival metrics to
  assess model performance.
- Work with real-world clinical and gene expression datasets to apply
  machine learning techniques in a research context.

## Requirements for participating:

Bring a laptop with R 4.4.0 installed.  
Install/update the following packages after 1 July to ensure you have
the latest versions:

- `tidyverse` (CRAN)
- `mlr3verse` (CRAN) (incl. `paradox >= 1.0.0`)
- `mlr3viz` (GitHub `mlr-org/mlr3viz`, latest version for new features!)
- `survival` (CRAN)
- `survminer` (CRAN)
- `rpart` (CRAN)
- `mlr3proba` (GitHub `mlr-org/mlr3proba`)
- `mlr3extralearners` (GitHub `mlr-org/mlr3extralearners`)

Install packages for models that we will try:

- `glmnet` (CRAN) (Required)
- `ranger` (CRAN) (Optional)
- `aorsf` (CRAN) (Optional)
- `CoxBoost` (GitHub `binderh/CoxBoost`) (Optional)

Install all packages with `{pak}` (`install.packages("pak")`):

``` r
# CRAN packages first
pak::pak(c("tidyverse", "mlr3verse", "survival", "rpart", "glmnet", "ranger", "aorsf", "survminer", upgrade = TRUE)

# Non-CRAN packages from GitHub
pak::pak(c("mlr-org/mlr3proba", "mlr-org/mlr3extralearners", "mlr-org/mlr3viz"), upgrade = TRUE)
pak::pak("binderh/CoxBoost")
```

Please note that we will have limited time to help with package
installation issues during the workshop.  
We recommend installing the packages in advance to ensure a smooth
experience.

## References

1.  Bischl, B., Sonabend, R., Kotthoff, L., & Lang, M. (Eds.). (2024).
    “Applied Machine Learning Using mlr3 in R”. CRC Press.
    <https://mlr3book.mlr-org.com>
2.  Sonabend, R., Király, F. J., Bender, A., Bischl, B., & Lang, M.
    (2021). mlr3proba: an R package for machine learning in survival
    analysis. Bioinformatics, 37(17), 2789–2791.
    <https://doi.org/10.1093/BIOINFORMATICS/BTAB039>
3.  Zhao, Z., Zobolas, J., Zucknick, M., & Aittokallio, T. (2024).
    Tutorial on survival modeling with applications to omics data.
    Bioinformatics. <https://doi.org/10.1093/BIOINFORMATICS/BTAE132>
    [Tutorial link](https://ocbe-uio.github.io/survomics/survomics.html)
