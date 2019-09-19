[Think Stats Chapter 6 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2007.html#toc60) (household income)

<prev>
  median = cdf.Value(0.5)                            #median is midpt of CDF
mean = np.sum(sample)/len(sample)                  #mean is sum of sample divided by len of sample
household_below_mean = cdf.PercentileRank(mean)    #find percentile rank below mean

def central_moment(k, sample):                     #function to find central moments
    central_mom_tally = 0
    for x in sample:                         
        central_mom_tally += (x - mean)**k         #add up (x - mean)**k       
    return(central_mom_tally/len(sample))          #divide by n, whic is len(sample)
    
std = np.sqrt(central_moment(2,sample))            #calculate standard dev
skewness=(central_moment(3, sample))/std**3        #calculate skewness
pearson_skewness = 3*(mean - median)/std           #calculate pearson_skewness

</prev>
