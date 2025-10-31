# Finite Automata & Regular Languages

## Words
An **Alphabet**, represented by $\sum$, is a finite, nonempty set of symbols.

A **Word**, represented by $w$, is a finite (possibly empty) sequence of symbols from $\sum$. The set of all words over $\sum$ is denoted $\sum$*.

**Examples:**

![alt text](/2ndYear/AaC/Notes%20(AaC)/Images/image.png)

## Languages
Any subset $L \sub \sum$* is called a **Language** over $\sum$

**Examples:**

![alt text](/2ndYear/AaC/Notes%20(AaC)/Images/image-1.png)

## Terminologies
$e$ denotes an **Empty Word**

$|w|$ denotes the **Length** of a **Word**

$w^R$ denotes the **Reverse** of a **Word**

**Palindromes** are **Words** where $w = w^R$

If $u$ and $v$ are **Words** over the same alphabet, then **uv** denotes their **Concatenation**. *E.g.* If $u = a_1...a_m$ and $v = b_1...b_n$, therefore $uv = a_1...a_mb_1...b_n$.

For a **Symbol** $a$ and a **Natural Number** $n$, then $a^n = aa...a$ where the symbol is repeated $n$ times.

**Subwords** are words that are a subset of another word. So if $u$ is a subword of $v$, there exist words $w_1$ and $w_2$ where $v = w_1uw_2$. *E.g.* *ell* is a subword of *hello*, *ello* and *hell*.

## Deterministic Finite Automata
DFA consists of five objects:
* $Q$ is a finite set of **States**
* $\sum$ is an **Alphabet**
* $\delta : Q \times \sum \implies Q$ is the **Transition Function**
* $s \in Q$ is the **Initial State**
* $F \subseteq Q$ is the set of **Accepting States**

**Examples:**

![alt text](/2ndYear/AaC/Notes%20(AaC)/Images/image-2.png)

![alt text](/2ndYear/AaC/Notes%20(AaC)/Images/image-3.png)

## Computations in DFA
The computation of inputs, namely words, into DFA are done as follows:
* First state the DFA, *e.g.* Let $A=(Q,\sum,\delta,s,F)$
* Provide an **Input**, *e.g.* A word $w \in \sum$*
* Read the word $w$ from left to right, and follow the path $A$ where each symbol of the word $w$ correspond to instructions as to where to go in the DFA.
* Finally assess and output, if an **End/Accepting State** is reached, return **Accept**. Otherwise return **Reject**.

For a word $w$ to be accepted by $A$, there must be a sequence of states $\{r_0,...,r_n\} \in Q$ in $A$ where:
* $r_0 = s$. *I.e.* the **First** state is the **Initial** state.
* $\delta(r_i,a_{i+1}) = r_{i+1}$ for $i = 0,...,n-1$. *I.e.* the **Transition** between states, given an **Alphabet** of the word $w$, can be performed for following along the sequence of states $\{r_0,...,r_n\}$. Or in other words, moving closer to the final state is possible.
* $r_n \in F$. *I.e.* the **Final** state in the sequence is also an **Accepting** state.

## Language and DFA Problems
**DFAs** can be used to define **Languages**, and illustrates the method of determining what words are accepted in the language, and also be used to form new words that are also accepted in the language (unless specified otherwise).

The relationship between DFAs and languages is defined as this:
* Let $A=(Q,\sum,\delta,s,F)$
* Therefore, for $L(A) \subset \sum$*...
* Then $L(A) = \{w \in \sum$*$ | A$ accepts $w\}$

In other words, the language $L$ following the DFA denoted by $A$, must contain a **Subset** of words in $\sum$*, where $A$ **Accepts** those words.

A language is a **Regular** language if there exists a DFA denoted by $A$ where $L = L(A)$. In other words, a DFA $A$ can be formed and exists to satisfy all the words in $L$. Not all languages are regular, such as the **Human** language, where not all combinations of alphabets can form acceptable words (*i.e.* absolute gibberish), and so a DFA cannot be easily made.

**DFA to Language example:**

![alt text](/2ndYear/AaC/Notes%20(AaC)/Images/image-4.png)

**Language to DFA example:**

![alt text](/2ndYear/AaC/Notes%20(AaC)/Images/image-5.png)
