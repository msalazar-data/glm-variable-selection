# GLM Variable Selection — Body Fat Modeling

Statistical analysis applying multiple variable selection strategies to identify the best predictors of body fat percentage, using Generalized Linear Models (GLM) with Gaussian and Gamma families.

## What this project does

- Loads and cleans the `fat` dataset (252 men, 14 anthropometric measurements)
- Removes implausible observations using BMI as a filter criterion
- Applies three variable selection approaches under different model families:
  - Best subset selection (BIC criterion)
  - Stepwise backward elimination (BIC)
  - Lasso regularization (cross-validated lambda)
- Compares models with main effects only vs. interactions and quadratic terms
- Evaluates Gaussian (identity link) and Gamma (log link) families
- Selects the optimal model based on BIC, residual deviance, and interpretability

## Techniques used

- Generalized Linear Models (GLM)
- Best subset selection — `bestglm`
- Stepwise selection — `MASS::stepAIC`
- Lasso regularization — `glmnet`
- Cross-validation for lambda tuning
- Residual diagnostics and model comparison

## Stack

R · `faraway` · `glmnet` · `bestglm` · `MASS` · `leaps` · `ggplot2` · `kableExtra` · `broom`

## Dataset

The `fat` dataset is included in the `faraway` R package — no external files needed.

```r
library(faraway)
data(fat)
```

178 observations · 18 variables · Source: Penrose et al. (1985)

## How to run

1. Clone the repository
2. Open `glm-variable-selection.Rmd` in RStudio
3. Install dependencies:
```r
install.packages(c("faraway", "glmnet", "bestglm", "MASS", "leaps", "ggplot2", "kableExtra", "broom"))
```
4. Click **Knit → PDF** (requires TinyTeX: `install.packages("tinytex"); tinytex::install_tinytex()`)

## R environment

```
R version 4.5.3 (2026-03-11)
Platform: x86_64-w64-mingw32/x64 (Windows 10)
```

Key packages: `faraway 1.0.9` · `glmnet 4.1-10` · `bestglm 0.37.3` · `leaps 3.2` · `MASS 7.3-65`

Full session info is included at the end of the compiled document.

## Authors

Dámaso López, Alexis Aminadab · Islas Zicatl, Max Emiliano · Mares Guerra, José de Jesús · Martínez Sánchez, José Ricardo · Ramos López, Gabriela · Salazar Argáez, Miguel Angel

Statistical Methods and Mathematics for Data Science Diploma -- Team 9
