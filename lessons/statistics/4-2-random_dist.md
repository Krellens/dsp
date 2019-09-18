[Think Stats Chapter 4 Exercise 2](http://greenteapress.com/thinkstats2/html/thinkstats2005.html#toc41) (a random distribution)
<pre>
random_nums = [np.random.random() for i in range(1000)]             #generate list of random numbers
random_cdf = thinkstats2.Cdf(random_nums, label = 'random numbers') #create CDF of random numbers
thinkplot.Cdfs([random_cdf])                                        #plot the CDF
#The cdf shows a uniform distribution, which is exactly what we expect

pmf = thinkstats2.Pmf(random_nums)                                  #generate a Pmf
thinkplot.Pmfs([pmf])                                               #plot the Pmf
#the pmf renders, it's just useless since their are so many values
<pre/>
