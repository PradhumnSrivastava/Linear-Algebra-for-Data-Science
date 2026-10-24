# Linear Algebra Mathematical Foundations

## 1. Number Systems

Number systems are the foundation of mathematics and linear algebra.

### 1.1 Natural Numbers

Natural numbers are used for counting.

$$
\mathbb{N} = \{1,2,3,4,\ldots\}
$$

Some conventions include zero in the natural numbers:

$$
\mathbb{N}_0 = \{0,1,2,3,\ldots\}
$$

### 1.2 Integers

Integers include negative numbers, zero, and positive numbers.

$$
\mathbb{Z} = \{\ldots,-3,-2,-1,0,1,2,3,\ldots\}
$$

### 1.3 Rational Numbers

A rational number can be expressed as a ratio of two integers, where the denominator is nonzero.

$$
\mathbb{Q} =
\left\{
\frac{p}{q}
\;\middle|\;
p,q\in\mathbb{Z},\ q\neq 0
\right\}
$$

Examples:

$$
\frac{1}{2},\quad -\frac{3}{4},\quad 5
$$

### 1.4 Irrational Numbers

Irrational numbers cannot be expressed as a ratio of two integers.

Examples:

$$
\sqrt{2},\quad \pi,\quad e
$$

### 1.5 Real Numbers

Real numbers include rational and irrational numbers.

$$
\mathbb{R} = \mathbb{Q}\cup
(\text{irrational numbers})
$$

Real numbers are used extensively in standard real-valued linear algebra.

### 1.6 Complex Numbers

A complex number has the form:

$$
z=a+bi
$$

where:

* $a$ is the real part.
* $b$ is the imaginary part.
* $i$ is the imaginary unit.

$$
i^2=-1
$$

The set of complex numbers is denoted by $\mathbb{C}$.

### 1.7 Relationship Between Number Systems

The standard inclusion relationships are:

$$
\mathbb{N}\subseteq\mathbb{Z}
\subseteq\mathbb{Q}
\subseteq\mathbb{R}
\subseteq\mathbb{C}
$$

These relationships assume $\mathbb{N}={1,2,3,\ldots}$.

---

## 2. Basic Algebra

Algebra uses symbols to represent numbers and mathematical quantities.

### 2.1 Variables

A variable represents a mathematical quantity.

Example:

$$
x+5=12
$$

Solving for $x$:

$$
x=12-5
$$

$$
\boxed{x=7}
$$

### 2.2 Algebraic Expressions

An algebraic expression combines variables, constants, and operations.

Example:

$$
3x^2+2x-5
$$

Here:

* $3$ is the coefficient of $x^2$.
* $2$ is the coefficient of $x$.
* $-5$ is the constant term.

### 2.3 Algebraic Identities

Square of a sum:

$$
(a+b)^2=a^2+2ab+b^2
$$

Square of a difference:

$$
(a-b)^2=a^2-2ab+b^2
$$

Difference of squares:

$$
a^2-b^2=(a-b)(a+b)
$$

Product of two binomials:

$$
(a+b)(c+d)=ac+ad+bc+bd
$$

These identities are useful when simplifying mathematical expressions and deriving formulas.

---

## 3. Equations and Inequalities

### 3.1 Linear Equations

A linear equation in one variable has the form:

$$
ax+b=0
$$

where $a,b\in\mathbb{R}$ and $a\neq 0$.

Its solution is:

$$
\boxed{x=-\frac{b}{a}}
$$

### 3.2 Linear Equations in Multiple Variables

A linear equation in two variables can be written as:

$$
ax+by=c
$$

A system of two linear equations is:

$$
a_1x+b_1y=c_1
$$

$$
a_2x+b_2y=c_2
$$

Systems like these can be represented using matrices:

$$
\begin{bmatrix}
a_1 & b_1\\
a_2 & b_2
\end{bmatrix}
\begin{bmatrix}
x\\
y
\end{bmatrix}
=
\begin{bmatrix}
c_1\\
c_2
\end{bmatrix}
$$

This is an important connection between algebra and linear algebra.

### 3.3 Inequalities

Examples:

$$
x>2
$$

$$
x\leq 5
$$

An inequality describes a range of possible values rather than necessarily one exact value.

---

## 4. Exponents and Radicals

### 4.1 Exponent Rules

For appropriate nonzero values of $a$:

$$
a^m a^n=a^{m+n}
$$

$$
\frac{a^m}{a^n}=a^{m-n}
$$

$$
(a^m)^n=a^{mn}
$$

$$
(ab)^n=a^n b^n
$$

$$
a^0=1
$$

$$
a^{-n}=\frac{1}{a^n}
$$

### 4.2 Fractional Exponents

For suitable real values:

$$
a^{1/n}=\sqrt[n]{a}
$$

$$
a^{m/n}=\sqrt[n]{a^m}
$$

### 4.3 Euclidean Norm Connection

For a vector:

$$
\mathbf{x}=
\begin{bmatrix}
x_1\\
x_2\\
\vdots\\
x_n
\end{bmatrix}
$$

its Euclidean norm is:

$$
\|\mathbf{x}\|_2=
\sqrt{x_1^2+x_2^2+\cdots+x_n^2}
$$

This formula uses the Pythagorean principle in higher dimensions.

---

## 5. Summation Notation

Summation notation provides a compact way to represent repeated addition.

### 5.1 Basic Definition

$$
\sum_{i=1}^{n}x_i
=
x_1+x_2+\cdots+x_n
$$

Here:

* $\sum$ denotes summation.
* $i$ is the index.
* $1$ is the lower limit.
* $n$ is the upper limit.
* $x_i$ is the term being added.

### 5.2 Example

$$
\sum_{i=1}^{4}i
=1+2+3+4=10
$$

### 5.3 Sum of the First $n$ Integers

$$
\sum_{i=1}^{n}i=\frac{n(n+1)}{2}
$$

### 5.4 Sum of Squares

$$
\sum_{i=1}^{n}i^2
=\frac{n(n+1)(2n+1)}{6}
$$

### 5.5 Sum of a Constant

$$
\sum_{i=1}^{n}c=nc
$$

### 5.6 Linearity of Summation

$$
\sum_{i=1}^{n}(x_i+y_i)
=
\sum_{i=1}^{n}x_i+
\sum_{i=1}^{n}y_i
$$

For a constant $c$:

$$
\sum_{i=1}^{n}cx_i
=
c\sum_{i=1}^{n}x_i
$$

Summation notation appears frequently in matrix operations, statistics, optimization, and machine learning.

---

## 6. Functions and Mappings

### 6.1 Definition

A function maps each element of a domain to exactly one element of a codomain.

$$
f:A\rightarrow B
$$

Here:

* $A$ is the domain.
* $B$ is the codomain.
* $f$ is the mapping.

### 6.2 Example

Consider:

$$
f(x)=2x+3
$$

For $x=4$:

$$
f(4)=2(4)+3=11
$$

### 6.3 Domain and Range

The domain contains the allowed inputs.

The range contains the outputs that the function actually produces.

### 6.4 Linear Functions Versus Linear Transformations

A scalar-valued function such as:

$$
f(x)=2x+3
$$

is not a linear transformation because it does not satisfy $f(0)=0$.

A linear transformation $T$ must satisfy both:

**Additivity**

$$
T(\mathbf{u}+\mathbf{v})
=
T(\mathbf{u})+T(\mathbf{v})
$$

**Homogeneity**

$$
T(c\mathbf{u})=cT(\mathbf{u})
$$

for all vectors $\mathbf{u},\mathbf{v}$ and scalars $c$ in the relevant vector space.

A transformation satisfying both properties is linear.

---

## 7. Sets and Set Operations

### 7.1 Set Definition

A set is a collection of distinct elements.

Example:

$$
A=\{1,2,3,4\}
$$

### 7.2 Union

The union contains elements belonging to either set.

$$
A\cup B
$$

### 7.3 Intersection

The intersection contains elements common to both sets.

$$
A\cap B
$$

### 7.4 Difference

The set difference contains elements in $A$ that are not in $B$.

$$
A\setminus B
$$

### 7.5 Cartesian Product

The Cartesian product of two sets is:

$$
A\times B=
\{(a,b)\mid a\in A,\ b\in B\}
$$

For example, if:

$$
A=\{1,2\},\qquad B=\{a,b\}
$$

then:

$$
A\times B=
\{(1,a),(1,b),(2,a),(2,b)\}
$$

Cartesian products are useful when defining coordinate spaces such as $\mathbb{R}^2$ and $\mathbb{R}^3$.

---

## 8. Mathematical Logic

### 8.1 Propositions

A proposition is a statement that is either true or false.

Example:

$$
2+3=5
$$

This proposition is true.

### 8.2 Logical Operators

Negation:

$$
\neg P
$$

Conjunction:

$$
P\land Q
$$

Disjunction:

$$
P\lor Q
$$

Implication:

$$
P\Rightarrow Q
$$

Equivalence:

$$
P\Leftrightarrow Q
$$

### 8.3 Necessary and Sufficient Conditions

The statement:

$$
P\Rightarrow Q
$$

means that $P$ is sufficient for $Q$, and $Q$ is necessary for $P$.

The statement:

$$
P\Leftrightarrow Q
$$

means both implications hold.

Mathematical theorems often use necessary and sufficient conditions to characterize concepts such as matrix invertibility.

---

## 9. Mathematical Proofs

### 9.1 Direct Proof

A direct proof starts with assumptions and logically derives the conclusion.

### 9.2 Proof by Contradiction

Assume the opposite of the desired conclusion and derive a contradiction.

### 9.3 Proof by Contrapositive

Instead of proving:

$$
P\Rightarrow Q
$$

prove the logically equivalent statement:

$$
\neg Q\Rightarrow\neg P
$$

### 9.4 Mathematical Induction

Mathematical induction is used to prove statements about positive integers.

**Step 1 — Base Case**

Verify that the statement holds for the initial value.

**Step 2 — Inductive Hypothesis**

Assume the statement holds for $n=k$.

**Step 3 — Inductive Step**

Use the assumption to prove that it holds for $n=k+1$.

For example, to prove:

$$
\sum_{i=1}^{n}i=\frac{n(n+1)}{2}
$$

assume:

$$
\sum_{i=1}^{k}i=\frac{k(k+1)}{2}
$$

Then:

$$
\begin{aligned}
\sum_{i=1}^{k+1}i
&=\frac{k(k+1)}{2}+(k+1)\\
&=\frac{k(k+1)+2(k+1)}{2}\\
&=\frac{(k+1)(k+2)}{2}
\end{aligned}
$$

This establishes the inductive step.

---

## 10. Why These Foundations Matter

| Mathematical concept | Application                                     |
| -------------------- | ----------------------------------------------- |
| Number systems       | Defining vector and matrix entries              |
| Algebra              | Simplifying equations and deriving formulas     |
| Equations            | Solving systems of linear equations             |
| Exponents            | Powers, scaling, and numerical calculations     |
| Summation notation   | Dot products, statistics, and loss functions    |
| Functions            | Understanding linear transformations            |
| Sets                 | Defining vector spaces and domains              |
| Logic                | Understanding mathematical theorems             |
| Proofs               | Establishing mathematical properties rigorously |

## Final Summary

Before moving to advanced Linear Algebra, make sure you can:

* Manipulate algebraic expressions confidently.
* Solve linear equations.
* Understand functions and mappings.
* Work with summation notation.
* Distinguish scalar quantities from vectors and matrices.
* Understand basic logical statements and mathematical proofs.

**Next topic:** Scalars, Vectors and Geometry.
