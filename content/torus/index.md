+++
title = "Intersection Number of Two Curves on a Torus"
author = ["Victoria Ordonez"]
draft = false
+++

## Introduction

The approach is to simplify the computation of the geometric intersection number by applying a linear diffeomorphism \\( A \\) that preserves intersection numbers. Specifically:

1. Define the torus as the quotient space \\( \mathbb{R}^2 / \sim \\) using an equivalence relation.
2. Construct a linear diffeomorphism \\( A \\) with integer entries and determinant \\( \pm 1 \\).
3. Apply \\( A \\) to transform the given curves \\( (p, q) \\) and \\( (p', q') \\) into \\( (0, 1) \\) and \\( (p'', q'') \\), respectively.
4. Show that the geometric intersection number of the transformed curves is \\( |p''| \\), where \\( p'' \\) is the determinant of the matrix formed by the original curve coordinates.


## Mapping \\( \mathbb{R}^2 \\) to the Quotient Space \\( \mathbb{R}^2 / \sim \\)

Consider the universal cover of the torus, \\( \mathbb{R}^2 \\). The quotient space \\( \mathbb{R}^2 / \sim \\) is formed by identifying points whose difference is an integer vector.  
The equivalence relation \\( \sim \\) is defined as:

Two points \\( (x_1, y_1) \\) and \\( (x_2, y_2) \\) are equivalent under \\( \sim \\) if:

$$
(x_1, y_1) \sim (x_2, y_2) \iff (x_2 - x_1, y_2 - y_1) \in \mathbb{Z}^2.
$$

The quotient map \\( \pi : \mathbb{R}^2 \to \mathbb{R}^2 / \sim \\) is then defined as:

$$
\pi(x, y) = (x \mod 1, y \mod 1),
$$

which maps each point in \\( \mathbb{R}^2 \\) to its equivalence class on the torus. Geometrically, this means every point \\( (x, y) \in \mathbb{R}^2 \\) is mapped to a point inside the unit square \\( [0, 1) \times [0, 1) \\), representing a point on the torus.

## Defining the Map \\( A \\) on \\( \mathbb{R}^2 \\)

Let \\( A: \mathbb{R}^2 \to \mathbb{R}^2 \\) be a linear map represented by a \\( 2 \times 2 \\) matrix:

$$
A = \begin{bmatrix}
  a & b \\\\
  c & d
\end{bmatrix}.
$$

For any point \\( (x, y) \in \mathbb{R}^2 \\), the action of \\( A \\) is given by:

$$
A \begin{bmatrix} x \\\\ y \end{bmatrix} = \begin{bmatrix}
  ax + by \\\\
  cx + dy
\end{bmatrix}.
$$

To show that \\( A \\) is well-defined on the torus, we must check that if two points \\( (x, y) \\) and \\( (x + m, y + n) \\) are equivalent under \\( \sim \\), then their images under \\( A \\) are also equivalent.

Applying \\( A \\) to both points:

$$
A \begin{bmatrix} x + m \\\\ y + n \end{bmatrix} = \begin{bmatrix} a(x + m) + b(y + n) \\\\ c(x + m) + d(y + n) \end{bmatrix} = \begin{bmatrix} ax + by \\\\ cx + dy \end{bmatrix} + \begin{bmatrix} am + bn \\\\ cm + dn \end{bmatrix}.
$$

Since \\( m, n \in \mathbb{Z} \\), the second term \\( \begin{bmatrix} am + bn \\\\ cm + dn \end{bmatrix} \\) is also an integer vector. Therefore, the images of \\( (x, y) \\) and \\( (x + m, y + n) \\) under \\( A \\) differ by an integer vector, implying that they lie in the same equivalence class on the torus.

Thus, \\( A \\) respects the equivalence relation and defines a well-defined map on the torus.



## Relationship Between Maps

The following diagram illustrates how the map \\( A \\) interacts with the quotient map \\( \pi \\):

$$
\begin{matrix}
    \mathbb{R}^2 & \xrightarrow{A} & \mathbb{R}^2 \\\\
    \downarrow \pi &  & \downarrow \pi \\\\
    \mathbb{R}^2 / \sim & \xrightarrow{A} & \mathbb{R}^2 / \sim
\end{matrix}
$$


## Simplifying Intersection Computation with a Diffeomorphism

Let \\( C_1 \\) and \\( C_2 \\) be two curves on the torus, represented by \\( (p, q) \\) and \\( (p', q') \\), respectively, such that \\( \gcd(p,q) = 1 \\), \\( \gcd (p',q') = 1 \\) and \\( p, q, p', q' \in \mathbb{Z} \\).

If we restrict \\( A \\) to have determinant \\( \pm 1 \\), then \\( A \\) is invertible and acts as a diffeomorphism on the torus, preserving the intersection number. We want to choose \\( A \\) such that \\( A(C_1) = (0,1) \\) and \\( A(C_{2}) = (p'', q'') \\). 

This is because \\( (0,1) \\) represents the longitude of the torus, so it intersects a general curve \\( (p'', q'') \\) exactly \\( |p''| \\) times, as \\( p'' \\) corresponds to the number of times the curve wraps around the torus in the longitudinal direction. We will prove this in the next section. Thus, the intersection number of the transformed curves is:

$$
|(0,1) \cap (p'', q'')| = |p''|
$$

We let

$$
A = \begin{bmatrix}
  -q & p \\\\
  c + kq & d - kp 
\end{bmatrix},
$$

where \\( c, d, p, q, k \in \mathbb{Z} \\) and \\( \gcd(p, q) = 1, cp + dq = 1 \\).

We see 

$$
A \begin{bmatrix} p \\\\ q \end{bmatrix} =
\begin{bmatrix} -qp + pq  \\\\
(c + kq)p + (d - kp)q \end{bmatrix} =
\begin{bmatrix} 0 \\\\ 1 \end{bmatrix}.
$$

$$
A \begin{bmatrix} p' \\\\ q' \end{bmatrix} =
\begin{bmatrix}  -qp' + pq' \\\\
(c + kq)p' + (d - kp)q'
\end{bmatrix} =
\begin{bmatrix} p'' \\\\ q'' \end{bmatrix}.
$$

where

$$
p'' = pq' - qp', \quad  q'' = cp' + dq' + k(qp' - pq')
$$

The matrix formed by placing the coordinates of the original curves \\( (p, q) \\) and \\( (p', q') \\) as columns is:

$$
M = \begin{bmatrix} p & p' \\\\ q & q' \end{bmatrix}.
$$

The determinant of this matrix gives the second coordinate \\( p'' \\) of the transformed curve \\( (p'', q'') \\):

$$
\det M = pq' - p'q.
$$

Therefore, the geometric intersection number of the original curves \\( C_1 \\) and \\( C_2 \\) is given by:

$$
|C_1 \cap C_2| = \left| pq' - p'q \right|
$$




## Proof that \\(|(0,1) \cap (p, q)| = |p| \\)

### Counting intersections of the lifts of the curves within the unit square \\( [0,1)^2 \\) is equivalent to counting intersections of the curves on the torus

The lift of a curve \\( (p, q) \\) on the torus is the preimage of \\( (p, q) \\) under \\( \pi \\), which consists of all integer-shifted copies of the curve:

$$
\pi^{-1}(p, q) = \bigcup_{(m, n) \in \mathbb{Z}^2} [L_{(p, q)} + (m, n)]
$$

where \\( L_{(p, q)} \\) is a line with slope \\( \frac{q}{p} \\) and  \\( m, n \in \mathbb{Z} \\).

Let \\( U = [0,1)^2 \subseteq \mathbb{R}^2 \\), \\( B = \pi(U) \\), and define the map \\( g: [0,1)^2 \to B \\).

By showing that \\( g \\) is bijective, we establish that the unit square maps bijectively to the torus.

### Injectivity

Assume \\( g(x_1, y_1) = g(x_2, y_2) \\). This implies that the two points are equivalent under the quotient map \\( \pi \\), meaning:

$$
(x_1, y_1) \sim (x_2, y_2) \implies (x_1, y_1) - (x_2, y_2) \in \mathbb{Z}^2.
$$

Since both \\( (x_1, y_1) \\) and \\( (x_2, y_2) \\) lie within the unit square \\( [0,1)^2 \\), the only integer vector that satisfies the condition is \\( (0,0) \\). Thus, we must have:

$$
x_1 = x_2, \quad y_1 = y_2.
$$

### Surjectivity

Given any point \\( b \in B \\), by the definition of the torus, there exists a unique corresponding point \\( (x, y) \in [0,1)^2 \\) such that:

$$
g(x, y) = b.
$$

Thus, since \\( g \\) is bijective, we conclude that the intersection number between two curves on the torus is the same as the number of intersections of their lifts in the unit square.


## Intersection of \\(C\\) and \\(B\\)

Let 
$$
C = \bigcup_{(m,n) \in \mathbb{Z}^2} \left( L + (m,n) \right) \cap [0,1)^2
$$

and 

$$
C \cap B = \left\\{ (0, \frac{i}{p}) \mid 0 \leq i \leq p-1 \right\\}, \text{ where } i \in \mathbb{Z}.
$$



Also, 

$$
B = \bigcup_{(m,n) \in \mathbb{Z}^2} \left( L_{(0,1)} \right) \cap [0,1)^2,
$$

where \\( L_{(0,1)} \\) is the vertical line given by:

$$
L_{(0,1)} := \left\\{ (x,y) \in \mathbb{R}^2 \mid x = 0 \right\\}.
$$

Thus,

$$
C \cap B = \bigcup_{(m,n) \in \mathbb{Z}^2} \Big( L + (m,n) \Big) \cap  L_{(0,1)} \cap  [0,1)^2.
$$


#### \\( C \cap B \subseteq \left\\{ (0, \frac{i}{p}) \mid 0 \leq i \leq p-1 \right\\} \\)

Suppose \\( (x,y) \in C \cap B \\). By definition:

$$
C \cap B \subseteq C \cap \text{y-axis}
$$

The curve \\( C \\) consists of integer translations of the form:

$$
y = \frac{q}{p} x + (m,n)
$$

where \\( (m,n) \in \mathbb{Z}^2 \\).
Since the intersection occurs at \( x = 0 \),

$$
y = \frac{-qm + pn}{p}
$$

and since \\( y \in [0,1)^2 \\),

$$
0 \leq \frac{-qm + pn}{p} < 1.
$$

Thus,

$$
0 \leq \frac{i}{p} < 1, \quad \text{where } i = -qm + pn.
$$

Therefore, every element of \\( C \cap B \\) belongs to the set:

$$
\left\\{ \Big(0, \frac{i}{p} \Big) \mid 0 \leq i \leq p-1 \right\\}.
$$

#### \\( \left\\{ (0, \frac{i}{p}) \mid 0 \leq i \leq p-1 \right\\} \subseteq C \cap B \\)

Assume \\( (x,y) = \\left( 0, \\frac{i}{p} \\right) \\) for some \\( i \\) such that \\( 0 \leq i \leq p-1 \\).

By Bézout’s identity, since \\( p \\) and \\( q \\) are coprime, there exist integers \\( u, v \\) such that:

$$
qu + pv = 1.
$$

Multiplying by \\( i \\):

$$
q(ui) + p(vi) = i.
$$

Thus, choosing \\( (m,n) = (ui, vi) \\) ensures

$$
 -qm + pn = i.
$$

This implies that the point \\( \\left(0, \\frac{i}{p}\\right) \\) lies on the translated line \\( L + (m, n) \\). Since \\( m, n \in \mathbb{Z} \\), the translation \\( (m, n) \\) is valid, and \\( \\frac{i}{p} \in [0, 1) \\) for all \\( 0 \leq i \leq p-1 \\), meaning that the point \\( \\left(0, \\frac{i}{p}\\right) \\) belongs to \\( C \cap B \\).

Thus,

$$
\left\\{ \Big(0, \\frac{i}{p} \Big) \\mid 0 \leq i \leq p-1 \right\\} \subseteq C \cap B.
$$

 

## Supplemental: Characterizing Line Translations

### Conditions for Translations of a Set in a Strip
We define the strip as:

$$
\text{strip} = \left\\{ (x, y) \in \mathbb{R}^2 \mid \frac{q}{p}(x - 1) \leq y < \frac{q}{p}x + 1 \right\\}.
$$

Consider the set 

$$
L = \left\\{ (x,y) \mid y = \tfrac{q}{p}x \right \\}
$$

and the translated set \\( (m,n) + L \\), which consists of points of the form:

$$
\ell + (m,n) = (x, \tfrac{q}{p}x) + (m, n) = (x + m, \tfrac{q}{p}x + n).
$$

### **When does \\( (m,n) + L \subset \text{strip} \\)?**

#### **\\((m,n) + L \subseteq \text{strip} \quad \Longleftrightarrow \quad (m,n) \in \text{strip}\\)**

#### **\\( (\Rightarrow) \\)**
Assume that \\( (m,n) + L \subseteq \text{strip} \\). Since \\( L \\) contains the origin \\( (0,0) \\), we have:

$$
(0,0) + (m,n) = (m,n) \in (m,n) + L.
$$

Since every point in \\( (m,n) + L \\) is contained within the strip, it follows that \\( (m,n) \in \text{strip} \\).

#### **\\( (\Leftarrow) \\)**
Now assume that \\( (m,n) \in \text{strip} \\). This means that \\( (m,n) \\) satisfies:

$$
\frac{q}{p}(m - 1) \leq n < \frac{q}{p}m + 1.
$$

We must check that:

$$
\frac{q}{p}((x + m) - 1) \leq \frac{q}{p}x + n < \frac{q}{p}(x + m) + 1.
$$

$$
\frac{q}{p}x + \frac{q}{p}m - \frac{q}{p} \leq \frac{q}{p}x + n < \frac{q}{p}x + \frac{q}{p}m + 1
$$

$$
\frac{q}{p}m - \frac{q}{p} \leq n <  \frac{q}{p}m + 1 \quad  \subset  \quad \text{strip}.
$$

Thus, \\( (m,n) + L \subset \text{strip} \\).

### **When are two integer shifts of L the same?**

#### **\\( L+ w = L + v \iff v = w + n(p,q), \quad \text{ where } n \in \mathbb{Z} \\)**

### **\\( (\Rightarrow) \\)**

Suppose \\( L + w = L + v \\). Then,

$$
L + w = L + v.
$$

$$
L + (w - v) = L.
$$

Thus, we see that \\( (w - v) \\) lies on \\( L \\), meaning that \\( w - v \\) is a point on the line \\( L \\). We can write:

$$
w - v = (x, x \cdot \frac{q}{p}).
$$

$$
w - v = x \left(1, \frac{q}{p} \right).
$$

$$
w - v = \frac{x}{p} (p, q).
$$

$$
w - v = n (p,q),
$$

where \\( n \in \mathbb{Z} \\) and \\( n = \frac{x}{p} \\), since \\( p|xq \\) and  \\( (p,q) = 1 \\), so  \\( p|x \\). 


### **\\( (\Leftarrow) \\)**

Now, suppose:

$$
v = w + n(p,q).
$$

We need to show \\( L + v = L + w + n(p,q) \\):

$$
\frac{q}{p} x + (v_1, v_2) = \frac{q}{p} x + (w_1, w_2) + n (p,q).
$$

$$
\frac{q}{p} (x - v_1) + v_2 = \frac{q}{p} (x - w_1 - np) + (w_2 + nq).
$$

$$
\frac{q}{p} x - w_1 \frac{q}{p} - \frac{q}{p} (np) + w_2 + nq = \frac{q}{p} x - w_1 \frac{q}{p} + w_2.
$$

$$
\frac{q}{p} (x - w_1) + w_2 = L + w.
$$

Thus, 

$$
L + v = L + w.
$$

#### \\(|C| = |p + q - 1| \\)

We will now show there are \\(p+q-1\\)  distinct intersections of the integer shifts of the line \\(L\\) with the unit square.

For each integer shift \\(m \in \mathbb{Z}\\), the x-intercepts and y-intercepts repeat every \\(\frac{1}{p}\\) and \\(\frac{1}{q}\\), respectively. Therefore, the x-intercepts within the unit square are:

$$
   \left \\{0, \frac{1}{p}, \frac{2}{p}, \dots, \frac{p-1}{p} \right \\}
   $$
This gives \\(p\\) evenly spaced x-intercepts. The y-intercepts within the unit square are:

$$
   \left \\{0, \frac{1}{q}, \frac{2}{q}, \dots, \frac{q-1}{q}\right \\}
   $$

This gives \\(q\\) evenly spaced y-intercepts.

The total number of intersections of the line \\(L\\) with the unit square edges is the sum of these horizontal and vertical crossings. However, the point at the origin \\((0,0)\\) is double-counted as both an x and y-intercept.

