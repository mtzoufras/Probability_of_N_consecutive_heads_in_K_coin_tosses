#  What is the probability P of getting N consecutive heads at least once in K tosses of a fair coin?

__Quick answer:__ The exact result is P=1-F<sub>K+2</sub><sup>(N)</sup>/2^K, where $F_{K+2}^{(N)}$ is the Fibonacci N-step number. For a good approximation I calculate $x = \frac{K-N+2}{2^{N+1}}$ and if $x\lesssim 0.1$ then $P\simeq x$, else $P\simeq 1-e^{-x}$.

__Corollary:__ This yields an approximate expression for the Fibonacci N-step number: $F_{K+2}^{(N)} \simeq 2^K \exp\left(-\frac{K-N+2}{2^{N+1}}\right)$

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
    
    The answer is usually given in terms of the [_Fibonacci N-step_](http://mathworld.wolfram.com/Fibonaccin-StepNumber.html) sequence. The derivation is straightforward (see the Appendix at the bottom) but since the Fibonacci is not an explicit function of the variables N and K the resulting formula is very opaque.  Here I will show a couple of simple semi-analytical (...) expressions and discuss their accuracy:
1. $P \simeq 1 - \exp\left(-\frac{K-N+2}{2^{N+1}}\right)$, with accuracy that generally improves with increasing $N,K$ 
2. If $\frac{K-N+2}{2^{N+1}}\ll 1$ then $P \simeq \frac{K-N+2}{2^{N+1}}$. 

![table](https://github.com/mtzoufras/Probability_of_N_consecutive_heads_in_K_coin_tosses/blob/master/Kflips.png?raw=true)
