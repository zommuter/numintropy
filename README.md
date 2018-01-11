# numintropy
Numerics minimizing entropy.

This project aims at creating a Python library for "sufficently" imprecise numerics. Basically it boils down to providing a probability distribution of values, applying algorithms or simple mathematical functions on them and obtain another probability distribution for the output values. From an information theory point of view the requirement is keeping the entropy as low as possible. Other ideas for the name were:

* EEP - exactly error propagation
* EIN - exactly imprecise numerics

But I decided to pick both a sufficiently unique name and nod at information theory. And entropy is humanity's nemesis anyway, so let's mention that eternal struggle...

# Basics
Mathematics could be so simple: Take a number $x$, apply some function $f$ on it and get the result $f(x)$. But both $x$ and $f$ could be imprecise: $x$ due to physical measurement (let's call this **input imprecision**), $f$ due to an algorithm that has to finish in a finite time (and let's call this one **algorithmic imprecision**). So you end up with an imprecise $f(x)$ as well. And of course this imprecision propagates if you chain multiple functions. Let's have a close look at this.

## Input imprecision
Any value the imprecision of which cannot be influenced numerically, be that due to physical constraints such as the uncertainty principle or a suboptimal measurement setup, due to insufficient information or any other reason. The two most typical forms of imprecision encountered here are intervals (e.g. a measurement with a ruler is basically only precise up to half a scale tick mark) and Gaussian distributions.

## Algorithmic imprecision
Any value the imprecision of which *can* be influenced. Examples include iterative solvers e.g. for differential equations which would theoretically converge given infinite time but will already stop after a given criterion is matched. If the precision is insufficient, it can however be increased.

## Imprecision propagation
The combination of input imprecision and algorithmic imprecision causes the output of any algorithm to be imprecise as well. Typical methods used to estimate error propagation include truncated Taylor series expansions and interval arithmetic. Ultimately, this project shall however yield much more precise estimations for the actual output imprecision, or rather a sufficiently *exact* output value distribution.

## Minimizing entropy
Finally, the project shall not just propagate imprecision as good as possible, but also offer means to minimize the entropy of the output distribution by determining which parameters of the algorithms to tune in order to sufficiently decrease the algorithmic imprecision.
