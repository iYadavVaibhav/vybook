# Basic Statistics
Basics of statistics for Data Science.

**Central tendency** measures tell us how values are grouped around the centre value.

**Variation** tells us how disperse the data is or how much it is scattered

**Shape** tells us the pattern of distribution of values. How the data is distributed in a frequency.

Two type:
- Descriptive
- Inferential

## Summarizing Quantitative Data
Mean median and mode are three ways to summarize the data and to measure the central tendency of data. These are usually calculated for quantitative data. 

**Mean**

Average or mean are one and the same thing. It is sum of all the data points divided by number of data points. 

$$ 𝜇 = \frac{ \sum_{i=0}^n x_i }{ n } $$

It gets affected by the outliers .

**Median**

It is the middle number in an ordered list. 

If it's even then it is sum of two middle number divided by 2, else it's the middle one. 

if $n = even$ then: $(a+b)/2$ where a and b are middle numbers.

It is not affected by the extreme values.

**Mode**

It is the most *common number* or the most frequent number in the dataset. 

*No mode*, if the values in a given set all occur the same number of times, the data set has no mode because no number is any more common than any other. 

*Several mode* if more than one number is repeated same number of times.

It is not affected by extreme values.

**Geometric Mean**

It is used to measure rate of change of variable over time. For eg, rate of return on investment over years.

$$ X_G = (X_1 \ x \  X_2 \ x\ ... \ x\  X_n)^{(1/n)} $$

GM rate of return, here $R_i$ is rate of return in time period i

$$ R_G = [ (1 + R_1) \ x \ (1 + R_2) \ x ... x \ (1 + R_n) ]^{(1/n)} - 1 $$

### Effect of Outliers

Removing a big outlier decreases the mean more but less change on median and may be median doesn't change.

## Spread and Variation of Data
The spread of data can be measured by its range, interquartile range (IQR), variance, standard deviation. and coefficient of Variation.

**Range**

It is difference between largest and smallest value in data. It is not dependent on distribution of data and is sensitive to outliers.

**Interquartile Range**

Quartiles divide the ordered data in to 4 segments. Each have equal number of values.  Median (Q2) divides the dataset into two different parts. IQR is the difference in the middle of the first half (Q1) and the middle of second half (Q3). We then find the median of these two different parts and then find the difference. 

If we have even number of data points in dataset then we include the first middle number in first set and the second middle number in second set.

IQR is useful to find out how much the data is varying. 

Range can be misleading when we have outliers. But in this case interquartile range can give us much better measure of spread of data.

$IQR$ = md 2nd quartile - md 1st quartile = $Q_3 - Q_2$

**Quartile Measures**

- Q1, is the value for which 25% of the observations are smaller and 75% are larger
- Q2 is the same as the median (50% of the observations are smaller and 50% are larger)
- Only 25% of the observations are greater than the Q3

A *box plot* shows Min, Q1, Q2, Q3 and Max values of data.

**Measure of spread**

Measure of spread can be found by calculating range variance and standard deviation. 
- Sample is part of data while population is entire dataset. 
- We can estimate population by using these measures from the samples. 

**Variance**

Squared deviation of values from the mean

$$ 𝜎^2 = \frac{ \sum(x_i - 𝜇)^2 }{ n } = \frac{ \sum(x_i)^2 }{ n } - 𝜇^2 $$

**Standard Deviation**

Variation about the mean. It has *same unit as the original data*.

$$ 𝜎 = \sqrt{Variance} = \sqrt{𝜎^2} = \sqrt \frac{ \sum_{1}^n(x_i - 𝜇)^2 }{ n }$$

**For example:**

A = [-10, 0, 10, 20, 30]

B = [8, 9, 10, 11, 12]

Mean of two data set is same (10) but range varies. So we calculate variance to show difference between datasets.

$$ 𝜎^2(A) = 200 $$

$$ 𝜎^2(B) = 2 $$

$$ 𝜎(A) = \sqrt{200} = 10\sqrt{2} $$

$$ 𝜎(B) = \sqrt{2} $$

**Result**

Hence, points in A are 10 times more deviated.

**Note:**

- The more the spread, the greater is range, variance and SD
- The more data is contracted, the smaller these measures are.
- Standard Deviations tells us how far we are from the mean.
- If all values are same (no variation) then all these are zero.
- None of these measures can ever be negative.
- Adding a number to all values, $x_i$, makes no difference to variance.
- Multiplying a number, k, to all values, $x_i$, makes variance  $𝜎^2 \times k$  

**Better measures**

What defines dataset better, mean or median?
- Mean can give us the standard deviation, median can you give us IQR. 
- Mean is better for symmetric dataset, median is better for skewed dataset which has outliers. 
- Median is better for salaries and home prices as it has outliers.

## Measure of Discrete Variables

Discrete Variable has a finite outcome. It has a fixed values. The events are **mutually exclusive**.

### Expected Value

This is measure of center. Also called **weighted average**.

$$ 𝜇 = E(X) = \sum_{i=1}^N X_i P(X=X_i) $$

This is sum of each (value x probability)

### Expected Variance

Difference from mean, squared times probability, then sum:

$$ 𝜎^2 = \sum_{i=1}^N [X_i - E(X)]^2 P(X=X_i) $$


### Expected Standard Deviation

Difference from mean, squared times probability, then sum:

$$ 𝜎 = \sqrt{𝜎^2} = \sqrt{ \sum_{i=1}^N [X_i - E(X)]^2 P(X=X_i) } $$

## Measure of Relations

### Coefficient of Variation

Coefficient is the multiplicative factor. That is how many times a variable is of another variable. 

Here we compare variation and mean. So it **variation relative to mean**. Always in percentage, and can compare data with different units.

$$ CV = \frac{ S }{ X } \times 100\% $$

For example, 

Stock A = $50, SD = $5

CV(A) = (5/50)*100% = 10%

Stock B = $100, SD = $5

CV(B) = (5/100)*100% = 5%

Hence, both stocks have same SD, but stock B is less variable relative to its price.

### Covariance

Measure of strength of linear relationship between two discrete random variables X and Y.

$$ 𝜎_{XY} = \sum_{i=1}^N [X_i - E(X)][Y_i - E(Y)] P(X=X_i,Y=Y_i)  $$

where, $P(X=X_i,Y=Y_i)$ is probability of occurrence of the i outcome of X and the i outcome of Y.

### Coefficient of Correlation

The relative strength of linear relation between two variables is called correlation. It is between -1 and 1.

$$ r = \frac{cov(X,Y)}{S_XS_Y} $$

This is covariance relative to standard deviation. In above,

$$ cov(X,Y) =  \frac{\sum_{i=1}^N [X_i - \overline{X}][Y_i - \overline{Y}]}{n-1} $$
$$ S_X =  \sqrt{ \frac{\sum_{i=1}^N [X_i - \overline{X}]^2}{n-1} } $$
$$ S_Y =  \sqrt{ \frac{\sum_{i=1}^N [Y_i - \overline{Y}]^2}{n-1} } $$

Cor = 0, means no linear relation, but may has non-linear relation.

In investment portfolio, expected return and standard deviation of two funds together can be calculated.

## Shape of Distribution

This tells us how data is distributed. It can be measure by:
- Skewness: Extent to which data values are not symmetrical
- Kurtosis: Affects the peakedness of the curve of the distribution. It tell the sharpness of rise of curve. Bell shaped is Mesokurtic (Kurtosis = 0).

### Skewness

Data can be symmetric, left or right skewed. If it is symmetric then we can work on half of the sample of data.

Left: Mean < Median
Symmetric: Mean = Median
Right: Median < Mean

### Kurtosis

How sharply the curve rises. Eg:
- High rise, Kurtosis > 0, Leptokurtic.
- Bell shaped, Kurtosis = 0, Mesokurtic.
- Low rise, Kurtosis < 0, Platykurtic.

> Image of shape and quartiles and box plot
