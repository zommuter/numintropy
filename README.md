# numintropy
Numerics minimizing entropy.

This project aims at creating a Python library for "sufficently" imprecise numerics. Basically it boils down to providing a probability distribution of values, applying algorithms or simple mathematical functions on them and obtain another probability distribution for the output values. From an information theory point of view the requirement is keeping the entropy as low as possible. Other ideas for the name were:

* EEP - exactly error propagation
* EIN - exactly imprecise numerics

But I decided to pick both a sufficiently unique name and nod at information theory. And entropy is humanity's nemesis anyway, so let's mention that eternal struggle...

# Basics
Mathematics could be so simple: Take a number $x$, apply some function $f$ on it and get the result $f(x)$. But both $x$ and $f$ could be imprecise: $x$ due to physical measurement (let's call this **input imprecision**), $f$ due to an algorithm that has to finish in a finite time (and let's call this one **algorithmic imprecision**). So you end up with an imprecise $f(x)$ as well. And of course this imprecision propagates if you chain multiple functions. Let's have a close look at this.

## Input imprecision

## Algorithmic imprecision

## Imprecision propagation
