+++
title = "Intersection Number of Two Curves on Torus"
author = ["Victoria Ordonez"]
draft = false
+++

## Mapping \\( \mathbb{R}^2 \\) to the Quotient Space \\( \mathbb{R}^2 / \sim \\)

Consider the universal cover of the torus, \\( \mathbb{R}^2 \\). The quotient space \\( \mathbb{R}^2 / \sim \\) is formed by identifying points whose difference is an integer vector.\\
The equivalence relation \\( \sim \\) is defined as: \\
Two points \\( (x_1, y_1) \\) and \\( (x_2, y_2) \\) are equivalent under \\( \sim \\) if:
\\[
(x_1, y_1) \sim (x_2, y_2) \iff (x_2 - x_1, y_2 - y_1) \in \mathbb{Z}^2.
\\]
The quotient map \\( \pi : \mathbb{R}^2 \to \mathbb{R}^2 / \sim \\) is then defined as:
\\[
\pi(x, y) = (x \mod 1, y \mod 1),
\\]
which maps each point in \\( \mathbb{R}^2 \\) to its equivalence class on the torus. Geometrically, this means every point \\( (x, y) \in \mathbb{R}^2 \\) is mapped to a point inside the unit square \\( [0, 1) \times [0, 1) \\), representing a point on the torus.

## Defining the Map \\( A \\) on \\( \mathbb{R}^2 \\)

Let \\( A: \mathbb{R}^2 \to \mathbb{R}^2 \\) be a linear map represented by a \\( 2 \times 2 \\) matrix:
\\[
A = \begin{bmatrix}
  a & b \\
  c & d
\end{bmatrix}.
\\]
For any point \\( (x, y) \in \mathbb{R}^2 \\), the action of \\( A \\) is given by:
\\[
A \begin{bmatrix} x \\ y \end{bmatrix} = \begin{bmatrix}
  ax + by \\
  cx + dy
\end{bmatrix}.
\\]

## Inducing a Well-Defined Map on the Quotient Space

To induce a well-defined map \\( \bar{A}: \mathbb{R}^2 / \sim \to \mathbb{R}^2 / \sim \\), we must show if two points \\( (x, y) \\) and \\( (x + m, y + n) \\) are equivalent under the equivalence relation, their images under \\( A \\) must also be equivalent.

Applying \\( A \\) to the equivalent point \\( (x + m, y + n) \\):
\\[
A \begin{bmatrix} x + m \\ y + n \end{bmatrix} = \begin{bmatrix}
  a(x + m) + b(y + n) \\
  c(x + m) + d(y + n)
\end{bmatrix}.
\\]
\\[
= \begin{bmatrix}
  (ax + by) + (am + bn) \\
  (cx + dy) + (cm + dn)
\end{bmatrix}.
\\]
Since \\( m, n \in \mathbb{Z} \\), \\( (am + bn) , (cm + dn) \in \mathbb{Z} \\), meaning the transformed point differs from \\( A(x, y) \\) by an integer vector, so it lies in the same equivalence class in the quotient space. Thus, the map \\( \bar{A} \\) is well-defined on the torus.

## Relationship Between Maps

\\[
\begin{matrix}
    \mathbb{R}^2 & \xrightarrow{A} & \mathbb{R}^2 \\
    \downarrow \pi &  & \downarrow \pi \\
    \mathbb{R}^2 / \sim & \xrightarrow{\bar{A}} & \mathbb{R}^2 / \sim
\end{matrix}
\\]

## Matrix Representation of Curves on the Torus

Each curve on the torus can be represented by a vector \\( (p, q) \in \mathbb{R}^2 \\), where \\( p \\) and \\( q \\) are the winding numbers of the curve around meridian and longitude. A curve with vector \\( (p, q) \\) winds around the torus \\( p \\) times about the meridian and \\( q \\) times about the longitude.

Thus, the matrix \\( A \\) represents two curves on the torus:
\\[
A = \begin{bmatrix}
  p & p' \\
  q & q'
\end{bmatrix},
\\]
where the first column \\( (p, q) \\) represents the first curve, and the second column \\( (p', q') \\) represents the second curve.

The goal is to compute the intersection number of these two curves, which can be obtained by taking the absolute value of the determinant of the matrix \\( A \\).

## Intersection Number and Determinant

We start by considering two specific curves:
- The first curve is equivalent to the vertical line segment represented by \\( (0, 1) \\).
- The second curve is represented by the vector \\( (p', q') \\).

Since we are assuming \\( (p, q) = (0, 1) \\), the matrix becomes:
\\[
A = \begin{bmatrix} 0 & p' \\ 1 & q' \end{bmatrix}.
\\]

The determinant of this matrix is:
\\[
\det A = \det \begin{bmatrix} 0 & p' \\ 1 & q' \end{bmatrix} = (0 \cdot q') - (1 \cdot p') = -p'.
\\]
Thus, the absolute value of the determinant is:
\\[
\left| \det A \right| = |-p'| = p'.
\\]

{{< paige/scrolltotop >}}