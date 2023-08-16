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


