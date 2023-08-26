vectors 


# Matrices
A matrix is a rectangular array of number, arranged in rows and columns.
Example : [ [ 1,2,3 ], [ 2,3,4 ] ]
This is a $`2 \times 3`$ (2 rows and 3 columns)
- An $`m \times n`$ has m rows and n columns
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

