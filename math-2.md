vectors

# Matrices

A matrix is a rectangular array of number, arranged in rows and columns.
Example : [ [ 1,2,3 ], [ 2,3,4 ] ]
This is a $`2 \times 3`$ (2 rows and 3 columns)

- An $m \times n$ has m rows and n columns
- (i,j)-th entry of a matrix is the entry occuring in the i-th row and j-th column

#### Square matix

A Square matrix is a matrix in which the number of row is the same as number of columns

- the i-th diagoal entry of square matrix is (i,i)-th entry
- The diagonal of a sqaure matrix is the set of diagonal entries.

#### Diagonal matrices

A square matric in which all entries except the diagonal are 0 called diagonal matrix

example : [[ 1,0,0 ], [ 0, -3, 0],[ 0,0,4.2 ]]

#### Scalar Matrices

A diagonal matrix in which all the entries are equal is called a scalar matrix.

example : [ [ -3,0,0 ], [ 0,-3,0 ], [ 0,0,-3]]

#### identity Matrx

A scalar matrix with all entries 1 is called indetity matrix  and is doneted by _I_

## Linear Equation

Any set of equation can be represented as  Ax = B

There are 3 possibilities for the solutions to a linear system of equation

- The system has infintely many solution
- The system has a unique solution
- The system has no solution

### Determinants

Every square matrix A has a number associated number, called its determinanat and denoted by _det(A) or_ |A|

- solving a system of linear equation
- finding the inversse of a matrix
- calculus and more

**Properties**
det(AB) = det(A) det(B)
det($`A^{-1}`$) = $`\frac{1}{det(A)}`$

- swithing of two rows or columns det(initial) = -  det(after)
- adding multiples of row to another row. det(initial) = det(after)
- mutiplying a row by scalar t = det(A) = t. det(A)
- det($`A^n`$) = $`det(A)^n`$
- det($`A^{-1}`$) = $`det(A)^-1`$
- det(AB) = det(BA)
- det($`A^T A`$)  = det$`(A)^2`$
- Switching two rows and columns changes the sign.
- the determinat of matrix with row or column of zeros is 0
- The determinant of a mtrix in which one row (or column) is a linear combination of other rows (resp column) is 0
- Scalar multiplication of a row bya constant t multiplies the determinat by t
- While computing the determinant along a suitable row or column.

The transpose of $`A_{m \times n}`$ is the $`n \times m`$ with (i,j)-th entry A_{ji}

Notation : $`A^T`$
Defination: $`(A^T)_{ij}= A_{ji}`$

det(A ) = det($`A^T`$)

Minors and Cofactors
if A is $`n \times n`$ square matrix with n $`\leq`$ 4. Then the minor of the entry in the i-th row and j-th column is determinanat of the submatrix by deleting the i-th row and j-th column.

name: the (i,j)-th minor
Notation : $`M_{ij}`$

![Alt text](./img/minors.png)

The (i,j)-th cofactor $`C_{ij} = (-1)^{i+j} M_{ij}`$

## cramer's Rule

COnsider the following system of linear equations
$`4x_1 - 3x_2 =11 \\ 6x_1 +5x_2 = 7`$
Matrix representation : Ax = B
the matrix A is given by A = [[ 4, -3 ],[ 6,5 ]] , b = [ 11, 7]

> A must be invertible matrix

**steps**

- make coefficeint matrix A
- calculate det(A)
- Replace the first column of A by the column vector b and call it $`A_{x_1}`$
- Replace the second column of A by the vector b and call it $`A_{x_2}`$

Generally , $`A_{x_i}`$ to be matrix obtained by replacing the i-th column of A by the vetor b. cramer'r rule states the ubique solution is :
$`x_i= \frac{det(A_{x_i})}{det(A)}`$

## the solution of a system of linear equation with an invertible coefficient matrix

Let A be an $`n \times n`$ matrix. The inverse of A is another $`n \times n`$ matrix B such that AB = BA = $`I_{n \times n}`$ and is denoted by $`A^{-1}`$

Conclusion: inverse of A exists => det(A) has to be non-zero

### the adjugate of square matrix

The (i,j)-th minor is the determinat of the submatrix formed by deleting i-th row and j-th column.
the (i,j)-th  cofactor is ndefined as : $`C_{ij} = (-1)^{i+j} M_{aij}`$
The cofactor  matrix C is the matrix whsoe (i,j)-th entry is C_{ij}
The adjugate matrix of A is deined as : adj(A) = C^{T}

the $`A^{-1}`$ is computed by = $`\frac{1}{det(A)} adj(A)`$

***Solutions***

COnsider the system  of linear  eqautiopn of Ax=b where the coefficient matrix A is an invertiable matrix
Multiplying bith sides by $`A^{-1}`$ we obtain
Ax = b
x = $`A^{-1}b`$

***Homogeneous equations***

A system of linear equation is homogeneous if all of the constant terms are 0.b = 0

The matrix form of a homogeneous system is Ax= 0
If  A is ivertible matrix then multiplying both sides by $`A^{-1}`$. we obtain x = $`A^{-1} 0`$ = 0

A homogeneous  syste m of linear equation with n eqaution s in n unknowns

- has a unique solution 0 if its coeeficient matrix is invertible. i.e. its determinat is no-zero.
- has an infinite number of solutions if its coefficient matrix is not invertible. its determinant is 0.

## the echelon form

A general system of m linear equation with n unknowns can be written as

$`\begin{equation} a_{11} x_1 + a_{12} x_2 + a_{13} x_3 = b1 \\ a_{21} x_1 + a_{22} x_2 +...+ a_{23} x_3 = b2\\ . \\ .\\ . \\ a_{m1} x_1 + a_{m2} x_2 + a_{mn} x_n = b1 \end {equation}`$

Matrix representaion of this system of linear eqaution is Ax=b where
![Alt text](./img/matrix-representaton.png)

A solution is an assignment of values for x so that the eqautions are satisfied.

### Reduced Row echelon form

A matrix is in row echleon form if:

- the first non-zero element in each row, called the leading entry is 1.
- Each leading entry is in an column to the right of leading entry in the previous row.
- Rows with all zero elements, if any, are below rows having a non-zero elememt.
- For a non-zero row, the leading entry in the row is the only non-zero in its column.

### Solutions of Ax =b when A is in reduced row echleon form

let Ax =b be a system of linear equation and suppose A is in reduced row echleon form.
Suppose for some i, $`i^{th}`$ row of A is a zero row but $`b_i \neq 0`$ Then this system has no solution.

Reason: This means if we write the corresponsing system of linear equations: the $`i^{th}`$ eqaution reads
$`0 x_1 + 0 x_2 + ... + 0 x_n = b_i`$
since $`b_i \neq 0`$ this cannot be satisfied.

Let Ax = b be a system of linear equations and suppose A is in reduced row echleon form.  
Assume that for every zero row of A, the corresponding entry of b is also 0 (i.e. if the $`i^{th}`$ row  of A is zero, so is $`b_i`$)

- If the i-th column has the leading entry of some row, we call $`x_i`$ a dependent variable
- if the i-th column does not have the leaading entry of some row , we call $`x_i`$ an idenpendent variable.
- Assign arbitary values to independent variables.
- For a dependent variable, there is a unique equation in which
it occurs. All other variables in that equation are independent
variables and thus have values assigned. Hence, we can
compute the value of the dependent variable from this
equation substituting the assigned values for the other
independent variables in the equation.
- The obtained value for $`x_i`$ give a solution to  the system.
- in fact every solution is obatined in this way.

Conclusion: If A is in reduced roe echleon form, this easy procedure provides us with all the solution of Ax= b.

## Row reduction

operation allowed

1. Interchange of two rows
2. Scalar multiplication of a row by a constant t.
3. Adding multiples of a row by another row.

For a sqaure matrix A:

Observe :
row reducing A into row echleon form produces an upper trangle matrix with diagonal entries all 1 (if it is invertible) or some 1s and 0s.

- Row reduce A into row echleon form.
- If the diagonal entries of the reduced matrix contain a 0, then
its determinant is 0 and tracing the determinant back along
the row reduction procedure shows that the determinant of A
must be 0.
- If the diagonal entries of the reduced matrix are all 1s its
determinant is 1. Tracing back along the procedure used to
row reduce using the table of how the determinant changes
according to elementary row operations, we can compute the
determinant of A.

#### the augmented matrix

Let Ax =b be a system of linear eqautions wher A is an $`m \times n`$ matrix and b is a $`m \times 1`$ column varctor.
the augemented matrix of this system is defined as the matrix of size $`m \times (n+1)`$ whose fiorst n columns are the columns of A and last column is b.
We denoted the argumented matrix by [A|b] and  put a vertcial line between the first n columns and the last column b while writting it.

## Guass Elimination Method

Consider the system of linear equations Ax= b

1. Form the augmented matrix of the system [A|b]
2. Perform the same operations on [A|b]  that we used to brinfg A into reduced row echleon form.
3. Let R be the submatrix of obtained matrix of the  first n columns and c be the submatrix of the obtained matrix consisting of the last column.

We write the obntained matrix as [R|c]. Notice that R is the reduced  row echelon matrix obtained by row reducing A.
> the solutioon sof Ax= b are preciesly solutoins of [R|c]

4. Form the corresponding  system of linear equations Rx=c
5. Find all the solutioons of Rx=c and hence of Ax= b

Since R is in reduced row echleon form. we can find ALL  its solutions (as described earlier)

### homogenous system of linear equations

0 is always a solution of homogenous system of linear equations Ax = 0. This solutions is called _trivial solution_

For a homogenous system, there are  two different possibilities:

- 0 is the unique solution
- there are infintely many solutions other than 0

In a homogeneous system of equations, if there are more variables that equations, then it is guaranteed. to have nontrivial solutions.

***Computing the inverse***

Computing the inverse of an invertibel matrix A is equivalent to : finding solution of $`A_x = [1.0.0]`$, $`A_y =[0,1,0]`$, $`A_z = [0,0,1]`$

# Vector space

Consider vectors ($`x_1,x_2,x_3 ..., x_n`$) in $`\R^n`$ and $`c \in \R`$

- Recall addition and scalar multiplication of these vectors is defined as

**Properties**
let v, w and v' bec vectors in $`\R^n`$ and a,b $`\in \R`$

1. v+w = w+v
2. (v+w) + v' = v +(w+v')
3. the 0 vector statisfies v+0 = 0+v = v
4. the vector -v satisfies v +(-v) = 0
5. 1v = v
6. (ab) v = a(bv)
7. a(v+w) = av +bw
8. (a+b)v = av+bv

A vector space is a set of two operations (called addition and scalar multiplication with above properties 1-7)

It is standard to supress the . and only write cv instead of c.v
the function + and . are required to statify the following rules:

Example

- $`v_1 + v_2 = v_2 + v1`$  for all $`v_1, v_2  \in V`$

### Linear combinations of vectors

Let V be a vector space and $`v_1, v_2 ,..., v_n \in V`$. The linear combination of $`v_1, v_2, ... v_n`$ with coefficient $`a_1, a_2, ..., a_n \in R`$ is the vector $`\sum_{i=1}{n} a_i v_i \in V`$

A vector $`v \in V`$ in a linear combination of $`v_1, v_2 ,..., v_n`$ if there exist some $`a_1, a_2, ... ,a_n \in R`$ that $`v = \sum_{i=1}^n a_i v_i`$

#### Linear dependence

A set of vectors $`v_1, v_2, ... , v_n`$ from a vector spacce V is said to be linearly dependent, if exist scalars $`a_1, a_2, ..., a_n`$ not all space such that
$`a_1v_1 + a_2v_2 + ... + a_n v_n = 0`$

Equivalent, the 0 vector is a linear combination of $`v_1, v_2, ..., v_n`$ with non-zero coefficients.

Example :
Consider the followinf vectors in $`\R^3`$ (2,3,7) and ($`\frac{5}{3}, \frac{5}{2} , \frac{35}{6}`$)
It is easy to check that 5(2,3,7) - 6($`\frac{5}{3}, \frac{5}{2} , \frac{35}{6}`$) = (0,0,0)
Hence these two vectors are linearly independent, Also observer that one is scalar multiple of the other.

> If a set is linearly dependent, then so is every superset of it.

TO check $`v_1, v_2, v_3 ... v_n \in \R^m`$ are linearly independent, we have to check that the homogenous system of linear equation Vx =0 has only the trivial solution, where the $`j^{th}`$ column of V id $`v_j`$

### more than n vectors in R

any set of r vectors in $`R^n`$ with r> n are linearly dependent.

## Realtionaship with determinant

To check whether a set of n vectors in $`R^n`$ are linearly independent. we have to finf solution of homogeneous system Vx = 0
Where V is an $`n \times n`$ matrix obtained by arrainging the vectors in columns.
Since V is sqaure matrix, it has unique solution x=0 if an only if V is invertible  if an donly if det(A) $`\neq`$ 0

- If A is invertible then there exists $`A^{-1}`$ such that $`AA^{-1} = I = A^{-1}A`$. hence det(A).det($`A^{-1}`$)  =1 which implies det(A) $`\neq`$
- Now if det(A) $`\neq`$ 0 then $`A^{-1} = \frac{1}{det(A)} adj(A)`$ exits
![Alt text](./img/example-linear-independent.png)

## Span of a set of vectors

The span of a set S (of vectors ) is defined as the of all finite linear cobination of elements (vectors) of S, and denoted by _Span(S)_

Span(S) = $`\sum_{i=1}^n a_i v_i \in V | a_1, a_2, ..., a_n \in \R`$
Let S = {(1,0)} $`\subset \R^2`$. then Span(S) = {a(1,0) | $`a \in \R`$} = $`(a,o)|a \in \R`$
Thus, Span(S) is the X-axis in $`\R^2`$

### Spanning set of vector space

Let V be a vector space. A set S $`\subseteqq`$ V is a spanning set for V if Span(S) = V

Example

- If S = {(1,0), (0,1)} the San(S) = $`R^2`$
- If S = {(1,0), (0,1),(1,2)}, then Span(S) = $`R^2`$
- If S = {(1,1), (0,1)} then Sapan(S) = $`R^2`$
- If S = {(1,0,0),(0,1,0),(0,0,1)} then Span(S) = R^3

**Adding vectors to obtain a spanning set for $`\R^3`$ .**
we will start to build a spanning set for the vector space $`\R^3`$.
Start with $`S_0`$ to be the empty set $`\emptyset`$. then Span($`S_0`$) = Span($`\emptyset`$) = {(0,0,0)}
Since this not the full vector space,append a vector outside Span($`S_0`$) in $`\R^3`$ e.g. (0,2,1) to $`S_0`$ and call the new set $`S_1`$
So, $`S_1 = S_0 \cup  \{(0,2,1)\}`$
choose a vector from outside the Span(S) and append it to S_2 call the new set $`S_3`$. 

### Basis 
A basis B of a vector space V is linearly indpendent subsets of V that spans V.
- B is linearly independent and Span(B) = V
- B is  maximal linearly indpendent set.
- B is a minimal spanning set.

Equivalent : A basis of B of a vector space V is a subset B $`\subseteqq`$ V such that the every element of V can be uniquely written as a linear combination of elements of B.

I.e. if B = {$`v_1, v_2 ,,, v_n`$} then for every $`v \in V`$, there is a unique set of scalars $`a_1, a_2, ... a_n \in \R`$ such that $`v= \sum_{i=1}^n a_iv_i`$


## Rank/Dimension of vector space
The dimension (or rank) of a vector space is the size(or cardinality) of a basis of the vector space.
for this course, if B is basis of V, then the rank is the number of elements in B.
For every vector space there exists a basis, and all bases of a vector space have the same number of elements (or cardinality)
hence, the dimension (or rank) of a vector space(say V) is suniquely defined and denoted by _dim(V) or rank(V)_ respectively.

The $`i^{th}`$ standard basis of vector in $`\R^n`$ $`e_i =(0,0,0,0,...1, ...0)`$
recall that the set {$`e_1, e_2 ... e_n`}$ is basis of $`\R^n`$ called the standard basis. Hence the dimension of $`\R^n`$ is n.

## rank of a matrix
let A be an $`m \times n`$ matrix.
- the column space of A is the subspace of $`R^n`$ spanned by the column vector of A.
- the row space of A is the subspace of $`R^n`$ spanned by the row vector of A.
- the dimension of the column space A is defined as column rank of A.
- The dimension of row space is defined as the row rank of A.
- fact; Column rank = Row rank and this number is called rank of A.




