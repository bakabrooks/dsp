[Think Stats Chapter 3 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2004.html#toc31) (actual vs. biased)

>> **Problem:**
>>
>> Something like the class size paradox appears if you survey children and ask how many children are in their family. Families with children are more likely to appear in your sample, and families with no children have no chance to be in the sample.
>>
>> Use the NSFG responded variable `NUMKDHH` to construct the actual distribution for the number of children under 18 in the household.
>>
>> Now compute the biased distribution we would see if we surveyed the children and asked them how many children under 18 (including themselves) are in their household.
>>
>> Plot the actual and biased distributions, and compute their means. As a starting place, you can use `chap03ex.ipynb`.
>>
>> ```python
>> resp = nsfg.ReadFemResp()
>> 
>> # Compute the actual PMF 
>> pmf = thinkstats2.Pmf(resp.numkdhh, label='actual')
>> 
>> def BiasPmf(pmf, label):
>>   '''
>>   Calculates observed values given an input distribution's pmf and returns the biased distribution.
>>   
>>   Parameters:
>>   pmf (thinkstats2.pmf): pmf of the actual distribution.
>>   label (string): label for the pmf.
>>   
>>   Returns:
>>   thinkstats2.Pmf'''
>>   new_pmf = pmf.Copy(label=label)
>> 
>>   for x, p in pmf.Items():
>>    new_pmf.Mult(x, x)
>> 
>>   new_pmf.Normalize()
>>   return new_pmf
>> 
>> biased_pmf = BiasPmf(pmf, 'observed')
>> 
>> thinkplot.Preplot(2)
>> thinkplot.Pmfs([pmf, biased_pmf])
>> thinkplot.Show(xlabel-'children under 18 in household', ylabel='PMF')
>> ```
>>
>> ![](/Users/baka_brooks/Documents/metis-pre-work/metis-pre-work-notes/thinkstats_chap3_fig.png)
>>
>> ```python
>> # Find the mean of the biased and unbiased PMFs
>> print('Pmf mean: ', pmf.Mean())
>> print('Biased pmf mean: ', biased_pmf.Mean())
>> ```
>>
>> Pmf mean: 1.024205155043831
>>
>> Biased pmf mean: 2.403679100664282
