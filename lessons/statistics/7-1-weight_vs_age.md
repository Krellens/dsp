[Think Stats Chapter 7 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2008.html#toc70) (weight vs. age)

>> REPLACE THIS TEXT WITH YOUR RESPONSE
<pre>
import first

live, firsts, others = first.MakeFrames()
live = live.dropna(subset=['agepreg', 'totalwgt_lb'])

thinkplot.Scatter(live.agepreg, live.totalwgt_lb, alpha=0.1, s=10)
thinkplot.Config(xlabel='Age (years)',
                 ylabel='Weight (lbs)',
                 legend=False)
                 
SpearmanCorr(live.agepreg,live.totalwgt_lb)

Corr(live.agepreg,live.totalwgt_lb)
