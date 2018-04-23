#  What is the probability P of getting N consecutive heads at least once in K tosses of a fair coin?

This question shows up a lot online. For example:
* Quora: 
    * [Run of 5 in 11](https://www.quora.com/What-is-the-probability-of-getting-5-consecutive-heads-in-11-tosses-of-a-fair-coin) 
    * [Run of 5 in 10](https://www.quora.com/What-is-the-probability-of-getting-5-consecutive-heads-in-10-tosses-of-a-fair-coin)
* PhysicsForums: 
    * [Run of 15 in 40](https://www.physicsforums.com/threads/what-is-the-probability-of-getting-15-or-more-consecutive-heads-over-40-coin-tosses.331603/) 
* Math.StackExchange: 
    * [Run of 20 in 100](https://math.stackexchange.com/questions/417762/probability-of-20-consecutive-success-in-100-runs) 
    * [Run of 7 in 150](https://math.stackexchange.com/questions/4658/what-is-the-probability-of-a-coin-landing-tails-7-times-in-a-row-in-a-series-of)
* DrDobbs: 
    * [Run of 20 in 1,000,000](http://www.drdobbs.com/architecture-and-design/20-heads-in-a-row-what-are-the-odds/229300217)
    
The answer is usually given in terms of the [Fibonacci N-step](http://mathworld.wolfram.com/Fibonaccin-StepNumber.html) sequence but since the Fibonacci N-step is not an explicit function of the variables N and K the resulting formula is very opaque.  In the attached notebook I derive a couple of simple semi-analytical expressions and discuss their accuracy. These expressions are:

![Prob1](https://latex.codecogs.com/gif.latex?P&space;\simeq&space;1&space;-&space;\exp\left(-\frac{K-N&plus;2}{2^{N&plus;1}}\right))

with accuracy that generally improves with increasing _N,K_. And if: 

![Prob2](https://latex.codecogs.com/gif.latex?\frac{K-N&plus;2}{2^{N&plus;1}}\ll&space;1\Rightarrow&space;P&space;\simeq&space;\frac{K-N&plus;2}{2^{N&plus;1}})

For the examples listed above we obtain:
![table](https://github.com/mtzoufras/Probability_of_N_consecutive_heads_in_K_coin_tosses/blob/master/Kflips.png?raw=true)
