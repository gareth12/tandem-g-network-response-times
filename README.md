Tandem G-network response times
===============================

This code seeks to implement the results from
* *[Response Time Distributions in Tandem G-Networks](http://www.jstor.org/stable/3214932)* by  Peter G. Harrison and Edwige Pitel, Journal of Applied Probability, Vol. 32, No. 1, Mar., 1995 pp. 224-246.

This paper computes the [Laplace–Stieltjes transform](https://en.wikipedia.org/wiki/Laplace%E2%80%93Stieltjes_transform) of the response time distribution in a tandem [G-network](https://en.wikipedia.org/wiki/G-network) with two nodes. The parameters for the model are the positive arrival rates at each node (l1p and l2p) the negative arrival rates at each node (l1n and l2n) and the service rates at each of the two nodes (m1 and m2).

NOTE: The current implementation of the code works correctly in the annulus R<sub>L_e\L</sub> ∩ R<sub>C</sub> only, and not in R<sub>L</sub>.

The value of the transform W*(s) at s (for positive s) can be computed using the function

``Wstar[s]``

or parameters for the positive customer arrival rates, negative customer arrival rates and service rates at each node can be supplied

``Wstar[s,l1p,l1n,l2p,p2n,m1,m2]``

Numerical examples
------------------

```
Wstar[0.001, 3, 2, 0, 2, 2, 1]
0.166163
```

This correctly computes the probability that a customer will not be killed (maximal value of the [CDF](https://en.wikipedia.org/wiki/Cumulative_distribution_function)) as it is in the annulus region.
