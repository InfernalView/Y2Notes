# NFAs & DFAs

## Power-Set Construction
Is a an 'algorithm' for obtaining a DFA from an NFA. Which is defined as:
* **Input**, a NFA denoted $A$
* **Output**, a DFA denoted $A'$ such that $L(A') = L(A)$

In other words (as a theorem):
* *"A language $L$ is accepted by some NFA if it is accepted by some DFA. Therefore the class of languages that are accepted by NFAs is preceisely the regular languages"*.
* Put simply, a language that is accepted by (*i.e.* formed into) an NFA and DFA, is a **Regular Language** and is in the class of regular languages.

Reminder: a **Powerset** of a set is the set of all subsets of that set
$\Rho(\{a,b\}) = \{\empty,\{a\},\{b\},\{a,b\}\}$

...

directly reachable if from the current state there is an empty transition, it would be combined in a subset like $\{1,2\}$ as opposed to separate $\{1\}$ and $\{2\}$

## General Construction
...
