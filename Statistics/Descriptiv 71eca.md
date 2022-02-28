# Descriptive Statistics: Fundamentals

quick prep notes @ranton95

**Contents:**

# Representation of Categorical Variables:

## Frequency distribution tables

![Untitled](Descriptiv%2071eca/Untitled.png)

Has the categories itself and the corresponding variables. Here frequency is the number of units sold.

## Barcharts

![Untitled](Descriptiv%2071eca/Untitled%201.png)

Separates categories and visualizes them

## Pie charts

![Untitled](Descriptiv%2071eca/Untitled%202.png)

Pie charts are visualized after calculating the Relative frequencies. 

**Relative frequency** is the percentage of the total frequency for each category. Naturally, all relative frequencies add up to 100%

## Pareto diagrams

A Pareto diagram is a special type of bar chart, where categories are shown in descending order of frequency. 

![Untitled](Descriptiv%2071eca/Untitled%203.png)

By **frequency**, statisticians mean the number of occurrences of each item. In this case, it is the number of units sold.

**Cumulative frequency** (line on the graph) is the sum of relative frequencies.

![Untitled](Descriptiv%2071eca/Untitled%204.png)

The Pareto Principle (80-20 rule) derives from this. 80% of the effect come from 20% of the causes.

It shows how subtotals change with each additional category and provide us with a better understanding of our data.

# Representation of Numerical Variables:

## Frequency distribution table

As the name implies, distributing the frequencies in desired intervals. Whenever we have to plot data, it is easier to plot once we arrange them in a table. The same approach is done here. When we deal with numerical variables, it makes much more sense to group the data into intervals and then find the corresponding frequencies.

This way we have a summary of the data for which we can create a meaningful visual representation. Generally, statisticians prefer 5-20 intervals, however, it depends. The **desired intervals** can be calculated as follows:

             desired intervals:    $\frac{largest number -smallest number}{number of desired intervals}$

From these intervals, the frequency in each interval is collected into the table. A number is included in the particular interval 

- If that number is **greater** than the lower bound
- is **lower** or **equal** to the upper bound

Following this, we calculate the relative frequencies in each interval.

                     Relative frequencies:    $\frac{Frequency}{Total Frequency}$

![Untitled](Descriptiv%2071eca/Untitled%205.png)

## The Histogram

One of the most common way to represent numerical data.

Unlike the bar chart, in Histograms, both the horizontal and vertical axes are numerical. Each bar has **width** equal to the **interval** from frequency distribution table and **height** equal to the **frequency.** 

![Untitled](Descriptiv%2071eca/Untitled%206.png)

There is no gab between the bars, meaning each interval ends where the next one starts.

In some cases, we plot the Histograms with respect to the **relative frequency** (which is denoted as %) rather than the **absolute frequency**.

## Cross table and scatter plot

**Cross table:** The most common way to represent Categorical Variable. Also known as *contingency tables*.

![Untitled](Descriptiv%2071eca/Untitled%207.png)

The most common way to represent cross table **side-by-side chart**, which is a variation of the bar chart.

![Untitled](Descriptiv%2071eca/Untitled%208.png)

All graphs are very easy to create and read, once you have identified the type of data you are dealing with.

![Untitled](Descriptiv%2071eca/Untitled%209.png)

**Scatter plots** are used when representing two numerical variables. Each point gives us information about a particular students performance. When interpreting a scatterplot, a statistician is not expected to look at a single data point. The main idea here is to extract how the data is distributed.

Scatterplots helps us determine the **Outliers**. These are data points that go against the logic of the whole dataset.

# Measurements of Central Tendency

## Mean

- Population Mean (**µ**) ****
- Sample Mean (**x̄**)

![Untitled](Descriptiv%2071eca/Untitled%2010.png)

The Mean is the most common measure of central tendency. However it has a huge downside as it is **easily affected** when an outlier exists in the dataset.

![Untitled](Descriptiv%2071eca/Untitled%2011.png)

This is where we use Median.

## Median

The median is the middle number in an ordered dataset.

- In order to calculate median, we arrange the dataset first in the ascending order.
- The median is the number at position (n+1)/2 in the ordered list where n is the number of observations

![Untitled](Descriptiv%2071eca/Untitled%2012.png)

![Untitled](Descriptiv%2071eca/Untitled%2013.png)

## Mode

The Mode is the value that occurs the most often. It can be used for both numerical and categorical data.

![Untitled](Descriptiv%2071eca/Untitled%2014.png)

When data point appears only once, there occurs the point where we say there is **no** mode.

# Measurements of Asymmetry

## Skewness

![Untitled](Descriptiv%2071eca/Untitled%2015.png)

Skewness indicates whether the data is concentrated on one side

- mean > median: Positive skew/Right skew (outliers to the right)
- mean = median: mode: No skew asymmetrical
- mean < median: Negative skew/Left skew (outliers to the left)

![Untitled](Descriptiv%2071eca/Untitled%2016.png)

# Measurements of Variability

When we take sample data for measurements the **formulas** applied 

for **population** and **sample** are **different**. For example:

![Untitled](Descriptiv%2071eca/Untitled%2017.png)

In **population data** we are 100% sure of the the measures we are calculating. However for **sample data** it is always an approximation of the population parameter. Hence the formulas are adjusted for both cases.

## Variance

Variance measures the dispersion(spread) of a set of data points around their mean value.

![Untitled](Descriptiv%2071eca/Untitled%2018.png)

Notice for the numerator, the difference indicates the dispersion from the mean and squaring to produce non-negative values.

## Standard Deviation

Standard deviation is the most common measure of variability for a single dataset.

It is simply the **square root** of **variance**:

![Untitled](Descriptiv%2071eca/Untitled%2019.png)

## Coefficient of Variation (CV)

**Coefficient of variation** also known as **Relative standard deviation** is equal to the standard deviation divided by the mean:

![Untitled](Descriptiv%2071eca/Untitled%2020.png)

![Untitled](Descriptiv%2071eca/Untitled%2021.png)

# Measurements of Relation Between Variables

## Covariance

Helpful for between understanding the clear relationship between two variables. Example, Housing prices. Size vs. Price scatter plot.

![Untitled](Descriptiv%2071eca/Untitled%2022.png)

We say that two variables are correlated and the main statistics to measure this correlation is called **covariance.**

Covariance can be **positive** or **negative** or even equal to **zero**.

![Untitled](Descriptiv%2071eca/Untitled%2023.png)

![Untitled](Descriptiv%2071eca/Untitled%2024.png)

## Linear Correlation Coefficient

Correlation adjusts covariance, so that the relationship between the two variables becomes easy and intuitive to interpret.

![Untitled](Descriptiv%2071eca/Untitled%2025.png)

                                    sample             population

                             

                          **-1 ≤ correlation coefficient ≤ 1**

Basically we manipulate the covariance to get a better result. However keep in mind there is a strong relationship between the two variables.

Correlation coeff. = 1 means the entire variability of one variable is explained by the other

Correlation coeff. = 0 : Absolutely independent (prices of coffee in Brazil, to prices of Houses in London)

Correlation coeff. = -1 perfect negative correlation. Think about your crypto trading of altcoin pairs and bitcoin.

## Causality

Important to understand the direction of causal relationships.

**Correlation does not imply causation.**