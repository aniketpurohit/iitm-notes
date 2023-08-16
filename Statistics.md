# Basic Concept 

**Sample space** 
A sample space S is a set. The elements of the set S will be called "outcomes" and should be viewed as a listing of all possibilities that might occur. We will call the process of actually one of the outcomes an "experiement"

**Event** 
Given a sample space S, an "event" is any subset E $`\subset`$ S
"Event" includes both S, the sample space itself, and $`\varnothing`$, the empty set. 

**Probability Space Axioms**
Let S be a sample space and let F be collection of all events
A probability is a function $`P : F \rightarrow [0,1]`$ 
1. P(S) = 1; and
2. If $`E_1, E_2, .... `$ are counatable collection of disjoint events (That is, $`E_i \cap E_j = \varnothing `$ if $` i \neq j`$ , then $`P(\cup_{j=1}^\infty E_j ) = \sum_{j=1}^\infty P(E_j) `$

Explanation: 
- for second axioms, probabilities add when combining a countable number of disjoint events. It is implicit that the series on right hand side of the equation converges.

## Basic properties 
1. P($`\varnothing`$) = 0;
2. If $`E_1, E_2, E_3 ... E_n`$ are finite collection of disjoint events, Then $`P(\cup_{j=1}^\infty E_j ) = \sum_{j=1}^\infty P(E_j)`$
3. If E and F are events with $`E \subset F`$, then P(E) $`\leq`$ P(F).
4. If E and F are events with $`E \subset F`$, then P(F\E) = P(F) - P(E);
5. If E and F are events then P(E $`\cup`$ F) = P(E) + P(F) - P(E $`\cap`$ F).

Proof of (1) 
The empty set is disjoint from itself, so $`\varnothing`$  is a countable disjoint collection of events. 

**Equally Likely Outcomes**
When Sample space of only a countable collection of outcomes, describing the probability of each individual outcome is sufficient to describe the penalty of all events. This is because if A $`\subset`$ S we may simply compute P(A) = P($`\cup_{w \in A} \{w\}`$) = $`\sum_{w \in A} P(\{w\})`$ 

**Uniform** 
Let S = {$`w_1, w_2, .. w_n`$} be a non-empty collection of disjoint events. If E $`\subset`$ S is any subset of S, let P(E) = $`\frac{|E|}{|S|}`$ (*where |E| represent the number of elements in E*) Then P defines a probability on S and P assigns probability to each individual outcome in S.
Finally, let w $`\in `$ S be any single coutcome and let E = {w}. Then P (E) = $`\frac{1}{|S|}`$, so every outcome in S is equally likely. 

## Conditional Probability and Baye's Theorem 
Let S be a sample space with probability P. Let A and B two events with P(B) > 0. Then the conditional probability of A given B written as P(A|B) and is defined by $`\frac{P(A \cap B)}{P(B)}`$

***Theorem :***
Let A be an event and let $`\{ B_i : 1 \leq i \leq n \}`$ be a disjoint collection of events for which $`P(B_i) > 0 `$ for all i and such that $`A \subset \cup_{i=1}^n B_i `$. Suppose $`P(B_i)`$ and $`P(A|B_i)`$ are known, Then P (A)  may be computed as 
$`P(A) = \sum_{i=1}^n P(A|B_i) P(B_i)`$

***Theorem :***
For an integer $`n \geq 2`$, let $`A_1, A_2, .. ,A_n`$ be a collection of events of which $`P(\cap^{j-1}_{j=1} A_j) = P(A1) . \pi^n_{j=2} P(A_j |(\cap^{j-1}_{k=1} A_k) `$

## Baye's Theorem 
Suppose A is an event, $`\{ B_i : 1 \leq i \leq n \}`$ are a collection of disjoint events whose union contains all of A. Futher assume that P(A) > 0 and $`P(B_i) > 0`$ for all $`1 \leq i \leq n`$. Then for any $`1 \leq i \leq n`$,
$`P(B_i|A) = \frac{P(A|B_i)P(B_i)}{\sum^n_{j=1} P(A|B_j)} P(B_j)`$

**Independence**
Two events A dnd B are independent if $`P(A \cap B) = P(A)P(B)`$.
$`P(A|B) = P(A) = P(A|B^c)`$
$`P(A_1 \cap A_2 \cap A_3) = P(A_1)P(A_2)P(A_3)`$

**Mutual Indepedence**
A finite collection of events $`A_1, A_2, ... A_n`$ is a mutuallly independence if $`P(E_1 \cap E_2 \cap .... \cap E_n) = P(E_1)P(E_2) ... P(E_n)`$ whenewver $`E_j`$
is either $`A_j \text{ or }  A_j^c`$. An arbitary collection of events $`A_t`$, where t $`\in`$ I for some index set I is mutually independent if every finite subcollection is mutually independent.

# Sampling and Repeated Trails 

## Bernoulli Trials
