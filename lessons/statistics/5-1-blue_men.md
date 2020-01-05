[Think Stats Chapter 5 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2006.html#toc50) (blue men)

>> ```python
>> import scipy.stats
>> 
>> # generate the normal distribution of male heights centered around mean = 178 and standard deviation = 7.7
>> mu = 178
>> sigma = 7.7
>> dist = scipy.stats.norm(loc=mu, scale=sigma)
>> 
>> # find the cdfs within the normal distribution of the high and low values of acceptable male heights for the blue man group 
>> five_ten = 177.8
>> sixx_one = 185.4
>> 
>> cdf_low = dist.cdf(five_ten)
>> cdf_high = dist.cdf(six_one)
>> # find the difference in cdfs to find the cdf for males in the blue man group height range
>> between = cdf_high - cdf_low
>> 
>> print(cdf_low, cdf_high, between)
>> # Output --> (0.489639, 0.831734, 0.342095)
>> ```
>>
>> CDF between 5'10" and 6'1" is 0.342
