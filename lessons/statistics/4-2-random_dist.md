[Think Stats Chapter 4 Exercise 2](http://greenteapress.com/thinkstats2/html/thinkstats2005.html#toc41) (a random distribution)

>> Yes the distribution of the numbers generated by *numpy.random.random* is uniform! Here is are the plots to prove it:


**PMF of numpy.random.random**

![PMF of numpy.random.random](/lessons/statistics//PMF_of_numpy.random.random.png) 

**CDF of numpy.random.random**

![CDF of numpy.random.random](/lessons/statistics//CDF_of_numpy.random.random.png) 

Code:
```
pmf = np.random.random(1000,)
cdf = np.random.random(1000,)
pmf_real = thinkstats2.Pmf(pmf)
thinkplot.Pmf(pmf_real)
thinkplot.Config(xlabel='Random numbers between 0 and 1', ylabel='Pmf')
cdf_real = thinkstats2.Cdf(cdf)
thinkplot.Cdf(cdf_real)
thinkplot.Config(xlabel='Random numbers between 0 and 1', ylabel='CDF')
```
