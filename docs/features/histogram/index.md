# Check feature distributions

**Histograms** are useful for visually inspecting feature distributions, and especially to check if it follows a normal (Gaussian) distribution.

Normal distributions provide several useful properties for statistical modelling and is one of the key assumptions of linear regression.

## Selecting a feature

Once you load a dataset in the `Datasets` tab. You can start visualising the distribution of your features by moving on to the `Histogram` tab.
Following from the Datasets tutorial, we use the Iris dataset as an example.

### Numerical features

When you select a `Numerical` feature, values are counted and put into small intervals (bins).

Visually, this means that you can use the X-axis to see where those intervals fall and the Y-axis indicates the count of data points within each bin. For instance, if a bin for values between `1.4` and `1.6` has a count of 26, then there were 26 data points which fall into the range `[1.4, 1.6)`.

This example is for the `PetalLengthCm` feature from the Iris dataset, which measures a flower's petal length in centimeters.

![hist_numerical](images/petal_length.png)

### Categorical features

When you select a `Categorical` feature, value counts are exact and the Y-axis shows how many data points had the exact values shown on the X-axis.

From the Iris dataset, the histogram for the `Species` feature shows how many data points correspond to each species. In this example, you can see that each species is represented equally in this dataset.

![hist_categorical](images/species.png)

## Feature Transformation

### Log transformation methods
Visprex provides two feature transformations out-of-the-box, log10 and and natural log. You can see this in the `f(x)` section below the list of features.

- `x`: Default value. No transformation.
- `log10(x)`: Logarithmic trasformation with base 10.
- `ln(x)`: Logarithmic transformation with base e.

### When is log transformation useful?

Log transformation is useful when the distribution of your selected feature is heavily skewed to either side.

For example, most distributions around money (income, house properties, GDP) tends to have a skewed distribution where a small group of data points show extremely high values.

Choose `world-dataset-2023.csv` from example datasets.

![hist_world](images/world.png)

Click on `Histogram` tab and select the `GDP` feature. We can see that the distribution is heavily skewed to the right where countries with higest GDP values lie on the far right side of the histrogram.

![hist_gdp](images/gdp.png)

Click on `log10(x)` to transform the values to the base 10 logarithmic scale, then you can see that the distribution now closely approximates the normal distribution.

Given that this value is denominated by the US Dollars and the base is 10, you can now read the bins on this histogram as the number of countries that fall into the range between `10^(x)` and `10^(x+d)`, where `d` is the difference between the start of the interval and the end of the interval on the histogram.

![hist_log_gdp](images/log10_gdp.png)


