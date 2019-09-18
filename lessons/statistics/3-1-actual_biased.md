[Think Stats Chapter 3 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2004.html#toc31) (actual vs. biased)

#read in data <br>
resp = nsfg.ReadFemResp()

#generate pmf from numkdhh column
pmf_kids = thinkstats2.Pmf(resp.numkdhh, label = 'PMF') 

#make a copy of pmf_kids 
pmf_kids_bias = pmf_kids.Copy(label='biased PMF')       

#use items to iterate through pmf_kids, then multiply each element
#by the corresponding number of kids to bias the data accordingly
#normalize the generated bias pmf
for x, p in pmf_kids_bias.Items():         
    pmf_kids_bias.Mult(x, x)               
pmf_kids_bias.Normalize()                  

#plot the pmfs
thinkplot.preplot(2)                       
thinkplot.Pmfs([pmf_kids, pmf_kids_bias])
thinkplot.Config(xlabel='kids', ylabel='PMF')

