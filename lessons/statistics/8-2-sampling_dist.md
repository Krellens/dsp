[Think Stats Chapter 8 Exercise 2](http://greenteapress.com/thinkstats2/html/thinkstats2009.html#toc77) (scoring)

>> REPLACE THIS TEXT WITH YOUR RESPONSE
<pre>
def experiment2(n, m, lam):
    L = []
    for _ in range(m):
        sample = np.random.exponential(1.0/lam, n)
        sample_mean = np.mean(sample)
        L.append(1/sample_mean)
        
    cdf = thinkstats2.MakeCdfFromList(L)
    thinkplot.Cdf(cdf)
    print(RMSE(L,lam))
    ci = cdf.Percentile(5), cdf.Percentile(95)
    print(ci)
experiment2(10, 1000, 2)

</pre>
