# Grover's Algorithm

### Background
Grover's Algorithm was inspired by Deutsch's to mulnipluate not only the sign of the states but also the coefficients (probability amplitude) of the states.

### Algorithm
Given an oracle and a set of states, find the state where f(x*) = -1. In layman's terms, given a bag of N keys, find the key that can open the door (oracle).
The trick is to amplified the flipped state using average over the mean technique. Once the state's coefficient has been boosted enough, there is a very high chance of the correct key will come up when measured.

### Quantum Circuit
![alt text](resources/1000px-Grovers_algorithm.svg.png)
