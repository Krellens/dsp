[Think Stats Chapter 3 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2004.html#toc31) (actual vs. biased)

resp = nsfg.ReadFemResp()
pmf_kids = thinkstats2.Pmf(resp.numkdhh, label = 'kids')

pmf_kids_bias = pmf_kids.Copy(label='kids bias')
for x,p in pmf_kids_bias.Items():
    pmf_kids_bias.Mult(x,x)
pmf_kids_bias.Normalize()

thinkplot.PrePlot(2)
thinkplot.Pmfs([pmf_kids, pmf_kids_bias])
thinkplot.Config(xlabel='Kids', ylabel='PMF')
