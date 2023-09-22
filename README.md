# Auto_Regression_Analysis
Data Visualization and Linear Model Regressions to interpret the inference in the Auto dataset.

The R code in this project performs a series of data exploration and regression modeling tasks using the `Auto` dataset. Here's a detailed breakdown of what each section of the code is doing:

1. **Data Exploration and Preprocessing:**
   - The code starts with loading necessary libraries, including `tidyverse` and `ISLR2`, and loads the `Auto` dataset.
   - It then displays a glimpse of the dataset and a summary to get an initial understanding of the data.

2. **Creating Factor Variables for Origin:**
   - The code installs and loads the `ISLR` and `SmartEDA` packages.
   - It loads the `Carseats` dataset from the `ISLR` package.

3. **Exploratory Data Analysis (EDA):**
   - The code performs exploratory data analysis using the `ExpData` function from the `SmartEDA` package.
   - It provides an overview of the data, its structure, and additional statistics like mean, median, and variance.
   - Quantile functions (`quantile_10` and `quantile_90`) are defined and used to calculate quantiles for specific variables.
   - The results of the EDA are stored in `output_e1`.

4. **Graphical Representation of Numerical Features:**
   - Density plots (univariate) are generated for numerical features using the `ExpNumViz` function.
   - The `plot1` variable stores the plots.

5. **Frequency Tables for Categorical Variables:**
   - Frequency tables for all categorical independent variables, such as origin, are created using the `ExpCTable` function.

6. **Bar Plots for Categorical Variables:**
   - Bar plots are generated for categorical variables, including cylinders and origin, using the `ExpCatViz` function.
   - The `plot2` variable stores the plots.

7. **Scatter Plots for Numeric Variables:**
   - Scatter plots between all numeric variables and the target variable `mpg` are created using the `ExpNumViz` function.
   - The `plot3` variable stores the plots.

8. **Box Plots for Numerical Variables vs. Categorical Variable (Bivariate Comparison):**
   - Box plots are generated to compare numerical attributes by each category of origin using the `ExpNumViz` function.
   - The `plot4` variable stores the plots.

9. **Adding Factor Variable for Origin:**
   - A factor variable `origin_fac` is created based on the `origin` variable with custom labels for American, European, and Japanese origins.

10. **Linear Regression Modeling:**
    - A linear regression model (`main_regression`) is fitted with `mpg` as the outcome variable and several predictor variables, including `horsepower`, `displacement`, `acceleration`, `cylinders`, and `origin_fac`.
    - The summary of the regression results is displayed, including coefficients and p-values.

11. **Counting Cars in Each Cylinder Level:**
    - The code counts the number of cars in each cylinder level using the `count` function from the `dplyr` package.

12. **Filtering Out Specific Cylinder Values:**
    - Cars with `cylinders` values of 3 and 5 are filtered out from the dataset.

13. **Residual and QQ Plot Analysis:**
    - Residual and QQ plots are generated for the linear regression model. The code assesses linearity, equal variance, and normality assumptions.
    
14. **Interaction Term Analysis:**
    - The code explores interaction terms between predictor variables, such as log transformations and interactions with categorical variables like `origin_fac`.

15. **Alternative Regression Models:**
    - Additional linear regression models are fitted, considering log transformations for the outcome variable `mpg`.

16. **Model Interpretation:**
    - Detailed model interpretation and coefficient analysis are provided for the different regression models.

17. **Conclusion:**
    - The code offers insights into which model transformations and interaction terms might be appropriate for the dataset and discusses the implications of these choices.

Overall, the code combines data exploration, regression modeling, and interpretation to gain insights into the relationships between various variables and the target variable `mpg`. It also explores potential model improvements through transformations and interactions.
