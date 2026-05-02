# StudentStatsHelper
Final Project
[README.md](https://github.com/user-attachments/files/27306095/README.md)
---
title: "StudentStatsHelper"
output: github_document
---

# StudentStatsHelper

StudentStatsHelper is a beginner-friendly R package made for students learning introductory statistics. The package includes helper functions for descriptive statistics, confidence intervals, hypothesis testing, regression analysis, grade summaries, and simple plots.

## Why this package was created

Many students learn statistics formulas in class but struggle to connect the formula, the R code, and the final interpretation. This package is meant to make common statistics tasks easier to understand by returning clean and simple outputs.

## Installation

After the package is posted on GitHub, it can be installed using:

```{r eval=FALSE}
install.packages("devtools")
devtools::install_github("YOUR-GITHUB-USERNAME/StudentStatsHelper")
```

Then load the package:

```{r eval=FALSE}
library(StudentStatsHelper)
```

## Package functions

This package has six unique functions:

1. `student_summary()` - creates an S3 summary object for numeric data.
2. `ci_mean()` - calculates a t-based confidence interval for a mean.
3. `t_test_helper()` - runs a one-sample t-test and gives a clear decision.
4. `grade_summary()` - converts scores into letter grade categories.
5. `regression_helper()` - runs a simple linear regression and returns important output.
6. `plot_distribution()` - creates a histogram and density plot for a numeric variable.

## Built-in data

The package includes a small fabricated dataset called `student_scores`.

```{r eval=FALSE}
head(student_scores)
```

## Examples

```{r eval=FALSE}
student_summary(student_scores$final_exam)
```

```{r eval=FALSE}
ci_mean(student_scores$final_exam, conf_level = 0.95)
```

```{r eval=FALSE}
t_test_helper(student_scores$final_exam, mu = 80)
```

```{r eval=FALSE}
grade_summary(student_scores$final_exam)
```

```{r eval=FALSE}
regression_helper(student_scores, y = "final_exam", x = "study_hours")
```

```{r eval=FALSE}
plot_distribution(student_scores, "final_exam")
```

## Example Dataset

This package includes a sample dataset called `student_performance.csv`
which contains student-level data such as study hours, exam scores, attendance,
sleep hours, and GPA.

### Example Usage

data <- read.csv("data/student_performance.csv")

student_summary(data)
mean_sd(data$exam_score)
confidence_interval(data$exam_score)

## Metadata

The metadata for this package is stored in the `DESCRIPTION` file. It includes the package title, version, author, description, license, imports, suggested packages, and encoding information.

## License

This package uses an MIT License.

## Classes and methods

This package uses an S3 class called `student_summary`. It also includes a print method called `print.student_summary()`.

## Use of AI

AI was used as a support tool to help plan the package structure, draft documentation, and organize the code. 
