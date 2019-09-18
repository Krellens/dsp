[Think Stats Chapter 2 Exercise 4](http://greenteapress.com/thinkstats2/html/thinkstats2003.html#toc24) (Cohen's d)

<pre>
import numpy as np
import nsfg
preg = nsfg.ReadFemPreg()
live = preg[preg.outcome == 1]
first_babies = live[live.birthord == 1]
other_babies = live[live.birthord != 1]

def CohenD(group1,group2):
    meanDiff = abs(group1.mean() - group2.mean())
    pooledStdDev = ( np.sqrt((group1.std()**2 + group2.std()**2)/2) )
    d = meanDiff/pooledStdDev
    return(d)

CohenD(first_babies.prglngth, other_babies.prglngth)
CohenD(first_babies.totalwgt_lb, other_babies.totalwgt_lb)

#The cohen D value for total weight is larger than the cohen D value for pregnancy length, although both are well
#below .2 and thus relatively statistically insignifigant 
</pre>
