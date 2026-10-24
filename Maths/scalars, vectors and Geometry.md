# 02. Scalars, Vectors and Geometry

## Table of Contents

1. [[#2.1 Scalars and Vectors]]
2. [[#2.2 Vector Notation]]
3. [[#2.3 Vector Representation]]
4. [[#2.4 Vector Addition and Subtraction]]
5. [[#2.5 Scalar Multiplication]]
6. [[#2.6 Linear Combinations]]
7. [[#2.7 Dot Product]]
8. [[#2.8 Vector Norms and Magnitude]]
9. [[#2.9 Distance Between Vectors]]
10. [[#2.10 Angles Between Vectors]]
11. [[#2.11 Orthogonal Vectors]]
12. [[#2.12 Cross Product]]
13. [[#2.13 Projection of Vectors]]
14. [[#2.14 Vector Geometry]]
15. [[#Summary]]
16. [[#Practice Questions]]

---

# 2.1 Scalars and Vectors

## 2.1.1 What Is a Scalar?

A scalar is a single numerical quantity that represents magnitude without requiring a direction.

Examples:

* Temperature: $25^\circ C$
* Mass: $70\text{ kg}$
* Distance: $10\text{ m}$
* Learning rate: $0.001$
* Loss value: $0.25$

Mathematically, a real scalar belongs to the set:

$$
c\in\mathbb{R}
$$

A scalar may also be complex in complex-valued linear algebra:

$$
c\in\mathbb{C}
$$

## 2.1.2 What Is a Vector?

A vector is a mathematical object whose components describe a quantity in a vector space.

In elementary geometry, a vector can represent both magnitude and direction.

A vector in $n$-dimensional real space can be written as:

$$
\mathbf{v}=
\begin{bmatrix}
v_1\\
v_2\\
\vdots\\
v_n
\end{bmatrix}
\in\mathbb{R}^n
$$

Here:

* $\mathbf{v}$ is the vector.
* $v_i$ is its $i$-th component.
* $n$ is the number of components.

Example:

$$
\mathbf{v}=
\begin{bmatrix}
3\\
4
\end{bmatrix}
$$

This vector has two components and belongs to $\mathbb{R}^2$.

Its magnitude is:

$$
\|\mathbf{v}\|_2=\sqrt{3^2+4^2}=5
$$

## 2.1.3 Scalar vs Vector

| Property                    | Scalar            | Vector                                                   |
| --------------------------- | ----------------- | -------------------------------------------------------- |
| Mathematical representation | Single value      | Ordered components                                       |
| Example                     | $5$               | $\begin{bmatrix}3\4\end{bmatrix}$                        |
| Dimension                   | Scalar quantity   | $n$ components in $\mathbb{R}^n$                         |
| Multiplication              | Scalar arithmetic | Scalar multiplication, dot product, and other operations |
| ML example                  | Learning rate     | Feature vector                                           |

## 2.1.4 Why Vectors Matter in AI

Suppose a student has three features:

* Study hours = $5$
* Attendance percentage = $80$
* Assignment score = $90$

The feature vector can be represented as:

$$
\mathbf{x}=
\begin{bmatrix}
5\\
80\\
90
\end{bmatrix}
$$

A machine-learning model can use this vector as an input.

In a real application, features may need normalization or standardization because their scales differ.

---

# 2.2 Vector Notation

Vectors can be represented using different mathematical notations.

## 2.2.1 Bold Notation

$$
\mathbf{v}=
\begin{bmatrix}
2\\
5\\
7
\end{bmatrix}
$$

The bold symbol $\mathbf{v}$ indicates that the quantity is a vector.

## 2.2.2 Component Notation

The same vector can be written as:

$$
\mathbf{v}=(2,5,7)
$$

This notation is common when listing components.

## 2.2.3 Unit Vector Notation

In three-dimensional Cartesian coordinates, the standard unit vectors are:

$$
\mathbf{i}=
\begin{bmatrix}
1\\0\\0
\end{bmatrix},
\qquad
\mathbf{j}=
\begin{bmatrix}
0\\1\\0
\end{bmatrix},
\qquad
\mathbf{k}=
\begin{bmatrix}
0\\0\\1
\end{bmatrix}
$$

Any vector $\mathbf{v}=(a,b,c)$ can be expressed as:

$$
\mathbf{v}=a\mathbf{i}+b\mathbf{j}+c\mathbf{k}
$$

For example:

$$
\mathbf{v}=
\begin{bmatrix}
2\\3\\4
\end{bmatrix}
=2\mathbf{i}+3\mathbf{j}+4\mathbf{k}
$$

## 2.2.4 Index Notation

For a vector with $n$ components:

$$
\mathbf{x}=(x_1,x_2,\ldots,x_n)
$$

The symbol $x_i$ denotes the $i$-th component.

For example:

$$
\mathbf{x}=(4,7,9)
$$

Then:

$$
x_1=4,\qquad x_2=7,\qquad x_3=9
$$

## 2.2.5 Row and Column Vectors

A row vector has one row:

$$
\mathbf{x}^{T}=
\begin{bmatrix}
2&4&6
\end{bmatrix}
$$

A column vector has one column:

$$
\mathbf{x}=
\begin{bmatrix}
2\\4\\6
\end{bmatrix}
$$

The transpose converts a column vector into a row vector and vice versa.

If:

$$
\mathbf{x}=
\begin{bmatrix}
2\\4\\6
\end{bmatrix}
$$

then:

$$
\mathbf{x}^{T}=
\begin{bmatrix}
2&4&6
\end{bmatrix}
$$

The superscript $T$ denotes transpose, not exponentiation.

---

# 2.3 Vector Representation

## 2.3.1 Geometric Representation

In two dimensions, a vector can be represented by an arrow from the origin to a point.

For:

$$
\mathbf{v}=
\begin{bmatrix}
3\\2
\end{bmatrix}
$$

the vector starts at $(0,0)$ and ends at $(3,2)$.

The horizontal displacement is $3$, and the vertical displacement is $2$.

## 2.3.2 Vector in Two Dimensions

$$
\mathbf{v}=
\begin{bmatrix}
x\\y
\end{bmatrix}
$$

Its magnitude is:

$$
\|\mathbf{v}\|_2=\sqrt{x^2+y^2}
$$

Its direction angle, measured from the positive $x$-axis, is:

$$
\theta=\operatorname{atan2}(y,x)
$$

The function $\operatorname{atan2}$ accounts for the correct quadrant.

## 2.3.3 Vector in Three Dimensions

$$
\mathbf{v}=
\begin{bmatrix}
x\\y\\z
\end{bmatrix}
$$

Its magnitude is:

$$
\|\mathbf{v}\|_2=\sqrt{x^2+y^2+z^2}
$$

Three-dimensional vectors are useful in physics, computer graphics, robotics and spatial data analysis.

## 2.3.4 Position Vector

A position vector describes the position of a point relative to the origin.

If a point is:

$$
P=(x,y,z)
$$

then its position vector is:

$$
\overrightarrow{OP}=
\begin{bmatrix}
x\\y\\z
\end{bmatrix}
$$

## 2.3.5 Vector Between Two Points

Suppose:

$$
A=(x_1,y_1)
$$

and:

$$
B=(x_2,y_2)
$$

The vector from $A$ to $B$ is:

$$
\overrightarrow{AB}=
\begin{bmatrix}
x_2-x_1\\
y_2-y_1
\end{bmatrix}
$$

Example:

$$
A=(1,2),\qquad B=(4,6)
$$

Therefore:

$$
\overrightarrow{AB}=
\begin{bmatrix}
4-1\\
6-2
\end{bmatrix}
=
\begin{bmatrix}
3\\4
\end{bmatrix}
$$

---

# 2.4 Vector Addition and Subtraction

## 2.4.1 Vector Addition

Two vectors of the same dimension can be added component-wise.

Let:

$$
\mathbf{a}=
\begin{bmatrix}
a_1\\a_2\\\vdots\\a_n
\end{bmatrix}
$$

and:

$$
\mathbf{b}=
\begin{bmatrix}
b_1\\b_2\\\vdots\\b_n
\end{bmatrix}
$$

Then:

$$
\mathbf{a}+\mathbf{b}=
\begin{bmatrix}
a_1+b_1\\
a_2+b_2\\
\vdots\\
a_n+b_n
\end{bmatrix}
$$

### Example

$$
\mathbf{a}=
\begin{bmatrix}
2\\3
\end{bmatrix},
\qquad
\mathbf{b}=
\begin{bmatrix}
4\\5
\end{bmatrix}
$$

Therefore:

$$
\mathbf{a}+\mathbf{b}
=
\begin{bmatrix}
2+4\\
3+5
\end{bmatrix}
=
\begin{bmatrix}
6\\8
\end{bmatrix}
$$

## 2.4.2 Properties of Vector Addition

### Commutative Property

$$
\mathbf{a}+\mathbf{b}=\mathbf{b}+\mathbf{a}
$$

### Associative Property

$$
(\mathbf{a}+\mathbf{b})+\mathbf{c}
=
\mathbf{a}+(\mathbf{b}+\mathbf{c})
$$

### Additive Identity

$$
\mathbf{a}+\mathbf{0}=\mathbf{a}
$$

### Additive Inverse

$$
\mathbf{a}+(-\mathbf{a})=\mathbf{0}
$$

## 2.4.3 Vector Subtraction

Vector subtraction is defined as addition of the negative vector.

$$
\mathbf{a}-\mathbf{b}
=
\mathbf{a}+(-\mathbf{b})
$$

Component-wise:

$$
\mathbf{a}-\mathbf{b}
=
\begin{bmatrix}
a_1-b_1\\
a_2-b_2\\
\vdots\\
a_n-b_n
\end{bmatrix}
$$

### Example

$$
\mathbf{a}=
\begin{bmatrix}
7\\9
\end{bmatrix},
\qquad
\mathbf{b}=
\begin{bmatrix}
2\\4
\end{bmatrix}
$$

Then:

$$
\mathbf{a}-\mathbf{b}
=
\begin{bmatrix}
7-2\\
9-4
\end{bmatrix}
=
\begin{bmatrix}
5\\5
\end{bmatrix}
$$

## 2.4.4 Geometric Interpretation

Vector addition can be interpreted using the triangle rule or parallelogram rule.

Vector subtraction represents the displacement from the endpoint of one vector to the endpoint of another when their tails are placed at the same origin.

---

# 2.5 Scalar Multiplication

Scalar multiplication means multiplying every component of a vector by the same scalar.

For scalar $c\in\mathbb{R}$ and vector $\mathbf{v}\in\mathbb{R}^n$:

$$
c\mathbf{v}=
\begin{bmatrix}
cv_1\\
cv_2\\
\vdots\\
cv_n
\end{bmatrix}
$$

### Example

Let:

$$
\mathbf{v}=
\begin{bmatrix}
2\\3
\end{bmatrix}
$$

and $c=4$.

Then:

$$
4\mathbf{v}
=
4\begin{bmatrix}
2\\3
\end{bmatrix}
=
\begin{bmatrix}
8\\12
\end{bmatrix}
$$

## 2.5.1 Geometric Meaning

For a nonzero vector $\mathbf{v}$:

* If $c>1$, its magnitude increases.
* If $0<c<1$, its magnitude decreases.
* If $c<0$, its direction reverses.
* If $c=0$, the result is the zero vector.

The magnitude obeys:

$$
\|c\mathbf{v}\|_2=|c|\|\mathbf{v}\|_2
$$

The absolute value is important because magnitudes cannot be negative.

## 2.5.2 Properties

Distributivity over vector addition:

$$
c(\mathbf{u}+\mathbf{v})
=
c\mathbf{u}+c\mathbf{v}
$$

Distributivity over scalar addition:

$$
(c+d)\mathbf{v}
=
c\mathbf{v}+d\mathbf{v}
$$

Associativity of scalar multiplication:

$$
c(d\mathbf{v})=(cd)\mathbf{v}
$$

Identity:

$$
1\mathbf{v}=\mathbf{v}
$$

---

# 2.6 Linear Combinations

## 2.6.1 Definition

A linear combination of vectors is a sum of scalar multiples of those vectors.

For vectors $\mathbf{v}_1,\mathbf{v}_2,\ldots,\mathbf{v}_k$ and scalars $c_1,c_2,\ldots,c_k$:

$$
\mathbf{u}=
c_1\mathbf{v}_1+
c_2\mathbf{v}_2+
\cdots+
c_k\mathbf{v}_k
$$

The scalars $c_i$ are called coefficients.

## 2.6.2 Example

Let:

$$
\mathbf{v}_1=
\begin{bmatrix}
1\\2
\end{bmatrix},
\qquad
\mathbf{v}_2=
\begin{bmatrix}
3\\1
\end{bmatrix}
$$

Find:

$$
\mathbf{u}=2\mathbf{v}_1+3\mathbf{v}_2
$$

Substitute:

$$
\mathbf{u}
=
2\begin{bmatrix}
1\\2
\end{bmatrix}
+
3\begin{bmatrix}
3\\1
\end{bmatrix}
$$

Apply scalar multiplication:

$$
\mathbf{u}
=
\begin{bmatrix}
2\\4
\end{bmatrix}
+
\begin{bmatrix}
9\\3
\end{bmatrix}
$$

Therefore:

$$
\boxed{
\mathbf{u}=
\begin{bmatrix}
11\\7
\end{bmatrix}
}
$$

## 2.6.3 Linear Combinations in Matrix Form

Place the vectors into the columns of a matrix:

$$
A=
\begin{bmatrix}
|&|&&|\\
\mathbf{v}_1&\mathbf{v}_2&\cdots&\mathbf{v}_k\\
|&|&&|
\end{bmatrix}
$$

Let the coefficient vector be:

$$
\mathbf{c}=
\begin{bmatrix}
c_1\\c_2\\\vdots\\c_k
\end{bmatrix}
$$

Then:

$$
\boxed{\mathbf{u}=A\mathbf{c}}
$$

This equation is fundamental to linear algebra.

## 2.6.4 Span

The span of a set of vectors is the collection of all their possible linear combinations.

$$
\operatorname{span}
\{\mathbf{v}_1,\ldots,\mathbf{v}_k\}
=
\left\{
\sum_{i=1}^{k}c_i\mathbf{v}_i
\;\middle|\;
c_i\in\mathbb{R}
\right\}
$$

The span can form a line, a plane, or a higher-dimensional subspace.

---

# 2.7 Dot Product

## 2.7.1 Definition

The dot product, also called the Euclidean inner product, takes two vectors of the same dimension and produces a scalar.

For:

$$
\mathbf{a}=
\begin{bmatrix}
a_1\\a_2\\\vdots\\a_n
\end{bmatrix},
\qquad
\mathbf{b}=
\begin{bmatrix}
b_1\\b_2\\\vdots\\b_n
\end{bmatrix}
$$

their dot product is:

$$
\boxed{
\mathbf{a}\cdot\mathbf{b}
=
\sum_{i=1}^{n}a_i b_i
}
$$

Expanded form:

$$
\mathbf{a}\cdot\mathbf{b}
=
a_1b_1+a_2b_2+\cdots+a_nb_n
$$

## 2.7.2 Numerical Example

Let:

$$
\mathbf{a}=
\begin{bmatrix}
2\\3\\4
\end{bmatrix},
\qquad
\mathbf{b}=
\begin{bmatrix}
5\\1\\2
\end{bmatrix}
$$

Then:

$$
\begin{aligned}
\mathbf{a}\cdot\mathbf{b}
&=2(5)+3(1)+4(2)\\
&=10+3+8\\
&=\boxed{21}
\end{aligned}
$$

## 2.7.3 Geometric Formula

For nonzero vectors $\mathbf{a}$ and $\mathbf{b}$:

$$
\boxed{
\mathbf{a}\cdot\mathbf{b}
=
\|\mathbf{a}\|_2
\|\mathbf{b}\|_2
\cos\theta
}
$$

where $\theta$ is the angle between the vectors.

Rearranging:

$$
\cos\theta=
\frac{\mathbf{a}\cdot\mathbf{b}}
{\|\mathbf{a}\|_2\|\mathbf{b}\|_2}
$$

This formula connects algebraic operations to geometry.

## 2.7.4 Properties of the Dot Product

Commutativity:

$$
\mathbf{a}\cdot\mathbf{b}
=
\mathbf{b}\cdot\mathbf{a}
$$

Distributivity:

$$
\mathbf{a}\cdot(\mathbf{b}+\mathbf{c})
=
\mathbf{a}\cdot\mathbf{b}
+
\mathbf{a}\cdot\mathbf{c}
$$

Scalar multiplication:

$$
(c\mathbf{a})\cdot\mathbf{b}
=
c(\mathbf{a}\cdot\mathbf{b})
$$

Dot product with itself:

$$
\mathbf{a}\cdot\mathbf{a}
=
\|\mathbf{a}\|_2^2
$$

For a real vector:

$$
\mathbf{a}\cdot\mathbf{a}
=
\sum_{i=1}^{n}a_i^2
\geq 0
$$

Equality holds exactly when $\mathbf{a}=\mathbf{0}$.

## 2.7.5 Dot Product in Machine Learning

The output of a linear model can be represented as:

$$
\hat{y}=\mathbf{w}^{T}\mathbf{x}+b
$$

where:

* $\mathbf{x}$ is the feature vector.
* $\mathbf{w}$ is the weight vector.
* $b$ is the bias.
* $\hat{y}$ is the prediction.

For a single output, $\mathbf{w}^{T}\mathbf{x}$ is a dot product.

Dot products also appear in cosine similarity, embedding search and Transformer attention.

---

# 2.8 Vector Norms and Magnitude

## 2.8.1 What Is a Norm?

A norm measures the size or magnitude of a vector.

It is written as:

$$
\|\mathbf{x}\|
$$

A mathematical norm satisfies:

1. Non-negativity and definiteness.
2. Absolute homogeneity.
3. Triangle inequality.

Formally:

$$
\|\mathbf{x}\|\geq 0
$$

and:

$$
\|\mathbf{x}\|=0
\iff
\mathbf{x}=\mathbf{0}
$$

For any scalar $c$:

$$
\|c\mathbf{x}\|=|c|\|\mathbf{x}\|
$$

Triangle inequality:

$$
\|\mathbf{x}+\mathbf{y}\|
\leq
\|\mathbf{x}\|+\|\mathbf{y}\|
$$

## 2.8.2 L2 Norm

The Euclidean norm is:

$$
\boxed{
\|\mathbf{x}\|_2
=
\sqrt{\sum_{i=1}^{n}x_i^2}
}
$$

Example:

$$
\mathbf{x}=
\begin{bmatrix}
3\\4
\end{bmatrix}
$$

Then:

$$
\|\mathbf{x}\|_2
=
\sqrt{3^2+4^2}
=
\sqrt{25}
=
5
$$

## 2.8.3 L1 Norm

The L1 norm is:

$$
\boxed{
\|\mathbf{x}\|_1
=
\sum_{i=1}^{n}|x_i|
}
$$

For $\mathbf{x}=(3,-4)$:

$$
\|\mathbf{x}\|_1=|3|+|-4|=7
$$

## 2.8.4 L-infinity Norm

The infinity norm is:

$$
\boxed{
\|\mathbf{x}\|_\infty
=
\max_i|x_i|
}
$$

For $\mathbf{x}=(3,-4,2)$:

$$
\|\mathbf{x}\|_\infty=4
$$

## 2.8.5 General Lp Norm

For $p\geq 1$:

$$
\boxed{
\|\mathbf{x}\|_p
=
\left(\sum_{i=1}^{n}|x_i|^p\right)^{1/p}
}
$$

The L1 and L2 norms are common examples. The infinity norm is defined separately as the limit of the Lp norms as $p\to\infty$.

## 2.8.6 Unit Vector

A unit vector has norm equal to one.

For a nonzero vector $\mathbf{x}$:

$$
\boxed{
\hat{\mathbf{x}}
=
\frac{\mathbf{x}}{\|\mathbf{x}\|_2}
}
$$

Example:

$$
\mathbf{x}=
\begin{bmatrix}
3\\4
\end{bmatrix}
$$

Since $|\mathbf{x}|_2=5$:

$$
\hat{\mathbf{x}}
=
\begin{bmatrix}
3/5\\4/5
\end{bmatrix}
$$

Verification:

$$
\|\hat{\mathbf{x}}\|_2
=
\sqrt{\frac{9}{25}+\frac{16}{25}}
=1
$$

The zero vector cannot be normalized because its norm is zero.

## 2.8.7 Norms in AI and Machine Learning

| Norm            | Common use                                            |
| --------------- | ----------------------------------------------------- |
| L1 norm         | Sparse regularization and Manhattan distance          |
| L2 norm         | Euclidean distance, weight decay and vector magnitude |
| L-infinity norm | Maximum component deviation                           |
| General Lp norm | Mathematical analysis and distance measures           |

The L1 and L2 penalties used in optimization are typically defined through these norms or their squares.

---

# 2.9 Distance Between Vectors

## 2.9.1 Euclidean Distance

The Euclidean distance between vectors $\mathbf{x}$ and $\mathbf{y}$ is the norm of their difference.

$$
\boxed{
d_2(\mathbf{x},\mathbf{y})
=
\|\mathbf{x}-\mathbf{y}\|_2
}
$$

Expanded form:

$$
d_2(\mathbf{x},\mathbf{y})
=
\sqrt{\sum_{i=1}^{n}(x_i-y_i)^2}
$$

## 2.9.2 Example

Let:

$$
\mathbf{x}=
\begin{bmatrix}
1\\2
\end{bmatrix},
\qquad
\mathbf{y}=
\begin{bmatrix}
4\\6
\end{bmatrix}
$$

Their difference is:

$$
\mathbf{x}-\mathbf{y}
=
\begin{bmatrix}
-3\\-4
\end{bmatrix}
$$

Therefore:

$$
\begin{aligned}
d_2(\mathbf{x},\mathbf{y})
&=\sqrt{(-3)^2+(-4)^2}\\
&=\sqrt{9+16}\\
&=\boxed{5}
\end{aligned}
$$

## 2.9.3 Manhattan Distance

The Manhattan distance is:

$$
\boxed{
d_1(\mathbf{x},\mathbf{y})
=
\sum_{i=1}^{n}|x_i-y_i|
}
$$

For the previous vectors:

$$
d_1(\mathbf{x},\mathbf{y})
=
|1-4|+|2-6|
=7
$$

## 2.9.4 General Minkowski Distance

For $p\geq 1$:

$$
d_p(\mathbf{x},\mathbf{y})
=
\left(
\sum_{i=1}^{n}|x_i-y_i|^p
\right)^{1/p}
$$

## 2.9.5 Applications

Distance measures are used in:

* K-nearest neighbors.
* Clustering.
* Anomaly detection.
* Recommendation systems.
* Similarity-based retrieval.

Feature scaling is often important because features with larger numerical ranges can dominate Euclidean distances.

---

# 2.10 Angles Between Vectors

## 2.10.1 Derivation

The dot product satisfies:

$$
\mathbf{a}\cdot\mathbf{b}
=
\|\mathbf{a}\|_2
\|\mathbf{b}\|_2
\cos\theta
$$

Dividing both sides by the product of the norms gives:

$$
\cos\theta
=
\frac{\mathbf{a}\cdot\mathbf{b}}
{\|\mathbf{a}\|_2\|\mathbf{b}\|_2}
$$

Therefore:

$$
\boxed{
\theta
=
\cos^{-1}
\left(
\frac{\mathbf{a}\cdot\mathbf{b}}
{\|\mathbf{a}\|_2\|\mathbf{b}\|_2}
\right)
}
$$

This formula requires both vectors to be nonzero.

## 2.10.2 Example

Let:

$$
\mathbf{a}=
\begin{bmatrix}
1\\0
\end{bmatrix},
\qquad
\mathbf{b}=
\begin{bmatrix}
0\\1
\end{bmatrix}
$$

Their dot product is:

$$
\mathbf{a}\cdot\mathbf{b}=0
$$

Their norms are both one.

Therefore:

$$
\theta=\cos^{-1}(0)
$$

Hence:

$$
\boxed{\theta=90^\circ=\frac{\pi}{2}}
$$

## 2.10.3 Cosine Similarity

Cosine similarity measures the cosine of the angle between two nonzero vectors.

$$
\boxed{
\operatorname{cos\_sim}(\mathbf{a},\mathbf{b})
=
\frac{\mathbf{a}\cdot\mathbf{b}}
{\|\mathbf{a}\|_2\|\mathbf{b}\|_2}
}
$$

For real, nonzero vectors, the result lies in:

$$
-1\leq
\operatorname{cos\_sim}(\mathbf{a},\mathbf{b})
\leq 1
$$

Interpretation:

* $1$: same direction.
* $0$: orthogonal vectors.
* $-1$: opposite directions.

In embedding search, cosine similarity is often used to compare the directions of embedding vectors. It is undefined if either vector is zero.

---

# 2.11 Orthogonal Vectors

## 2.11.1 Definition

Two real vectors are orthogonal when their dot product is zero.

$$
\boxed{
\mathbf{a}\cdot\mathbf{b}=0
}
$$

For nonzero vectors, this means the angle between them is $90^\circ$.

The zero vector is orthogonal to every vector, even though an angle involving the zero vector is undefined.

## 2.11.2 Example

Let:

$$
\mathbf{a}=
\begin{bmatrix}
2\\3
\end{bmatrix},
\qquad
\mathbf{b}=
\begin{bmatrix}
3\\-2
\end{bmatrix}
$$

Calculate the dot product:

$$
\begin{aligned}
\mathbf{a}\cdot\mathbf{b}
&=2(3)+3(-2)\\
&=6-6\\
&=0
\end{aligned}
$$

Therefore:

$$
\boxed{\mathbf{a}\perp\mathbf{b}}
$$

## 2.11.3 Orthonormal Vectors

A set of vectors is orthonormal when:

1. Every vector has unit norm.
2. Distinct vectors are mutually orthogonal.

For vectors $\mathbf{q}_i$ and $\mathbf{q}_j$:

$$
\boxed{
\mathbf{q}_i^T\mathbf{q}_j
=
\begin{cases}
1,&i=j\\
0,&i\neq j
\end{cases}
}
$$

This condition is often written using the Kronecker delta:

$$
\mathbf{q}_i^T\mathbf{q}_j=\delta_{ij}
$$

Orthonormal bases are important in QR decomposition, least squares, Fourier methods and dimensionality reduction.

---

# 2.12 Cross Product

## 2.12.1 Definition

The cross product is a binary operation on vectors in three-dimensional real Euclidean space.

For:

$$
\mathbf{a}=
\begin{bmatrix}
a_1\\a_2\\a_3
\end{bmatrix},
\qquad
\mathbf{b}=
\begin{bmatrix}
b_1\\b_2\\b_3
\end{bmatrix}
$$

their cross product is:

$$
\boxed{
\mathbf{a}\times\mathbf{b}
=
\begin{bmatrix}
a_2b_3-a_3b_2\\
a_3b_1-a_1b_3\\
a_1b_2-a_2b_1
\end{bmatrix}
}
$$

The result is perpendicular to both input vectors.

## 2.12.2 Determinant Notation

The cross product can be written using formal determinant expansion:

$$
\mathbf{a}\times\mathbf{b}
=
\begin{vmatrix}
\mathbf{i}&\mathbf{j}&\mathbf{k}\\
a_1&a_2&a_3\\
b_1&b_2&b_3
\end{vmatrix}
$$

Expanding along the first row:

$$
\begin{aligned}
\mathbf{a}\times\mathbf{b}
={}&
\mathbf{i}(a_2b_3-a_3b_2)\\
&-\mathbf{j}(a_1b_3-a_3b_1)\\
&+\mathbf{k}(a_1b_2-a_2b_1)
\end{aligned}
$$

The negative sign before the $\mathbf{j}$ component is important.

## 2.12.3 Example

Let:

$$
\mathbf{a}=
\begin{bmatrix}
1\\2\\3
\end{bmatrix},
\qquad
\mathbf{b}=
\begin{bmatrix}
4\\5\\6
\end{bmatrix}
$$

Then:

$$
\mathbf{a}\times\mathbf{b}
=
\begin{bmatrix}
2(6)-3(5)\\
3(4)-1(6)\\
1(5)-2(4)
\end{bmatrix}
$$

Therefore:

$$
\boxed{
\mathbf{a}\times\mathbf{b}
=
\begin{bmatrix}
-3\\6\\-3
\end{bmatrix}
}
$$

## 2.12.4 Geometric Interpretation

The magnitude of the cross product is:

$$
\boxed{
\|\mathbf{a}\times\mathbf{b}\|_2
=
\|\mathbf{a}\|_2
\|\mathbf{b}\|_2
|\sin\theta|
}
$$

This is the area of the parallelogram formed by the two vectors.

The area of the triangle formed by them is:

$$
A_{\triangle}
=
\frac{1}{2}
\|\mathbf{a}\times\mathbf{b}\|_2
$$

If the vectors are parallel, the cross product is zero.

## 2.12.5 Properties

Anticommutativity:

$$
\mathbf{a}\times\mathbf{b}
=
-(\mathbf{b}\times\mathbf{a})
$$

Distributivity:

$$
\mathbf{a}\times(\mathbf{b}+\mathbf{c})
=
\mathbf{a}\times\mathbf{b}
+
\mathbf{a}\times\mathbf{c}
$$

A vector crossed with itself:

$$
\mathbf{a}\times\mathbf{a}=\mathbf{0}
$$

The cross product is generally not associative.

It is especially useful in three-dimensional geometry, physics, graphics and robotics.

---

# 2.13 Projection of Vectors

## 2.13.1 Concept

A vector projection describes the component of one vector in the direction of another.

Let $\mathbf{a}$ be projected onto a nonzero vector $\mathbf{b}$.

The scalar projection is:

$$
\boxed{
\operatorname{comp}_{\mathbf{b}}(\mathbf{a})
=
\frac{\mathbf{a}\cdot\mathbf{b}}
{\|\mathbf{b}\|_2}
}
$$

The vector projection is:

$$
\boxed{
\operatorname{proj}_{\mathbf{b}}(\mathbf{a})
=
\frac{\mathbf{a}\cdot\mathbf{b}}
{\|\mathbf{b}\|_2^2}
\mathbf{b}
}
$$

Equivalently:

$$
\operatorname{proj}_{\mathbf{b}}(\mathbf{a})
=
\frac{\mathbf{a}\cdot\mathbf{b}}
{\mathbf{b}^T\mathbf{b}}
\mathbf{b}
$$

These formulas require $\mathbf{b}\neq\mathbf{0}$.

## 2.13.2 Derivation

Suppose the projection is a scalar multiple of $\mathbf{b}$:

$$
\mathbf{p}=c\mathbf{b}
$$

The residual vector is:

$$
\mathbf{r}=\mathbf{a}-\mathbf{p}
$$

For an orthogonal projection, the residual is perpendicular to $\mathbf{b}$:

$$
\mathbf{r}\cdot\mathbf{b}=0
$$

Substitute the residual:

$$
(\mathbf{a}-c\mathbf{b})\cdot\mathbf{b}=0
$$

Expand:

$$
\mathbf{a}\cdot\mathbf{b}
-c(\mathbf{b}\cdot\mathbf{b})=0
$$

Rearrange:

$$
c=
\frac{\mathbf{a}\cdot\mathbf{b}}
{\mathbf{b}\cdot\mathbf{b}}
$$

Therefore:

$$
\boxed{
\mathbf{p}
=
\frac{\mathbf{a}\cdot\mathbf{b}}
{\mathbf{b}\cdot\mathbf{b}}\mathbf{b}
}
$$

## 2.13.3 Numerical Example

Let:

$$
\mathbf{a}=
\begin{bmatrix}
3\\4
\end{bmatrix},
\qquad
\mathbf{b}=
\begin{bmatrix}
1\\0
\end{bmatrix}
$$

First calculate:

$$
\mathbf{a}\cdot\mathbf{b}=3
$$

and:

$$
\mathbf{b}\cdot\mathbf{b}=1
$$

Therefore:

$$
\operatorname{proj}_{\mathbf{b}}(\mathbf{a})
=
\frac{3}{1}
\begin{bmatrix}
1\\0
\end{bmatrix}
$$

Hence:

$$
\boxed{
\operatorname{proj}_{\mathbf{b}}(\mathbf{a})
=
\begin{bmatrix}
3\\0
\end{bmatrix}
}
$$

The residual is:

$$
\mathbf{r}
=
\mathbf{a}-\operatorname{proj}_{\mathbf{b}}(\mathbf{a})
=
\begin{bmatrix}
0\\4
\end{bmatrix}
$$

Verification:

$$
\mathbf{r}\cdot\mathbf{b}=0
$$

Therefore, the residual is perpendicular to the projection direction.

## 2.13.4 Projection Matrix

For a nonzero vector $\mathbf{b}$, the projection matrix onto its span is:

$$
\boxed{
P=
\frac{\mathbf{b}\mathbf{b}^T}
{\mathbf{b}^T\mathbf{b}}
}
$$

Then:

$$
\operatorname{proj}_{\mathbf{b}}(\mathbf{a})=P\mathbf{a}
$$

The matrix has two important properties:

$$
P^T=P
$$

and:

$$
P^2=P
$$

The first property means that $P$ is symmetric. The second means that projecting an already projected vector does not change it.

---

# 2.14 Vector Geometry

## 2.14.1 Distance Formula

For two points $A=(x_1,y_1)$ and $B=(x_2,y_2)$:

$$
d(A,B)
=
\sqrt{(x_2-x_1)^2+(y_2-y_1)^2}
$$

In $n$ dimensions:

$$
d(\mathbf{x},\mathbf{y})
=
\sqrt{\sum_{i=1}^{n}(x_i-y_i)^2}
$$

## 2.14.2 Equation of a Line

A line through a point $\mathbf{p}$ with direction vector $\mathbf{v}$ can be represented as:

$$
\boxed{
\mathbf{x}=\mathbf{p}+t\mathbf{v}
}
$$

where $t\in\mathbb{R}$.

For example:

$$
\mathbf{p}=
\begin{bmatrix}
1\\2
\end{bmatrix},
\qquad
\mathbf{v}=
\begin{bmatrix}
3\\4
\end{bmatrix}
$$

Then:

$$
\mathbf{x}
=
\begin{bmatrix}
1\\2
\end{bmatrix}
+
t
\begin{bmatrix}
3\\4
\end{bmatrix}
$$

Thus:

$$
x=1+3t,\qquad y=2+4t
$$

## 2.14.3 Equation of a Plane

A plane in three dimensions can be represented using a normal vector $\mathbf{n}$ and a point $\mathbf{p}$:

$$
\boxed{
\mathbf{n}\cdot(\mathbf{x}-\mathbf{p})=0
}
$$

If:

$$
\mathbf{n}=
\begin{bmatrix}
a\\b\\c
\end{bmatrix}
$$

then the plane equation becomes:

$$
ax+by+cz=d
$$

for a suitable constant $d$.

The normal vector is perpendicular to every direction lying in the plane.

## 2.14.4 Area of a Parallelogram

For vectors $\mathbf{a}$ and $\mathbf{b}$ in three dimensions:

$$
A=
\|\mathbf{a}\times\mathbf{b}\|_2
$$

In two dimensions, if:

$$
\mathbf{a}=
\begin{bmatrix}
a_1\\a_2
\end{bmatrix},
\qquad
\mathbf{b}=
\begin{bmatrix}
b_1\\b_2
\end{bmatrix}
$$

then:

$$
A=
|a_1b_2-a_2b_1|
$$

This is the absolute value of the determinant formed by the two vectors.

## 2.14.5 Volume of a Parallelepiped

For three vectors in $\mathbb{R}^3$:

$$
\boxed{
V=
|\mathbf{a}\cdot(\mathbf{b}\times\mathbf{c})|
}
$$

The scalar triple product gives the signed volume; its absolute value gives the geometric volume.

## 2.14.6 Linear Independence: Geometric Intuition

Two vectors in $\mathbb{R}^2$ are linearly independent if neither is a scalar multiple of the other.

For two vectors:

$$
\mathbf{a}=
\begin{bmatrix}
a_1\\a_2
\end{bmatrix},
\qquad
\mathbf{b}=
\begin{bmatrix}
b_1\\b_2
\end{bmatrix}
$$

they are linearly independent exactly when:

$$
a_1b_2-a_2b_1\neq 0
$$

If the determinant is zero, the vectors are linearly dependent.

This criterion applies to two vectors in $\mathbb{R}^2$; higher-dimensional cases require a more general test.

---

# Summary

| Topic                   | Essential formula                                                                                                    |            |                 |
| ----------------------- | -------------------------------------------------------------------------------------------------------------------- | ---------- | --------------- |
| Vector magnitude        | $|\mathbf{x}|_2=\sqrt{\sum_i x_i^2}$                                                                                 |            |                 |
| Vector addition         | $(\mathbf{a}+\mathbf{b})_i=a_i+b_i$                                                                                  |            |                 |
| Scalar multiplication   | $|c\mathbf{x}|_2=                                                                                                    | c          | |\mathbf{x}|_2$ |
| Linear combination      | $\mathbf{u}=\sum_i c_i\mathbf{v}_i$                                                                                  |            |                 |
| Dot product             | $\mathbf{a}\cdot\mathbf{b}=\sum_i a_i b_i$                                                                           |            |                 |
| Angle                   | $\cos\theta=\frac{\mathbf{a}\cdot\mathbf{b}}{|\mathbf{a}|_2|\mathbf{b}|_2}$                                          |            |                 |
| Euclidean distance      | $d(\mathbf{x},\mathbf{y})=|\mathbf{x}-\mathbf{y}|_2$                                                                 |            |                 |
| Orthogonality           | $\mathbf{a}\cdot\mathbf{b}=0$                                                                                        |            |                 |
| Cross product magnitude | $|\mathbf{a}\times\mathbf{b}|_2=|\mathbf{a}|_2|\mathbf{b}|_2                                                         | \sin\theta | $               |
| Vector projection       | $\operatorname{proj}_{\mathbf{b}}(\mathbf{a})=\frac{\mathbf{a}\cdot\mathbf{b}}{\mathbf{b}\cdot\mathbf{b}}\mathbf{b}$ |            |                 |

---

# Practice Questions

## Beginner

1. What is the difference between a scalar and a vector?
2. Write a vector with components $3,4,5$ in column notation.
3. Calculate $\mathbf{a}+\mathbf{b}$ for $\mathbf{a}=(2,3)$ and $\mathbf{b}=(4,5)$.
4. Calculate $3\mathbf{v}$ for $\mathbf{v}=(2,-1)$.
5. Find the Euclidean norm of $\mathbf{x}=(6,8)$.

## Intermediate

6. Calculate the dot product of $(1,2,3)$ and $(4,5,6)$.
7. Find the angle between $(1,0)$ and $(0,1)$.
8. Determine whether $(2,4)$ and $(1,2)$ are linearly independent.
9. Calculate the projection of $\mathbf{a}=(3,4)$ onto $\mathbf{b}=(1,0)$.
10. Calculate the cross product of $(1,0,0)$ and $(0,1,0)$.

## Advanced

11. Derive the vector projection formula using the orthogonality of the residual.
12. Prove the triangle inequality for the Euclidean norm using the Cauchy-Schwarz inequality.
13. Prove that an orthogonal projection matrix is idempotent: $P^2=P$.
14. Explain how dot products are used to calculate cosine similarity.
15. Explain the role of vector representations in machine-learning models.

---

# Next Topic

**03. Matrices and Matrix Operations**

Topics to study next:

* Matrix notation and dimensions
* Types of matrices
* Matrix addition and subtraction
* Scalar multiplication
* Matrix multiplication
* Transpose
* Symmetric and skew-symmetric matrices
* Identity and zero matrices
* Diagonal and triangular matrices
* Trace
* Block matrices
* Matrix powers
* Properties of matrix operations
