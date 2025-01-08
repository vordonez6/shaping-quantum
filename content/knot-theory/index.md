+++
title = "Knot Theory"
author = ["Victoria Ordonez"]
draft = false
+++

# Elementary Knot Moves

**Elementary knot moves** are reversible changes to the shape of a knot made by modifying its edges. 


## Operations:

\[
(1) \quad \text{Place a point } C \text{ on an edge } AB, \text{ dividing it into two edges } AC \text{ and } CB
\]

\[
(1)' \quad \text{If } AC \text{ and } CB \text{ are adjacent edges such that removing } C \text{ results in a straight line } AB, \text{ then } C \text{ may be erased, restoring the edge } AB
\]


<div class="centered_image">
{{< paige/figure caption="(1) & (1)'" >}}
{{< paige/image alt="Landscape" breakpoints=true class="object-fit-cover rounded-4" fetchpriority="high" height="20rem" loading="eager" process="webp" src="./knotpics/1.png" width="100%" >}}
{{< /paige/figure >}}
</div>

\[
(2) \quad \text{For a point } C \text{ that doesn't lie on the knot } K, \text{ if the triangle } \triangle ABC, \text{ formed by } AB \text{ and } C, \text{ does not intersect } K \text{ (except at } AB\text{), then replace } AB \text{ with two new edges } AC \text{ and } CB
\]

\[
(2)' \quad \text{If } \triangle ABC \text{ contains two adjacent edges } AC \text{ and } CB, \text{ and this triangle does not intersect } K \text{ (except at } AC \text{ and } CB\text{), then } AC \text{ and } CB \text{ may be removed and replaced with } AB
\]


<div class="centered_image">
{{< paige/figure caption="(2) & (2)'" >}}
{{< paige/image alt="Landscape" breakpoints=true class="object-fit-cover rounded-4" fetchpriority="high" height="20rem" loading="eager" process="webp" src="./knotpics/2.png" width="100%" >}}
{{< /paige/figure >}}+
</div>

These four operations \((1), (1)', (2), (2)'\) are called *elementary knot moves*.

**Note:** Typically, only \((2)\) and \((2)'\) are referred to as elementary knot moves, as they involve actual transformations or "moves." Operations \((1)\) and \((1)'\) are adjustments to the knot structure and are thus not considered moves in the usual sense. 



# The Equivalence of Knots

Knots that can be changed from one to the other by applying elementary knot moves are said to be *equivalent*. Two knots are equivalent if we can alter one continuously, without causing any self-intersections, until it is transformed into the other knot.



## Homeomorphisms

Let \( f \) be a bijective map from a topological space \( X \) to a topological space \( Y \). Let \( f^{-1} \) be the inverse map \( f^{-1}: Y \to X \). When both \( f \) and \( f^{-1} \) are continuous maps, then the map \( f \) is a *homeomorphism*.
When \( X \) and \( Y \) have orientations assigned to them, we say \( f \) is an *orientation-preserving homeomorphism* if the original orientation of \( Y \) agrees with the orientation on \( Y \). 
A homeomorphism from \( X \) to itself is called an *auto-homeomorphism*.

### Examples

Let \( X \) and \( Y \) be \( \mathbb{R}^2 \). The parallel translation along a line, given by \( (x, y) \mapsto (x + a, y + b) \), and a rotation about some fixed point are examples of orientation-preserving auto-homeomorphisms, as shown in the figure below.


<div class="centered_image">
{{< paige/figure caption="Orientation-preserving Auto-homeomorphisms" >}}
{{< paige/image alt="Landscape" breakpoints=true class="object-fit-cover rounded-4" fetchpriority="high" height="20rem" loading="eager" process="webp" src="./knotpics/3.png" width="100%" >}}
{{< /paige/figure >}}+
</div>

However, the mirror image with respect to the \( x \)-axis, given by the homeomorphism \( f(x, y) = (x, -y) \), is not an orientation-preserving auto-homeomorphism. In fact, the orientation is reversed, as illustrated in the figure below. 


<div class="centered_image">
{{< paige/figure caption="Non Orientation-preserving Auto-homeomorphisms" >}}
{{< paige/image alt="Landscape" breakpoints=true class="object-fit-cover rounded-4" fetchpriority="high" height="20rem" loading="eager" process="webp" src="./knotpics/4.png" width="100%" >}}
{{< /paige/figure >}}+
</div>

Thus, we can say two knots \( K_1 \) and \( K_2 \) are *equivalent* if there exists an orientation-preserving homeomorphism of \( \mathbb{R}^3 \) that maps \( K_1 \) to \( K_2 \).

Since there exists a one-to-one correspondence between the 2-dimensional sphere \( \mathbb{S}^2 \), excluding the North Pole, \( N \), and the entire plane, \( \mathbb{R}^2 \), \( \mathbb{R}^2 \cup \{\infty\} \) and \( \mathbb{S}^2 \) are homeomorphic as shown below.


<div class="centered_image">
{{< paige/figure caption="\(\mathbb{R}^2 \cup \{\infty\} \cong \mathbb{S}^2\)" >}}
{{< paige/image alt="Landscape" breakpoints=true class="object-fit-cover rounded-4" fetchpriority="high" height="20rem" loading="eager" process="webp" src="./knotpics/5.png" width="100%" >}}
{{< /paige/figure >}}+
</div>

Similarly, the 3-dimensional sphere \( \mathbb{S}^3 \) is often thought of as \( \mathbb{R}^3 \cup \{\infty\} \). Thus, we can think of a knot lying in \( \mathbb{S}^3 \) rather than in \( \mathbb{R}^3 \) as long as the knot \( K \) does not contain the point at infinity. Therefore, if two equivalent knots \( K_1 \) and \( K_2 \) lie in \( \mathbb{S}^3 \), then their complements \( \mathbb{S}^3 - K_1 \) and \( \mathbb{S}^3 - K_2 \) are homeomorphic.



# Links

A *link* is a finite, ordered collection of knots that do not intersect each other. Each knot \( K_i \) is called a *component* of the link.

Two links \( L = \{K_1, K_2, \ldots, K_m\} \) and \( L' = \{K'_1, K'_2, \ldots, K'_n\} \) are *equivalent* if:

1. \( m = n \) (\( L \) and \( L' \) have the same number of components)
2. There exists an auto-homeomorphism, \( \varphi \) such that \( \varphi(K_1 \cup \ldots \cup K_m)=K'_1 \cup \ldots \cup K'_m \) preserves the orientation of \( \mathbb{R}^3 \).

Two links \( L \) and \( L' \) are equivalent if we can transform \( L \) into \( L' \) by performing elementary knot moves, where the triangle involved in a given elementary knot move must not intersect any of the other components.
