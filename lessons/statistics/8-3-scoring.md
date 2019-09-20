[Think Stats Chapter 8 Exercise 3](http://greenteapress.com/thinkstats2/html/thinkstats2009.html#toc77)

---
<pre>
def SimulateGame(lam):
    """Simulates a game and returns the estimated goal-scoring rate.

    lam: actual goal scoring rate in goals per game
    """
    goals = 0
    t = 0
    while True:
        timebetweengoals = random.expovariate(lam)
        if t>1:
            break
        goals += 1
        t += timebetweengoals
    return goals
    
 def multiGame(number_of_games, lam):
    L = []
    for _ in range(number_of_games):
        L.append(SimulateGame(lam))
    return (RMSE(L, lam),MeanError(L,lam))
multiGame(1000, 2)
#This way of making an estimate is not biased, because our lambda value 
#grows closer to the true value as we run more trials

<pre/>
---
