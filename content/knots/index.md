+++
title = "Knot Theory"
author = ["Victoria Ordonez"]
draft = false
+++

## Elementary Knot Moves

**Elementary knot moves** are reversible changes to the shape of a knot made by modifying its edges.


### Operations

\\[(1) \quad \text{Place a point } C \text{ on an edge } AB, \text{ dividing it into two edges } AC \text{ and } CB\\]

\\[(1)' \quad \text{If } AC \text{ and } CB \text{ are adjacent edges such that removing } C \text{ results in a straight line } AB, \text{ then } C \text{ may be erased, restoring the edge } AB\\]


<div class="centered_image">
{{< paige/figure caption="(1) & (1)'" >}}
{{< paige/image alt="Landscape" breakpoints=true class="object-fit-cover rounded-4" fetchpriority="high" height="20rem" loading="eager" process="webp" src="./knotpics/1&1.svg" width="100%" >}}
{{< /paige/figure >}}
</div>

\\[(2) \quad \text{For a point } C \text{ that doesn't lie on the knot } K, \text{ if the triangle } \triangle ABC, \text{ formed by } AB \text{ and } C, \text{ does not intersect } K \text{ (except at } AB\text{), then} \\ \text{replace } AB \text{ with two new edges } AC \text{ and } CB\\]


\\[
(2)' \quad \text{If } \triangle ABC \text{ contains two adjacent edges } AC \text{ and } CB, \text{ and this triangle does not intersect } K \text{ (except at } AC \text{ and } CB\text{), then } AC \text{ and } CB \text{ may be removed and replaced with } AB
\\]

<div class="centered_image">
{{< paige/figure caption="(2) & (2)'" >}}
{{< paige/image alt="Landscape" breakpoints=true class="object-fit-cover rounded-4" fetchpriority="high" height="20rem" loading="eager" process="webp" src="./knotpics/2&2.svg" width="100%" >}}
{{< /paige/figure >}}
</div>

These four operations \\((1), (1)', (2), (2)'\\) are called *elementary knot moves*.

**Note:** Typically, only \\((2)\\) and \\((2)'\\) are referred to as elementary knot moves, as they involve actual transformations or "moves." Operations \\((1)\\) and \\((1)'\\) are adjustments to the knot structure and are thus not considered moves in the usual sense. 


## The Equivalence of Knots

Knots that can be changed from one to the other by applying elementary knot moves are said to be *equivalent*. Two knots are equivalent if we can alter one continuously, without causing any self-intersections, until it is transformed into the other knot.

### Homeomorphisms

Let \\( f \\) be a bijective map from a topological space \\( X \\) to a topological space \\( Y \\). Let \\( f^{-1} \\) be the inverse map \\( f^{-1}: Y \to X \\). When both \\( f \\) and \\( f^{-1} \\) are continuous maps, then the map \\( f \\) is a *homeomorphism*.
When \\( X \\) and \\( Y \\) have orientations assigned to them, we say \\( f \\) is an *orientation-preserving homeomorphism* if the original orientation of \\( Y \\) agrees with the orientation on \\( Y \\). 

#### Examples

Let \\( X \\) and \\( Y \\) be \\( \mathbb{R}^2 \\). The parallel translation along a line, given by \\( (x, y) \mapsto (x + a, y + b) \\), and a rotation about some fixed point are examples of orientation-preserving auto-homeomorphisms, as shown in the figure below.

<div class="centered_image">
{{< paige/figure caption="Orientation-preserving Auto-homeomorphisms" >}}
{{< paige/image alt="Landscape" breakpoints=true class="object-fit-cover rounded-4" fetchpriority="high" height="20rem" loading="eager" process="webp" src="./knotpics/orientation-preserving-auto-homeomorphisms.svg" width="100%" >}}
{{< /paige/figure >}}
</div>

However, the mirror image with respect to the \\( x \\)-axis, given by the homeomorphism \\( f(x, y) = (x, -y) \\), is not an orientation-preserving auto-homeomorphism. In fact, the orientation is reversed, as illustrated in the figure below. 


<div class="centered_image">
{{< paige/figure caption="Non Orientation-preserving Auto-homeomorphisms" >}}
{{< paige/image alt="Landscape" breakpoints=true class="object-fit-cover rounded-4" fetchpriority="high" height="20rem" loading="eager" process="webp" src="./knotpics/non_orientation_preserving_auto-homeomorphisms.svg" width="100%" >}}
{{< /paige/figure >}}
</div>


Thus, we can say two knots \\( K\_1 \\) and \\( K\_2 \\) are *equivalent* if there exists an orientation-preserving homeomorphism of \\( \mathbb{R}^3 \\) that maps \\( K\_1 \\) to \\( K\_2 \\).

Since there exists a one-to-one correspondence between the 2-dimensional sphere \\( \mathbb{S}^2 \\), excluding the North Pole, \\( N \\), and the entire plane, \\( \mathbb{R}^2 \\), \\( \mathbb{R}^2 \cup \{\infty\} \\) and \\( \mathbb{S}^2 \\) are homeomorphic as shown below.


<div class="centered_image">
{{< paige/figure caption="\\(\mathbb{R}^2 \cup \{\infty\} \cong \mathbb{S}^2\\)" >}}
{{< paige/image alt="Landscape" breakpoints=true class="object-fit-cover rounded-4" fetchpriority="high" height="20rem" loading="eager" process="webp" src="./knotpics/sphere.svg" width="100%" >}}
{{< /paige/figure >}}
</div>

Similarly, the 3-dimensional sphere \\( \mathbb{S}^3 \\) is often thought of as \\( \mathbb{R}^3 \cup \{\infty\} \\). Thus, we can think of a knot lying in \\( \mathbb{S}^3 \\) rather than in \\( \mathbb{R}^3 \\) as long as the knot \\( K \\) does not contain the point at infinity. Therefore, if two equivalent knots \\( K\_1 \\) and \\( K\_2 \\) lie in \\( \mathbb{S}^3 \\), then their complements \\( \mathbb{S}^3 - K\_1 \\) and \\( \mathbb{S}^3 - K\_2 \\) are homeomorphic.

## Links

A *link* is a finite, ordered collection of knots that do not intersect each other. Each knot \\( K\_i \\) is called a *component* of the link.

Two links \\( L = \{K\_1, K\_2, \ldots, K\_m\}  \text{ and }  L' = \{K'\_1, K'\_2, \ldots, K'\_n\} \\) are *equivalent* if:

1. \\( m = n \text{  } \\) (\\( L \\) and \\( L' \\) have the same number of components)
2. There exists an auto-homeomorphism, \\( \varphi \\) such that \\( \varphi(K\_1 \cup \ldots \cup K\_m)=K'\_1 \cup \ldots \cup K'\_m \\) preserves the orientation of \\( \mathbb{R}^3 \\).

Two links \\( L \\) and \\( L' \\) are equivalent if we can transform \\( L \\) into \\( L' \\) by performing elementary knot moves, where the triangle involved in a given elementary knot move must not intersect any of the other components.

### Examples

<div class="centered_image">
{{< paige/figure caption="Equivalent Links" >}}
{{< paige/image alt="Landscape" breakpoints=true class="object-fit-cover rounded-4" fetchpriority="high" height="20rem" loading="eager" process="webp" src="./knotpics/tref2.svg" width="100%" >}}
{{< /paige/figure >}}
</div>

Consider the links above and let us assign an orientation to the links \\( L \\) and \\( L' \\) as shown below.

<div class="centered_image">
{{< paige/figure caption="Non-equivalent Links" >}}
{{< paige/image alt="Landscape" breakpoints=true class="object-fit-cover rounded-4" fetchpriority="high" height="20rem" loading="eager" process="webp" src="./knotpics/tref3.svg" width="100%" >}}
{{< /paige/figure >}}
</div>

We see that the second condition doesn't hold anymore and thus these oriented links are not equivalent.

## Trivial \\(n\\)-component Link

Only one trivial \\(n\\)-component link for each \\(n\\) exists, since orienting the trivial link has no effect on its equivalence.



<div class="centered_image">
{{< paige/figure caption="Trivial \(n\)-component Link" >}}
{{< paige/image alt="Landscape" breakpoints=true class="object-fit-cover rounded-4" fetchpriority="high" height="20rem" loading="eager" process="webp" src="./knotpics/trivial_n_component_link.svg" width="100%" >}}
{{< /paige/figure >}}
</div>

# Knot Decomposition

## \\( (1, 1) \\)-tangle

Let us consider a ball \\( B^3 \\) bounded by \\( S \\), a sphere \\( S \\) in \\( \mathbb{S}^3 \\). Let \\( \alpha \\) be a curve inside \\( B^3 \\) 
whose endpoints \\( A \\) and \\( B \\) lie on the surface of \\( S \\). If \\( \alpha \\) intersects \\( S \\) only at the points \\( A \\) and \\( B \\), it is called a \\( (1, 1) \\)-tangle as shown below.


<div class="centered_image">
{{< paige/figure caption="\( (1, 1)\)-tangle" >}}
{{< paige/image alt="Landscape" breakpoints=true class="object-fit-cover rounded-4" fetchpriority="high" height="20rem" loading="eager" process="webp" src="./knotpics/1-1_tangle.svg" width="100%" >}}
{{< /paige/figure >}}
</div>

**Note:** A \\( (1, 1) \\)-tangle may have disjoint simple closed curves.

Now, applying elementary knot moves to segments of the knotted \\( (1, 1) \\)-tangle, \\( \alpha \\), while keeping \\( A \\) and \\( B \\) fixed, \\( \alpha \\) becomes the \\( (1, 1) \\)-tangle shown below.

<div class="centered_image">
{{< paige/figure caption="Trivial \\( (1, 1)\\)-tangle" >}}
{{< paige/image alt="Landscape" breakpoints=true class="object-fit-cover rounded-4" fetchpriority="high" height="20rem" loading="eager" process="webp" src="./knotpics/trivial_tangle.svg" width="100%" >}}
{{< /paige/figure >}}
</div>

## Decomposing a Knot into Two Simpler Knots

Let \\( K \\) be a knot (link) in \\( \mathbb{S}^3 \\) and let \\( \Sigma \\) be a 2-dimensional sphere that intersects \\( K \\) at right angles at exactly two points \\( A \\) and \\( B \\). 

Because \\( K \\) lies in \\( \mathbb{S}^3 \\), it is divided by \\( \Sigma \\) into two \\( (1, 1) \\)-tangles \\( \alpha \\) and \\( \beta \\), one of which lies inside \\( \Sigma \\) and the other outside, as shown in the figure below. 
\\( \Sigma \\) becomes the boundary of two 3-dimensional balls: one formed by \\( \Sigma \\) and its interior, and the other by \\( \Sigma \\) and its exterior. Thus, \\( \mathbb{S}^3 \\) is composed of two 3-dimensional balls glued together along their common boundary, \\( \Sigma \\).

<div class="centered_image">
{{< paige/figure caption="Knot Decomposition" >}}
{{< paige/image alt="Landscape" breakpoints=true class="object-fit-cover rounded-4" fetchpriority="high" height="20rem" loading="eager" process="webp" src="./knotpics/pretzelandstart.svg" width="100%" >}}
{{< /paige/figure >}}
</div>

We then connect \\( A \\) to \\( B \\) by means of a simple polygonal line \\( s \\) that lies on \\( \Sigma \\), obtaining a knot \\( K\_1 \\), and by joining \\( s \\) to \\( \beta \\), we obtain a knot \\( K_2 \\).

If we connect \\( A \\) to \\( B \\) by another simple polygonal line \\( s' \\) lying on \\( \Sigma \\), we obtain two knots \\( K'\_1 \\) and \\( K'\_2 \\). By applying elementary knot moves to \\( s \\) on \\( \Sigma \\), we can transform it into \\( s' \\), thus \\( K\_1 \\) and \\( K'\_1 \\), as well as \\( K\_2 \\) and \\( K'\_2 \\) are equivalent.

If one of the tangles is a trivial \\( (1, 1) \\)-tangle, then its corresponding knot is the trivial knot. We see below that in this case, \\( K \\) and \\( K_{1} \\) are equivalent, meaning \\( K \\) is not a true decomposition.

<div class="centered_image">
{{< paige/figure caption="Knot Decomposition w/ trivial knot" >}}
{{< paige/image alt="Landscape" breakpoints=true class="object-fit-cover rounded-4" fetchpriority="high" height="20rem" loading="eager" process="webp" src="./knotpics/tref4.svg" width="100%" >}}
{{< /paige/figure >}}
</div>

## Prime Knot

When a true (non-trivial) decomposition cannot be found for \\( K \\), \\( K \\) is a *prime knot*. This means a knot \\( K \\) is either a prime knot or can be decomposed into at least two non-trivial knots, which in turn are either themselves prime knots or can be further decomposed into non-trivial knots.


{{< paige/scrolltotop >}}
