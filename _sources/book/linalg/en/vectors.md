(vectors_en)=
# Vectors

Author(s):

- [El-Ayyass Dani](http://github.com/dayyass)

Translation:

- [Pronkin Alexey](http://github.com/alexey-pronkin)
- [Zheltonozhskii Evgenii](https://github.com/Randl)
- [vvssttkk](https://github.com/vvssttkk)


## Definition

The term `vector` has several interpretations: mathematical, geometric, physical, etc. The exact meaning of the term depends on the context.

Formally, a vector is defined as an element of vector space -- a set with **addition** and **multiplication of a vector by a number (scalar)** operations, which satisfy [8 axioms](https://en.wikipedia.org/wiki/Vector_space).

For simplicity, let us consider the rectangular (Cartesian) coordinate system in the plane, familiar from school days -- two perpendicular to each other axes $x$ and $y$, selected unit vectors (orthogonal) $\mathbf{e}_1$, $\mathbf{e}_2$ on them and the origin of coordinates.

The vector $\mathbf{a}$ in this coordinate system can be written as follows: $\mathbf{a} = a_1 \mathbf{e}_1 + a_2 \mathbf{e}_2 = \begin{pmatrix} a_1 \\ a_2 \end{pmatrix}$

**Note 1**: Vector coordinates do not uniquely define its position in the plane, but only the position of the vector's end relative to its start. For example, a vector $\begin{pmatrix} 3 \\ 4 \end{pmatrix}$ can be drawn either from the origin $\begin{pmatrix} 0 , 0 \end{pmatrix}$ with the end at $\begin{pmatrix} 3 , 4 \end{pmatrix}$, or from an arbitrary point, e.g. $\begin{pmatrix} 1 , 1 \end{pmatrix}$ with the end at $\begin{pmatrix} 4 , 5 \end{pmatrix}$. Both of these vectors correspond to 3 orthogonal unite vectors on the $x$-axis and 4 on the $y$-axis. Normally, unless otherwise stated, it is assumed that the vector is deferred from the origin.

**Note 2**: A vector can be represented either as a column vector $\begin{pmatrix} a_1 \ a_2 \end{pmatrix}$ or as a row vector $\begin{pmatrix} a_1 \ a_2 \end{pmatrix}$. Hereinafter, by a vector we mean a column vector, unless otherwise stated.

The notion of a vector in the plane can be generalized to 3-dimensional space, and, in general, to $n$-dimensional space (which can no longer be visualized):

$$
    \mathbf{a} = a_1 \mathbf{e}_1 + a_2 \mathbf{e}_2 + ... + a_n \mathbf{e}_n = \begin{pmatrix} a_1 \ a_2 \\ ... \ a_n \end{pmatrix}
$$

## Vector operations

As stated earlier, there are two basic operations on vectors in the formal definition:

- addition:

$$
    \mathbf{a} + \mathbf{b} = (a_1 + b_1) \mathbf{e}_1 + (a_2 + b_2) \mathbf{e}_2 + ... + (a_n + b_n) \mathbf{e}_n = \ = \begin{pmatrix} a_1 \ a_2 \\ ... \ a_n \end{pmatrix} + \begin{pmatrix} b_1 \\ b_2 \\ ... \ b_n \end{pmatrix} = \begin{pmatrix} a_1 + b_1 \ a_2 + b_2 \\ ... \ a_n + b_n \end{pmatrix}
$$

- multiplication of a vector by a number (scalar):

$$
    \lambda \mathbf{a} = \lambda a_1 \mathbf{e}_1 + \lambda a_2 \mathbf{e}_2 + ... + \lambda a_n \mathbf{e}_n = \lambda \begin{pmatrix} a_1 \\ a_2 \\ ... \\ a_n \end{pmatrix} = \begin{pmatrix} \lambda a_1 \\ \lambda a_2 \\ ... \\ \lambda a_n \end{pmatrix}
$$

The operation of multiplying a vector by a number can be interpreted geometrically as a contraction/extension of a vector.

Using these two operations, we can define **linear combinations of vectors**: $\alpha_1 \mathbf{a}_1 + \alpha_2 \mathbf{a}_2 + ... + \alpha_n \mathbf{a}_n ,$ where $\mathbf{a}_1, \mathbf{a}_2, ..., \mathbf{a}_n$ are vectors and $\alpha_1, \alpha_2, ..., \alpha_n$ are numbers.

## The norm (length) of a vector

In linear algebra, the term **norm** is used to generalize the notion of vector length. It can be said that the notions of length and norm are equivalent.

Formally the norm is defined as a functional in the vector space satisfying [3 axioms](https://en.wikipedia.org/wiki/Norm_(mathematics)). Norm is mapping elements of this space (vectors) to the set of non-negative real numbers.

There are many functionals satisfying this definition of norm, but we will consider the most commonly used one -- **Euclidean norm**.

For simplicity, let us consider a vector in the plane. Geometrically, it is a directional segment. The directionality of a vector has no effect on its length, so we can work with it as a segment in the plane and calculate its length using school formulas.
Note that the vector coordinates correspond to the numbers multiplying coordinate axis orthogonal vectors, so the vector length formula is: $\lVert \mathbf{a} \rVert = \sqrt{a_1^2 + a_2^2}$. Accordingly, in general, the formula is  $\lVert \mathbf{a} \rVert = \sqrt{a_1^2 + a_2^2 + ... + a_n^2}$.

## Scalar product

One of the most common operations on two vectors is the so-called **scalar product**, the result of which is a number (scalar) -- hence the name of the operation.

**Note**: In addition to scalar product there is also [vector product or cross product](https://en.wikipedia.org/wiki/Cross_product) over a pair of vectors, the result of which is a vector. There is also [triple product](https://en.wikipedia.org/wiki/Triple_product) over a triplet of vectors, the result of which is a number. These operations will not be covered in this course.

Scalar product is used in determining the length of vectors and the angle between them. This operation has two definitions:

- Algebraic: $ \mathbf{a} \cdot \mathbf{b} = a_1 b_1 + a_2 b_2 + ... + a_n b_n$
- geometric: $\mathbf{a} \cdot \mathbf{b} = \lVert \mathbf{a} \rVert \lVert \mathbf{b} \rVert \cos{\\theta},$ where $\theta$ is the angle between the vectors $\mathbf{a}$ and $\mathbf{b}$.

Using both of these definitions, we can derive a formula for calculating the cosine of the angle between the vectors:

$$
    \cos{\theta} = \frac{\mathbf{a} \cdot \mathbf{b}}{\lVert \mathbf{a} \rVert \lVert \mathbf{b} \rVert} = \frac{a_1 b_1 + a_2 b_2 + ... + a_n b_n}{\sqrt{a_1^2 + a_2^2 + ... + a_n^2} \sqrt{b_1^2 + b_2^2 + ... + b_n^2}}
$$

Using this formula we can arrive at one of the main properties of scalar product, which is that **two vectors are perpendicular if and only if their scalar product is 0**: $\mathbf{a} \perp \mathbf{b} \leftrightarrow \cos{\theta} = 0 \leftrightarrow \mathbf{a} \cdot \mathbf{b} = 0$

The scalar product can be used to calculate the vector norm as follows: $\lVert \mathbf{a} \rVert = \sqrt{\mathbf{a} \cdot \mathbf{a}}$

## Linear independence

One of the fundamental concepts of linear algebra is **linear dependence/independence**.

To define this concept, consider a set of several vectors. A set of vectors is **linearly dependent** if there exists nontrivial linear combination of vectors of this set (at least one element of this combination is not 0) equal to a zero vector (a vector consisting only of 0):

$$
    \lambda_1 \mathbf{a}_1 + \lambda_2 \mathbf{a}_2 + ... + \lambda_m \mathbf{a}_m = \begin{pmatrix} 0 \\ 0 \\ ... \\ 0 \end{pmatrix}, \ \exists j, \, \lambda_j \not = {0}
$$

If a set of vectors is not linearly dependent, that is, there is no nontrivial linear combination of vectors of a given set equal to the zero vector, then such a set of vectors is called **linearly independent**.

**Example**:

- A linearly independent set of vectors (only the zero coefficients of a linear combination lead to a zero vector):

$$
    \begin{pmatrix} 1 \\ 0 \\ 0 \end{pmatrix} \begin{pmatrix} 0 \\ 1 \\ 0 \end{pmatrix} \begin{pmatrix} 0 \\\ 0 \\ 1 \end{pmatrix} \rightarrow 0 \cdot \begin{pmatrix} 1 \\ 0 \\ 0  \end{pmatrix} + 0 \cdot \begin{pmatrix} 0 \\ 1 \\ 0 \end{pmatrix} + 0 \cdot \begin{pmatrix} 0 \\ 0 \\ 1 \end{pmatrix} = \begin{pmatrix} 0 \\ 0 \\ 0 \end{pmatrix}
$$

- linearly dependent set of vectors (there are non-zero coefficients of the linear combination that lead to the zero vector):

$$
    \begin{pmatrix} 1 \\ 0 \\ 0 \end{pmatrix} \begin{pmatrix} 0 \\ 1 \\ 0 \end{pmatrix} \begin{pmatrix} 2 \\ 3 \\ 0 \end{pmatrix} \rightarrow 2 \cdot \begin{pmatrix} 1 \\ 0 \\ 0 \end{pmatrix} + 3 \cdot \begin{pmatrix} 0 \\ 1 \\ 0 \end{pmatrix} - 1 \cdot\begin{pmatrix} 2 \\ 3 \\ 0 \end{pmatrix} = \begin{pmatrix} 0 \\ 0 \\ 0 \end{pmatrix}
$$

The following property can be deduced from the definition of linear dependence:
A set of vectors is linearly dependent if and only if one of the elements of that set can be expressed through the remaining elements.

**Note**: If vectors represent some characteristics of objects, then linear dependence can be interpreted as data redundancy.

The notion of linear independence introduces the concept of **dimensionality** of a vector space -- the maximum number of linearly independent vectors in it.

## Basis

In the formal definition of a vector there are no quantitative interpretations of it, just two operations on vectors and 8 axioms.

So where do quantitative measurements come from? To make this clear, we need to introduce the concept of **basis**.

A basis is a finite set of vectors in a vector space such that any vector in that space can be uniquely represented as a linear combination of vectors of that set.

Recall one of the examples above, where we represented a rectangular coordinate system in the plane and unit vectors $\mathbf{e}_1$, $\mathbf{e}_2$. $\mathbf{e}_1 = \begin{pmatrix} 1 \\ 0 \end{pmatrix}$, $\mathbf{e}_2 = \begin{pmatrix} 0 \\ 1 \end{pmatrix}$.
In this example, we decompose the arbitrary vector $\mathbf{a}$ as follows:

$$
    \mathbf{a} = a_1 \mathbf{e}_1 + a_2 \mathbf{e}_2 = a_1 \begin{pmatrix} 1 \\ 0 \end{pmatrix} + a_2 \begin{pmatrix} 0 \\ 1 \end{pmatrix} = \begin{pmatrix} a_1 \\ 0 \end{pmatrix} + \begin{pmatrix} 0 \\ a_2 \end{pmatrix} = \begin{pmatrix} a_1 \\ a_2 \end{pmatrix}
$$

It turns out that the orthogonal vectors $\mathbf{e}_1$, $\mathbf{e}_2$ **are the basis of the two-dimensional vector space**, and by linear combination of these vectors we can uniquely represent any vector in this space.

The question arises, is this basis unique in two-dimensional space, or not?

The answer to this question is no. In fact, one can take any two vectors (**almost any**) and they will also form a basis, meaning that any vector can be decomposed by their linear combination.

**Example**.

Suppose we have a vector $\begin{pmatrix} 2 \\ 3 \end{pmatrix}$ in a basis of unit orthogonal vectors, and we want to decompose it in another basis $\begin{pmatrix} -2 \\ 0 \end{pmatrix} \begin{pmatrix} 0 \\ -3 \end{pmatrix}$:

$$
    \alpha_1 \begin{pmatrix} -2 \\ 0 \end{pmatrix} + \alpha_2 \begin{pmatrix} 0 \\ -3 \end{pmatrix} = \begin{pmatrix} 2 \\3 \end{pmatrix}
$$

From where we can find that $\alpha_1 = -1$, $\alpha_2 = -1$:

$$
    -1 \begin{pmatrix} -2 \\ 0 \end{pmatrix} + -1 \begin{pmatrix} 0 \\ -3 \end{pmatrix} = \begin{pmatrix} 2 \\ 0 \end{pmatrix} + \begin{pmatrix} 0 \\ 3 \end{pmatrix} = \begin{pmatrix} 2 \\ 3 \end{pmatrix}
$$

So, vector $\begin{pmatrix} 2 \\ 3 \end{pmatrix}$ in the basis of unit orthogonal vectors is represented as $\begin{pmatrix} -1 \\ -1 \end{pmatrix}$ in the basis $\begin{pmatrix} -2 \\ 0 \end{pmatrix} \begin{pmatrix} 0 \\ -3 \end{pmatrix}$.

But, as mentioned before, **not any set of vectors**  makes a basis.

For example, the set of vectors $\begin{pmatrix} -2 \\ 0 \end{pmatrix}$, $\begin{pmatrix} -3 \\ 0 \end{pmatrix}$ cannot decompose the vector $\begin{pmatrix} 2 \\ 3 \end{pmatrix}$, so this set of vectors is not a basis.

What is the fundamental difference between these sets, and can the basis of a two-dimensional space consist of more or fewer vectors than 2?

Linear algebra has an answer to this:

**Any $n$ linearly independent vectors of $n$-dimensional vector space form the basis of that space.**

Exactly due to the linear dependence, the vectors $\begin{pmatrix} -2 \\ 0 \end{pmatrix}$, $\begin{pmatrix} -3 \\ 0 \end{pmatrix}$ can't be the basis of a two-dimensional space.

## What did we learn?

- The definition of a vector;
- The operations on vectors;
- The vector norm (length);
- The scalar product;
- The linear independence;
- The basis.
