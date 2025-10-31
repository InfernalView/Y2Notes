# Non-Deterministic Finite Automata

## Non-Deterministic Finite Automata
NFA is different to a DFA, in that it can accept two different transitions with the same alphabet, or include the **Empty** letter in the alphabet. Or put in simpler terms: when reading a word, it is essensial to know **Exactly** which state to transition to. All DFAs are NFAs, that uniquely doesn't have the properties as mentioned.

NFA consists of five objects, like DFA, but slightly different:
* $Q$ is the set of **States**
* $\sum$ is an **Alphabet**
* $\triangle \subseteq Q \times (\sum \cup \{e\}) \times Q$ is the **Transition Selection**
* $s \in Q$ is the **Initial State**
* $F \subseteq Q$ is the set of **Accepting States**

NFA can be defined in terms of a **Transition Function** as this:
$$\delta : Q \times (\sum \cup \{e\}) \implies \Rho (Q)$$

## Computations in NFAs
Let $A = (Q,\sum,\triangle,s,F)$ be a NFA, and $w$ is a word in $\sum$*. Then $A$ accepts $w$ if there exists:
* $y_1,...,y_n \in \sum \cup \{e\}$ such that $w = y_1,...,y_n$
* ...And a sequenct of states $r_0,...,r_n \in Q$

Such that:
* $r_0 = s$
* $(r_i,y_{i+1},r_{i+1}) \in \triangle$ for $$i = $0,...,n-1$
* $r_n \in F$

NFAs are very useful, it is gererally far easier to find a NFA that accepts a language, compared to finding a DFA. And NFAs can allow for carrying out 'powerful' general constructions; as shown below:
![alt text](/2ndYear/AaC/Notes%20(AaC)/Images/image-6.png)
