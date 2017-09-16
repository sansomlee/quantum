# Grover's Algorithm

### Background
Grover's Algorithm was inspired by Deutsch's to mulnipluate not only the sign of the states but also the coefficients (probability amplitude) of the states.

### Algorithm
Given an oracle and a set of states, find the state where f(x*) = -1. In layman's terms, given a bag of N keys, find the key that can open the door (oracle).
The trick is to amplified the flipped state using average over the mean technique. Once the state's coefficient has been boosted enough, there is a very high chance of the correct key will come up when measured.

### Quantum Circuit
![alt text](resources/1000px-Grovers_algorithm.svg.png)


### Notes
Uw is the door and the diffusion operation is to boost the signal. Run it N^1/2 times will boost the coefficient of the state so that it can be detect for certain at measuring time.

### Simulation
Quirk Simulation for Grover's Alogrightm - http://algassert.com/quirk#circuit={"cols":[["X","X","X","X","X"],["H","H","H","H","H"],["Chance5"],["~vn6c"],["~m0if"],["Chance5"],["~vn6c"],["~m0if"],["Chance5"],["~vn6c"],["~m0if"],["Chance5"],["~vn6c"],["~m0if"],["Chance5"]],"gates":[{"id":"~vn6c","name":"Oracle","circuit":{"cols":[["Z","•","◦","•","•"]]}},{"id":"~m0if","name":"Grover's","circuit":{"cols":[["⊖","⊖","⊖","⊖","X"]]}},{"id":"~gik","name":"|10001>","circuit":{"cols":[["Z","◦","◦","◦","•"]]}}]}

### Links
- I like this blog when explaining how Grover's work - http://twistedoakstudios.com/blog/Post2644_grovers-quantum-search-algorithm
- 
