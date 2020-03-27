[Think Stats Chapter 3 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2004.html#toc31) (actual vs. biased)

>> You can see from the following plot and data that if you were to ask children how many children were in their family that you'd get a very biased dataset for how many children there are per family. Obviously, families with no children wouldn't be represented at all and families with multiple children would be overrepresented. This results in a huge difference in means between the observed values (mean of 1.02 children per family) and the biased values (mean of 2.4 children per family).

![Plot of Actual vs. Biased Distributions](/lessons/statistics/exercise3-1.png)

**Biased mean: 2.403679100664282**

**Unbiased mean: 1.024205155043831**

Code:
```
pmf2 = thinkstats2.Pmf(resp.numkdhh, label='actual distribution of # of children')
biased_pmf2 = BiasPmf(pmf2, label='observed distrubution of # of children')
thinkplot.PrePlot(2)
thinkplot.Pmfs([pmf2, biased_pmf2])
thinkplot.Config(xlabel='Number of Children', ylabel='PMF')
print('Unbiased mean:', pmf2.Mean())
print('Biased mean:', biased_pmf2.Mean())
```
