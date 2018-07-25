# annaGP
Implementation of Anna's GP thesis work

## Basics of node gains

In classic GP, solutions are evolved in the form of "expression trees" that can be written in Polish notation. E.g, the function f(x,y) = 2*x + y/4 would be represented as:
(+ (* 2 x) (/ y 4))  -> this tree has a length = 7 nodes

in "node gain GP" each node has a numerical value that multiplies it, called a gain. The same function can be expressed as follows:

([1] + ([2] x [0.25] y)  -> this tree has a length = 3 nodes

The same can be represented as two vectors: a node vector and a gain vector
(+ x y)     -> node vector
(1 2 0.25)  -> gain vector

## Learning (adaptation) of node gains

The values in the gain vector need to be adapted. A "fast and simple" way to do it is by Simulated Annealing.
