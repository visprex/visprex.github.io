# Check correlations between features

**Correlation Matrix** is an useful tool which provides an overview of correlations between features.

Note that categorical features are greyed out.

In the `Correlation Matrix` tab, you can see a `N-by-N` grid of features where `N` is the number of features in your dataset.

- Positive correlation is indicated in warm colours, which approximates red as it approaches 1
- Negative correlation is indicated in cold colours, which approximates purple as it approaches -1
- When there is no strong correlation between two features (around 0), the colour gets closer to white

### Positive Correlations
With the Iris dataset, for example, you can easily see that the `PetalLengthCm` and `SepalLengthCm` features are positively correlated, meaning that the larger the sepal, the larger the petal.

![positive](./images/positive.png)

### Negative Correlations

On the other hand, with the `world-dataset-2023.csv` dataset, you can see that `infant_mortality_rate` and `life_exp_at_birth` has a negative correlation of -0.49, meaning that the higher the infant mortality rate, the lower the life expectancy.

![negative](./images/negative.png)

## Removing colinear features
Correlation matrix can be useful for removing features that are perfectly/extremly highly correlated.

For instance, in the `world-dataset-2023.csv`, there are two measurements called `birth rate` and `fertility rate`, with a correlation of 0.98.
To simply the linear regression model, one can consider dropping one over the other.

![colinear](./images/colinear.png)