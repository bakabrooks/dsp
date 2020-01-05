[Think Stats Chapter 4 Exercise 2](http://greenteapress.com/thinkstats2/html/thinkstats2005.html#toc41) (a random distribution)

>> ```python
>> # generate 1000 random numbers
>> random_nums = np.random.random(size=1000)
>> 
>> # plot the pmf of the distribution
>> random_pmf = thinkstats2.Pmf(random_nums)
>> thinkplot.Pmf(random_pmf)
>> thinkplot.Config(xlabel='nums', ylabel='PMF', title="Random Numbers' PMF Plot")
>> ```
>>
>> ![](/Users/baka_brooks/Pictures/q4_p2_pmf.png)
>>
>> It is impossible to discern the distribution of the data from the PMF plot due to the number of data points.
>>
>> ```python
>> # plot the cdf of the distribution
>> random_cdf = thinkstats2.Cdf(random_nums)
>> thinkplot.Cdf(random_cdf)
>> thinkplot.Config(xlabel='percentile rank', ylabel='CDF', title="Random Numbers' CDF Plot")
>> ```
>>
>> ![](/Users/baka_brooks/Pictures/q4_p2_cdf.png)
>>
>> The CDF plot appears linear, therefore we can conclude that the distribution is uniform.
