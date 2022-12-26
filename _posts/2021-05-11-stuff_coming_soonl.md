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

$$ \vec{a} . \vec{b} = a_1 b_1 + a_2 b_2 + a_3 b_3 $$

$$ \vec{a} . \vec{a} = a_1^2 + a_2^2 + a_3^2 $$

$$ \hat{i} . \vec{b} = a_1 $$

$$ \hat{i} . \hat{i} = 1 \text{ and } \hat{j} . \hat{j} = 0$$

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
\vec{a} & \vec{a}
\end{bmatrix}
$$










 

 