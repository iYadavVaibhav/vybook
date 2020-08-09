# Advance Statistics

This note covers distributions, Confidence Intervals.

## Frequency Distribution

We can break data into different classes, then find frequency of data in each class. It is what we see in histogram.

Each class has a mid point, a frequency. We can find **Relative Frequency** which is frequency divided by total frequency (number of data points). So this give us percentage of data point is a particular class interval.

For eg, class A (10 but less than 20) has frequency 3, total observations 20, so relative freq 0.15, hence, 15% data points are in class A.

We can also find cumulative frequency and relative cumulative frequency or **Cumulative Percentage**. It can help us find probability that a data is under or less than that class interval.

**Use of Frequency Distribution**

- Raw to useful form
- Visually see the data distribution
- See interval in which data is contracted or clustered.

**Tips:**

- Play with class interval to see different picture of data.
- In large dataset, boundaries don't make much difference.
- When comparing different groups with sample, use relative frequency or percentage distribution.


## Probability Distribution Functions (PDF)

A frequency distribution can be a probability distribution if the area under the curve is equal to 1. The f(x) of Prob Dist gives us probability of occurrence of x in the given distribution.

**Random Variables** RV, $X$, are variables that can have any random value $x$. For eg. rolling a die.

$P(X=x)$ is probability that X has outcome x.

$F(x)$ = PDF

$E(x)$ is expected value = weighted average

RV can be of two types:
- Discreet, fixed values, finite outcome, mutually exclusive events.
- Continuous, any value in range, data points are approx values.

Discreet variables PDF:
- Bernoulli Distribution
- Binomial Distribution
- Poisson Distribution

### Bernoulli Distribution

The event has two outcomes, so probabilities are $p$ and $p-1$. 

### Binomial Probability Distribution

When we have to make $k$ success in $n$ attempts, then we can following formula:

$$ P = _nC_k . π^k . (1-π)^{(n-k)} $$

Here π is probability to get success. eg, throwing a basket ball.

Now if we move k from 0 to n, we get different values of P. This can make a distribution. We call this binomial distribution.

### Poisson Probability Distribution


Continuous RV can have PDF:
- Uniform or 
- Normal.

### Uniform Distribution

Here, probability of each outcome is equal. Hence, funcition is 1/range:

$$ f(X) = \frac{1}{(b - a)} $$ 
where a is min and b is max.

Measures:

$$ 𝜇 = \frac{a + b}{2} $$

$$ 𝜎 = \sqrt{  \frac{(b - a)^2}{ 12 }  } $$

Probability that 3 <= x <= 5, is area under the line between 3 and 5. As it is a rectangle, the area can be (base)(height).

### Normal Distribution

It is:
- Bell Shaped
- Symmetrical
- Mean, Median and Mode are equal

The random variable has theoretically infinite range. 

It is defined by:

$$ f(x) = \frac{1}{\sqrt{2\pi}𝜎}e^{-\frac{1}{2}(\frac{X - 𝜇}{𝜎})^2} $$

e = 2.71828
$\pi$ = 3.14159

Mean moves distribution left/right, sd increases/decreases spread.

P(-∞ < X < μ) = 0.5 and P(μ < X < ∞) = 0.5


### Standardized Normal or Z score

Any normal distribution can be transformed to **standard normal distribution** $(Z)$ using mean and sd.

Need to transform X units to Z units.

It has mean of 0 and SD of 1.

$$ z = \frac{X - 𝜇}{𝜎} $$

Also, known as *Z distribution*.

For eg, if mean=100, sd=50 then Z for X=200, (200-100)/50 = 2

This says that X = 200 is two standard deviations (2 increments of 50 units) above the mean of 100.

So for X and Z distribution the shape remains the same, only scale changes.

**Note:** We measure a few scores compared to the mean. Like performance in class. How far are we from the mean in terms of SD. are we 1sd far from mean or so on. One such score is Z score.

#### Calculating Probabilities

The probability is area under the curve. So P(a <= X <= b) is area under curve between x=a and x=b.

**Note:** 
- P(a <= X <= b) = P(a < X < b), as P(a) or P(any point) = 0. 
- The total area under the probability curve is 1 and curve is symmetric so half above mean and half below.

To calculate probability of any RV in a range we need to find area under the curve in that range. So easily find the answers we convert every normal distribution to standard Z distribution. Then from Z Table we look up values for that value of Z. The score at a value gives area from -$\infty$ till that value.

**Z Table** 
- is cumulative probability of standardized normal. 
- the sum of table headers are Z-scores, or how many standard deviation.
- the table values are probabilities.

For eg, Z(2) = 0.9772, this is P(Z < 2, till -infinity)

To find a probability for normal X distribution, convert X to Z the find Z value for it.

Most used Z-scores:
- 90% = 1.645
- 95% = 1.96
- 99% = 2.576

Excel formula 95% CI `=-NORM.S.INV((1-0.95)/2)`

#### Empirical Rules 

1σ covers 68.26% of X

2σ covers 95.44% of X

3σ covers 99.7% of X

Above, everything was calculated for a population. Now we will talk about the samples.




## Sampling  Distributions 

Population is the large group of data that we want to study. We pick a sample of people and try to compare how they perform compared to the population. We collect different sample from the population for example 50 different records from a population.

There will be variation in each of these different samples. So each of these sample gives us slight variation from each other. So sample A is different from sample B and so on. When we collect different samples and find their mean or sd, then this set of information makes sample distribution.



### Developing a Sampling Distributions

If I choose **every possible** sample of size "n" from a population then I get "sampling distribution". Now if we collect mean of each of these possible sample then we get "Sampling distribution of Sample Means".

When we make probability distribution of a population that is unbiased, there are equally likely chance to pick a number. So it is a uniform distribution.

Next, we take all possible sample and find mean of each. The prob distribution of the mean of sample will be a normal distribution.

So we find $𝜇_{\overline{X}}$ and $𝜎_{\overline{X}}$ and n, here n is number of items in each sample.

- x_ is a random variable and not 𝜇, mu is fixed.
- If we find all different mean of samples, `xi` then 90% CI of each xi will have 𝜇.



**Standard Error of the Mean**
- It is variability in the mean from sample to sample of same size. 
- Standard deviation of mean of means. For eg, 
    - if we take random samples of size `n` from a population, we get mean for each sample, $X_i$ . 
    - Different samples have different mean, not all are equal to population mean. 
    - S(A) give mean X(A) and so on. Now all these means $X_i$ = [X(A), X(B), X(C)..]  form a distribution.
    - The standard deviation of this distribution gives us Standard Error. 

$$ 𝜎_{\overline{X}} = \frac{𝜎}{\sqrt{n}} $$

If population is very small:

$$ 𝜎_{\overline{X}} = \frac{𝜎}{\sqrt{n}} \times \sqrt{\frac{N-n}{N-1}} $$


**Note:** The standard error of the mean decreases as the sample size increases.

If population is more and samples is less than 1% then we can ignore (N-n)/(N-1) as this equals to 1.


**Margin of Error**

if we know the width, +-100, and we know sd for population and we know confidence interval so we can find the sample size that can help us achieve this.

DMOE = Margin Of Error

sigma = 4608, dmoe=100, z=1.96

This is sample error:

$$  $$

1.96\*(4608/n\*\*(0.5)) = 100

n = 

pec half, sample 4 times, because of square.

inc confidance, z inc, sample inc.



**Sampling Error**

There is an error associated with mean of a sample. Because it is not exactly same as population mean mu.

We can find a sample size to get desired *margin of error (e)* with (1 - α) level of confidence.

$$ e = Z_{α/2}\frac{𝜎}{\sqrt{n}} $$

$$ n = \frac{Z_{α/2}^2 𝜎^2}{e^2} $$

For eg, what can be the sample size if we want error of $\pm$ 5 with 95% confidence interval when σ=20.



### Central Limit Theorem

It says that the distribution of mean of samples is mostly normal distribution. It is not dependent on shape of original population.

**Irrespective of what population looks like, sample means always follow normal distribution**

$$ \bar{X} =N (\mu ,\frac{\sigma}{\sqrt{n}})  $$

Here, N is normal distribution.

For any population, if we take samples and plot mean of samples, it always follows normal distribution.

the mean is almost equal to pop mean

sd is $ \sigma/\sqrt{n} $

n is sample size

$ \sigma_\bar{x} $ is small then more reliable 𝜇.

if sigma xi is more that means more spread out sample means, hence less reliable x_


### Point and Interval Estimates

Point is a single number, X, in population. We can find confidence interval for that number. Interval estimate tells us more information about the population than a point estimate tells us.

So for eg, 5kg rice packet has SD of 50gm in population. So 3SD would contain 99% of rice packets. Now if we take samples and find mean of samples it would give us a distribution. We can take one Point near 5kg, then we can find the confidence interval in which this mean will lie with a percentage confidence. Like, 95% confidence that x=49.94 is mean and lies between found interval. 

**Point estimate $\pm$ (Critical Value)(Standard Error)**

Point is the sample statistic estimating population parameter of interest.

Critical Value is z table value, based on confidence interval

Standard error is SD of point estimate.

100% is close to infinity, 100% sure that mean will lie between infinities. 95% is also large interval. 0% confidence would be a very small interval.

### Confidence Intervals and Levels
From a sample, we can infer the population parameter by finding its interval and a confidence. 
- For eg, order size. 
- From a sample, we can find CI and say, "We are 95% confident that the order size of population would be between 990 to 1100".

**How to find CI**
- Let alpha, α = probability we are not interested in, the point that lie outside 95%.
- => (1 - α) = 0.95 
- => α = 0.05
- => α/2 = 0.025
- Now, we are interested in points where the probability left out is 0.025, the lower tail, that is -infinity to lower point.
- In Z table, the value 0.025 can be found for Z score 1.9 and .06. So 1.96 is Z score.
- Hence, $Z_{α/2}=\pm1.96$, also called *critical value*.
- This tells us that on a standard curve, sd=1 and mean=0, the 95% confidence interval is +- 1.96. If we go 1.96 sd to left and right of mu, we cover 95% data.
- To find actual values of actual normal curve, we use the formula Point estimate $\pm$ (Critical Value)(Standard Error).

**CI, when σ is known:**

$$ \overline{X} \pm Z_{α/2} \frac{𝜎}{\sqrt{n}} $$

**Increasing Precision**
- If we increase the size of sample, `n` then CI range decreases. 
- So for same confidence we are finding less range interval, this increases precision.

**Use Cases:**
- For cost benefit analysis, for eg, minimum orders we can expect. If that order size makes our new business line profitable, go ahead. 
    - Find CI, CI tells us, that we can expect order size within an interval, 
    - So for 90% CI, it says we are 90% confident that the 𝜇 lies in interval. 
    - So definately we can expect orders more than lower limit.
- We do have 5% **risk involved**. We can further reduce it by finding 95% CI, but that reduces our precision as it increases the interval width.
- Smaller the range of CI, more precise we are. Our aim should be to increase the accuracy with precision. Increase % but also decrease range.
    - eg, 90% conf => 90 < x < 110, to
    - 98 < x < 102, this should be our approach.


### Confidence Interval Sigma Unknown
What if we don't know population standard deviation, sigma?
- Then we use *t-Distribution*.
- it was stated by William Gossett - 'The probable error of mean'
- Degree of Freedom, df = (nCol - 1) X (nRow - 1), from a contingency table.
- When we do not know sigma then we estimate it using proxy.
- We can substitute the sample standard deviation, S.
- This introduces extra uncertainty, since S is variable from sample to sample.- So we increase the interval to cover this uncertainity
- So we use the t distribution instead of the normal distribution.  


**why we use (n-1) in denominator?** 
- To add uncertainity.
- use one proxy, loose one degree of freedom.
- (n-k) loose k degree of freedom.
- We add uncertainity in the confidence interval to keep it safe.

**Student's t Distribution**

It is a family of distributions. Its value depends on degrees of freedom (d.f) = n - 1.

Degree of freedom is a number of observation that can take any value after we have mean calculated.

t -> Z as n increases.

$$ \overline{X} \pm t_{α/2} \frac{S}{\sqrt{n}} $$

where $t_{α/2}$ is the critical value of the t distribution with $n-1$ degrees
of freedom and an area of α/2 in each tail

- df = 1 , then broder and shorter compared to normal distribution.
- as we inc df, it becomes taller and thinner. it gets close to normal distribution.
- as n approcahes infinity, t-distn becomes normal distn.

**Conclusion:**
- So, if you don't know sigma, use t, for any degree of freedom and any conf interval.
- If you know sigma, never use t-distribution.

Use, $S_\bar{x}$ to find CI. Same as we do using sigma x bar.


$$ 
\sigma = \sqrt{ \frac{\sum_1^n (x_i - \mu)^2}{N} } , 
\sigma_\bar{x} = \frac{\sigma}{\sqrt{N}} 
\space\space\space\space\space\space\space\space\space\space\space\space\space\space 
S = \sqrt{ \frac{\sum_1^n (x_i - \bar{x})^2}{(n-1)} } , 
S_\bar{x} = \frac{S}{\sqrt{n}}
$$

|Population|Sample (Proxy)|
|:-|-|
|$ \mu $ = Avg of population, mean | $ \bar{X} $ = Avg of sample|
|N = values in population | n = values in sample|
|$\sigma$ = Std Dev of population | S = Std Dev of sample
|$ \sigma_\bar{X} $ = St Error of population, Sd of sample means | $ S_\bar{X} $ = St Error of sample


$$ CI = \mu \pm Z_{\alpha/2}*\sigma_\bar{x} $$


**Find CI of Population Mean:**
- Find avg, x-bar and sd of sample, S
- find S-X-bar, S by root N
- find t value of Confidence level, using, =T.INV.2T(1-alpha,n-1)
- find upper and lower limit, CI by, S +- (t * S-X_Bar)

Use this CI to tell that mu of population lies between this interval.

**Find 'n' samples required for desiered Confidence and Interval and Average expected**

For, e.g., if we need, 99% accuracy with a margin of 0.01mg in tablets then we can find sample size required.
- find t-value based on conf%

## Estimators and point estimates:
- point estimate is a point we estimate from a sample
- estimator is conf interval
- point is exactly in the middle of conf intvl
- they are both statistic
- e.g. x bar for mu and s^2 for sigma sq.

### Population Proportion

Just like mu we'll build CI for pop proportion 𝜋. Sample proportion 𝑝.

- Hit rate is proportion of people buying sarres
- Based on sample proportion, I can draw population proportion.
- to estimate population proportion form sample proportion we need to find probability distribution. The we can use all CI adn CLT
- Proportion is binomina, success/faliure, interested/non interested. It is state of mind.
- 
- prop depends on sample, bw 0 and 1.
- binomial distn, success or faliure, BD, will buy or not?
- (𝜋) is mean of *appropriately* constructed random variable.
- (p) is sample mean of random variable.

E(x) = n pi
var(x) = n pi (1 - pi)

Q ~ B{n pi, npi(1-pi)}

if x = {0,1} binomial, then
p= Q/n = exi/n, all 0 sum to 0

mathematically identical to x bar.

ci = p +- Za/2, sigma p cap, cap is proxy.





---



### P Value (needs elaboration)

It is same as probability but also take equally likely outcome and rare outcome. So p(two heads, HH) = 0.25. p value of HH is P(HH) + P(TT) + 0 for rare.

