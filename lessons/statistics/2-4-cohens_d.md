[Think Stats Chapter 2 Exercise 4](http://greenteapress.com/thinkstats2/html/thinkstats2003.html#toc24) (Cohen's d)

>> **Problem:**
>>
>> Using the variable `totalwgt_lb` investigate whether first babies are lighter or heavier than others. Compute Cohen's d to quantify the difference between the groups. How does it compare to the difference in pregnancy length?
>>
>> ```python
>> # Compute the difference in pregnancy length
>> firsts.totalwgt_lb.mean() - others.totalwgt_lb.mean()
>> # Output --> -0.12476118
>> # The difference in pregnancy length between first babies and other babies is 0.125 weeks, or 21 hours. 
>> 
>> # Compute the Cohen effect size 
>> CohenEffectSize(firsts.totalwgt_lb, others.totalwgt_lb)
>> # Output --> -0.088673
>> # The difference in means is 0.089 standard deviations.
>> ```
