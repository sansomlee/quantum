# Deutsch's Algorithm

### Background
David Deutsch attemps to show the differences of quantum computing and classical computing using the simplest possible algorithm

### Alogrithm
Given an oracle, a binary function f:{0,1}->{0,1}, find out if it is a constant function (gives all 0s or all 1s) or balance function (half the time 0 and half the time 1). It is possible to only invoke oracle once to verify the function using Quantum Parallelism.

### Quantum Circuit

#### |x,y> -> |x, y ⊕ f(x)>
The trick is to use XOR gate to construct a f-CNOT gate to test the function if it is a constant or balance one.

![alt text](DeutschCircuit.png)


Note that H|0>= 1
2
√ (|0 > +|1 > ) and H|1>= 1
2
√ (|0 > −|1 > ) so the input to Uf is
1
2
√ (|0 > +|1 > )
1
2
√ (|0 > −|1 > ). Let us look at Uf


x > 1
2
√ (|0 > −|1 > )

=
1
2
√ Uf(|x > (|0 > −|1 > ))=
1
2
√ (Uf(|x > |0 > ) − Uf(|x > |1 > ))=
1
2
√ ((|x > |0 ⊕ f(x) > ) − (|x > |1 ⊕ f(x) > ))
Suppose f(x)=0. Then 0 ⊕ 0 = 0 and 1 ⊕ 0 = 1 so the right hand side becomes


x > 1
2
√ (|0 > −|1 > ) which can
be written as (−1)f(x)


x > 1
2
√ (|0 > −|1 > ). If f(x)=1 then the right hand side becomes


x > 1
2
√ (|1 > −|0 > )
which can be written as (−1)f(x)


x > 1
2
√ (|0 > −|1 > ) where this time f(x)=1 implies (−1)f(x) = −1.
Now suppose f(0)=f(1)=0. Then when we evaluate Uf

1
2
√ (|0 > +|1 > )
1
2
√ (|0 > −|1 > )

we get the result
(−1)0
h
|0 > +|1 >
2
√
ih |0 > −|1 >
2
√
i
and if f(0)=f(1)=1 we get the result (−1)1
h
|0 > +|1 >
2
√
ih |0 > −|1 >
2
√
i
. If we now
apply the Hadamard gate to the first qubit of either of these we get (−1)f(x)H
h
|0 > +|1 >
2
√
ih |0 > −|1 >
2
√
i
and
since H
h
|0 > +|1 >
2
√
i
=


0 > we get(−1)f(x)
|0 >
h
|0 > −|1 >
2
√
i
so if we measure the first qubit we get 0. If f(0)=0
and f(1)=1 we get h
|0 > −|1 >
2
√
ih |0 > −|1 >
2
√
i
and if f(0)=1 and f(1)=0 we get −
h
|0 > −|1 >
2
√
ih |0 > −|1 >
2
√
i
and if we
apply H to the first qubit we get +
−
|1 >
h
|0 > −|1 >
2
√
i
since H

|0 > −|1 >
2
√

= 1 so if we measure the first qubit
we get 1. Thus that measurement will tell us whether the function is constant (measured 0) or not constant
(measured 1). Of course, this works because of quantum parallelism.
