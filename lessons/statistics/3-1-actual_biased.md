[Think Stats Chapter 3 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2004.html#toc31) (actual vs. biased)

resp = nsfg.ReadFemResp()        #read in data
pmf_kids = thinkstats2.Pmf(resp.numkdhh, label = 'PMF') #generate pmf from numkdhh column
pmf_kids_bias = pmf_kids.Copy(label='biased PMF')       #make a copy of pmf_kids 

for x, p in pmf_kids_bias.Items():         #use items to iterate through pmf_kids, then multiply each element
    pmf_kids_bias.Mult(x, x)               #by the corresponding number of kids to bias the data accordingly
pmf_kids_bias.Normalize()                  #normalize the generated bias pmf

thinkplot.preplot(2)                       #plot the pmfs
thinkplot.Pmfs([pmf_kids, pmf_kids_bias])
thinkplot.Config(xlabel='kids', ylabel='PMF')

