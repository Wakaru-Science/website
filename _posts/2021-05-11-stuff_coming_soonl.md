---
title: "Stuff coming soon!"
date: 2021-05-11T17:00:00-04:00
categories:
  - blog
tags:
  - Science

usemathjax: true
---

Vectors $$\mu$$

\begin{equation}
f(x) = \int_{-\infty}^\infty \hat f(\xi)\,e^{2 \pi i \xi x} \,d\xi
\end{equation}

Definition: Anything with a quantity and a direction is a vector. Vectors are numbers with direction, there are many quantities which are 'not symmetric in space', their value is dependent on direction, part of it's definition and a vector is used to represent that quantitity.

Example: Velocity is a vector because 5 m/s up is not the same as 5 m/s down, eventhought the 'speed' (5 m/s) is the same.

Diagram: A vector is reprentated by an arrow. The tail and head of arrow represents the direction, the length of the arrow represents quantity 'magnitude' of vector. The origin of a single vector does not matter. Vectors are free flowing, it is one of the only objects in physics that you can move around freely in a graph, as long as you do not change  the length and direction of vector.

Code: A vector can be represented as a array in numpy. A vector is not limited to 3 dimensions. 3D vectors in vpython is represented as dsfdfkm.

Notation: Vector has many notations. Usually $$\vec{a}$$ represents vector a. Sometimes, bold a, $$\textbf{a}$$ is also used.

Important Operations

Addition
Multiplication

Unit vectors

Definition: What is a hot day in a cold country is, at the same temperature, cold weather in a typically hot country. The 'hot' only has meaning when it is compared to something. 25 degrees celcius only has meaning when 0 degrees celcius is defined. Same way, the magnitude and direction of vector doesn't mean anything unless it is compared to some standard. That is the unit vector. Unit vector has a magnitude of '1' and a direction.

Example: If the 1 is 1 meter, then the car is moving with a magnitude of 25 times unit vector, means 25 m/s. Similarly if the '1' is 1 kilometer/hr, the the car is moving with 25 km/hr. For each dimension there can be only 1 unit vectors, so for 3D, 3 unit vectors, define 3 directions, i.e, up, left and forward. Each having an opposite down, right and backward.

Diagram: Unit vector is drawn the same as a vector, just smaller and usually grouped togeter.

Code: 

Notation: Unit vectors have special notation $$\hat{e}$$, call as 'e cap'. Unit vectors for 3D are $$\hat{i},\hat{j},\hat{k}$$.

Vector $$ \hat{e} \vec{e} $$

$$ \vec{a} = a_1 \hat{i} + a_2 \hat{i} + a_3 \hat{j} $$

dot product

$$ \vec{a} \cdot \vec{b} = a_1 b_1 + a_2 b_2 + a_3 b_3 $$

$$ \vec{a} \cdot \vec{a} = a_1^2 + a_2^2 + a_3^2 $$

$$ \hat{i} \cdot \vec{b} = a_1 $$

$$ \hat{i} \cdot \hat{i} = 1 \text{ and } \hat{j} \cdot \hat{j} = 0$$

When we are dealing with a group of vectors, this method quickly becomes tedious. Once the unit vectors are defined for a system, they do not change and writing them again and again does not accomplish anything. Moreover, we need a way to perform operations, addition, multiplication, and manipulate a group of vectors in one go. The current method is good for single for single vector operations, but not for a many vectors. In the current method, we also need a way to group multiple operations (series of additon, multipication in a specific order) so that we can we can do much more complicated things.

Instead of representing $$ \vec{a} \text{ as } a_1 \hat{i} + a_2 \hat{i} + a_3 \hat{j} $$, we can compress the equation as:
$$
\begin{bmatrix}
a_1 \\
a_2 \\
a_3
\end{bmatrix}
\begin{bmatrix}
\hat{i} & \hat{j} & \hat{k}
\end{bmatrix}
=
\begin{bmatrix}
\vec{a}
\end{bmatrix}
$$

Vector is represented as a 3x1 or 1x3 matrix. Matrix is condensed way to form linear combinations or linear equations.

Using the rules of matrix multiplication, the matrix equation expands into vector equation.

If you have two vectors, they can be represented in one matrix equation like 

$$
\begin{bmatrix}
a_1 & b_1\\
a_2 & b_2\\
a_3 & b_3
\end{bmatrix}
\begin{bmatrix}
\hat{i} & \hat{j} & \hat{k}
\end{bmatrix}
=
\begin{bmatrix}
\vec{a} & \vec{b}
\end{bmatrix}
$$

A new vector with a different coefficients as $$ \vec{a} = a_1 \hat{i} + a_2 \hat{i} + a_3 \hat{j} $$ but different basis is $$ \vec{a}^\prime = a_1 \hat{l} + a_2 \hat{m} + a_3 \hat{n} $$

These two vectors are represented as:

$$
\begin{bmatrix}
a_1 \\
a_2 \\
a_3
\end{bmatrix}
\begin{bmatrix}
\hat{i} & \hat{j} & \hat{k} \\
\hat{l} & \hat{m} & \hat{n}
\end{bmatrix}
=
\begin{bmatrix}
\vec{a} & \vec{a}^\prime
\end{bmatrix}
$$

We can perform one important simplification, ie once the basis $$[\hat{i} , \hat{j} ,\hat{k}]$$ is defined, a vector can be repsented only as $$
\begin{bmatrix}
a_1 \\
a_2 \\
a_3
\end{bmatrix}$$, where the order in which the vector magnitudes appears, denote which unit vector it corresponds to.


Thus, the dot product $$ \vec{a} \cdot \vec{b} = a_1 b_1 + a_2 b_2 + a_3 b_3 $$ is:

$$
\begin{bmatrix}
a_1 \\
a_2 \\
a_3
\end{bmatrix}
\cdot
\begin{bmatrix}
b_1 & b_2 & b_3 \\
\end{bmatrix}
=
a_1 b_1 + a_2 b_2 + a_3 b_3 $$

The unit vecors themselves become [1,1,1] because the order matters now, the notation used to define them is irrelevant.

Thus, $$ \vec{a} \cdot \hat{i} = a_1 $$ becomes,

$$
\begin{bmatrix}
a_1 \\
a_2 \\
a_3
\end{bmatrix}
\cdot
\begin{bmatrix}
1 & 0 & 0 \\
\end{bmatrix}
=
a_1 $$

Multiplying vector a by 3 is $$ 3\vec{a} = 3a_1 \hat{i} + 3a_2 \hat{i} + 3a_3 \hat{j} $$ but in matrix notation,

$$
3
\begin{bmatrix}
a_1 \\
a_2 \\
a_3
\end{bmatrix}
=
\begin{bmatrix}
3a_1 \\
3a_2 \\
3a_3
\end{bmatrix}
$$

This operation can also be rewritten as

$$
\begin{bmatrix}
3 & 0 & 0 \\
0 & 3 & 0 \\
0 & 0 & 3 \\
\end{bmatrix}
\begin{bmatrix}
a_1 &  a_2 & a_3
\end{bmatrix}
=
\begin{bmatrix}
3a_1 & 3a_2 & 3a_3
\end{bmatrix}
$$

Why did we complicate a simple operation? It is the show how good matrices are at mixing a vector (linear combination) for example

$$
\begin{bmatrix}
0.25 & 0 & 0.25 \\
0    & 1 & 0    \\
0.75 & 0 & 0.75 \\
\end{bmatrix}
\begin{bmatrix}
a_1 &  a_2 & a_3
\end{bmatrix}
=
\begin{bmatrix}
0.25a_1+0.75a_3 & a_2 & 0.25a_1+0.75a_3
\end{bmatrix}
$$

This property can be now used to create function like objects,

Instead of fixed fractions like 0.25, we can use trignometric functions, like $$\sin{\theta}$$, which can take $$\theta$$ as a variable. Trignometic functions such as $$\sin{\theta}$$ act like percentages (fractions) anyways.

$$
\begin{bmatrix}
1 & 0 & 0      \\
0 & \cos{\theta} & -\sin{\theta}    \\
0 & \sin{\theta} & \cos{\theta} \\
\end{bmatrix}
\begin{bmatrix}
a_1 & a_2 & a_3
\end{bmatrix}
=
\begin{bmatrix}
a_1 &  a_2\cos{\theta} + a_3\sin{\theta} & -a_2\sin{\theta} + a_3\cos{\theta}
\end{bmatrix}
$$

where the matrix-function will rotate the vector around x axis by $$ \theta $$ degrees. Such a matrix with a special job to do needs a special name too - Operator. Like a fucntion, an operator will transform a (set of) vectors.

How does the operator act?

$$
\begin{bmatrix}
1 \\
0 \\
0 \\
\end{bmatrix}
\begin{bmatrix}
a_1 & a_2 & a_3
\end{bmatrix} 
+
\begin{bmatrix}
0            \\
\cos{\theta} \\
\sin{\theta} \\
\end{bmatrix}
\begin{bmatrix}
a_1 & a_2 & a_3
\end{bmatrix} 
+
\begin{bmatrix}
0             \\
-\sin{\theta} \\
\cos{\theta}  \\
\end{bmatrix}
\begin{bmatrix}
a_1 & a_2 & a_3
\end{bmatrix} 
= \\
\begin{bmatrix}
a_1 &  a_2\cos{\theta} + a_3\sin{\theta} & -a_2\sin{\theta} + a_3\cos{\theta}
\end{bmatrix}
$$

Each column of the operator matrix tells us how the magnitude of vector in that direction is going to end up. If we are only interested in one direction, we can set all other columns to 0.

Row column is not so important. Setting a row to 0 is basically setting the contribution of an dimension to 0. Setting the row to 0 makes sure that no matter how complicated the matrix is, everytime the magnitude in that dimension gets multiplied, it is always multiplied by 0, and the final result will have no contribution from that direction whatsoever.

Just like functions we can combine two operators, to create more complicated transformations. Instead of multipying by 3, we can multiply by any number x 
$$
\begin{bmatrix}
x & 0 & 0 \\
0 & x & 0 \\
0 & 0 & x \\
\end{bmatrix}
\begin{bmatrix}
a_1 &  a_2 & a_3
\end{bmatrix}
=
\begin{bmatrix}
xa_1 & xa_2 & xa_3
\end{bmatrix}
$$

and raise the magnitude to the power of e 

$$
\begin{bmatrix}
exp() & 0 & 0 \\
0 & exp() & 0 \\
0 & 0 & exp() \\
\end{bmatrix}
\begin{bmatrix}
a_1 &  a_2 & a_3
\end{bmatrix}
=
\begin{bmatrix}
e^{a_1} & e^{a_2} & e^{a_3}
\end{bmatrix}
$$

Multiplying the result of both operations gives us 
$$
\begin{bmatrix}
xa_1e^{a_1}  &  xa_2e^{a_2} & xa_3e^{a_3}
\end{bmatrix}
$$

But can also have operator act on an operator, just like a function $$ g(f(x))$$
$$
\begin{bmatrix}
exp() & 0 & 0 \\
0 & exp() & 0 \\
0 & 0 & exp() \\
\end{bmatrix}
\begin{bmatrix}
x & 0 & 0 \\
0 & x & 0 \\
0 & 0 & x \\
\end{bmatrix}
\begin{bmatrix}
a_1 &  a_2 & a_3
\end{bmatrix}
=
\begin{bmatrix}
a_1e^{xa_1}  &  a_2e^{xa_2} & a_3e^{xa_3}
\end{bmatrix}

The only way of creating new vectors is scaling and adding them together, and matrices arises naturally.

Just like there are standard functions, standard matrices arises.

Identity matrix

This matrix is like number 1. It can be multiplied to the vector to gave same vector back.

$$
\begin{bmatrix}
1 & 0 & 0 \\
0 & 1 & 0 \\
0 & 0 & 1 \\
\end{bmatrix}
\begin{bmatrix}
a_1 &  a_2 & a_3
\end{bmatrix}
=
\begin{bmatrix}
a_1 & a_2 & a_3
\end{bmatrix}
$$

From now on, we will set the rules that all operators have to be square matrix.

Just like, all other numbers arise from adding number 1, we can add and multiply identity matrix with numbers to create a bunch of matirices. All these matrices will have it's off diagonal elements as 0.

There is a matrix what when multiplied by gives unitary matix. That matrix is its inverse 

Matrices in real life can be huge and can have all kinds of elements. In order to tame them, we need to set some ground rules for what matrix can and cannot have as it's elements and how to check whether those rules are followed. Scientists like to name these matrics with special names, so that when the name is invoked we immediately get valuable information about the contents of the matrix.

A matrix can have complex numbers as it's elements. You can take complex conjugate of an matrix.
The only way a matrix is equal to it's complex conjugate is when all elements of the matrix are real numbers. So if a matrix's complex conjugate is equal to the original matrix, its a real matrix.

A transpose of a matrix is when you interchange it's rows and collumns. The only way a matrix is equal to it's transpose is if it is symmetric. So a symmetric matrix is a matrix whose rows and columns can be interchanged.

A matrix whose

