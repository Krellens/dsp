[Think Stats Chapter 5 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2006.html#toc50) (blue men)
<pre>
import scipy.stats

mu = 178
sigma = 7.7
dist = scipy.stats.norm(loc=mu, scale=sigma)


bluemengroup_eligible = dist.cdf(185.42) - dist.cdf(177.8)
bluemengroup_eligible
#find the percentage of people who are below 185.42 cm, and it subtract the percentage of people who are below <br>
#177.8 cm. The final result will be the percent of the population between these two values, which is 34.2%
</pre>

