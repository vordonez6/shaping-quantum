+++
title = "Jones Polynomial"
weight = 50
author = ["Victoria Ordonez"]
draft = false
+++


The Jones polynomial associates a Laurent polynomial with integer coefficients to every knot and link. This polynomial is invariant under Reidemeister moves, making it a useful tool for distinguishing knots.

In order to define the Jones polynomial, we first need to define the Kauffman Bracket.

## The Kauffman Bracket

The Kauffman bracket is a function from unoriented link diagrams in the oriented plane (or \\( S^2 \\)) to Laurent polynomials with integer coefficients in an indeterminate \\( A \\). It maps a diagram \\( D \\) to \\( \langle D \rangle \in \mathbb{Z}[A^{-1}, A] \\) and is characterized by:

<div class="centered_image">
  {{< paige/figure caption="Kauffman Bracket" >}}
  {{< paige/image alt="Kauffman Bracket" breakpoints=true class="object-fit-cover rounded-4" fetchpriority="high" height="20rem" loading="eager" process="webp" src="./jonespics/kauff1.svg" width="100%" >}}
  {{< /paige/figure >}}
</div>

Where \\( \bigcirc \\) is the unknot and \\( D \sqcup \bigcirc \\) consists of the diagram \\( D \\) along with an additional closed curve that does not cross itself or \\( D \\). The skein relation (iii) expresses how the polynomial changes when resolving a crossing.

The bracket polynomial of a diagram with \\( n \\) crossings can be computed by resolving crossings recursively, reducing it to a sum of \\( 2^n \\) crossing-free diagrams. If a diagram has \\( c \\) components and no crossings, its polynomial follows as \\( (-A^{-2} - A^2)^{c-1} \\).

The ordering of crossing resolutions does not affect the final result, ensuring the well-defined nature of the Kauffman bracket. If an orientation-preserving homeomorphism of the plane is applied to the diagram, the polynomial remains unchanged.

We will now analyze the effect of Reidemeister moves on the bracket polynomial.

## Effect of Reidemeister Moves

If a diagram is changed by a **Type I Reidemeister** move, its bracket polynomial changes as follows:

<div class="centered_image">
  {{< paige/figure caption="After Type I Reidemeister" >}}
  {{< paige/image alt="After Type I Reidemeister" breakpoints=true class="object-fit-cover rounded-4" fetchpriority="high" height="20rem" loading="eager" process="webp" src="./jonespics/kauff2.svg" width="100%" >}}
  {{< /paige/figure >}}
</div>

<div class="centered_image">
  {{< paige/figure caption="After Type I Reidemeister Proof" >}}
  {{< paige/image alt="After Type I Reidemeister Proof" breakpoints=true class="object-fit-cover rounded-4" fetchpriority="high" height="20rem" loading="eager" process="webp" src="./jonespics/kauff3.svg" width="100%" >}}
  {{< /paige/figure >}}
</div>

This follows from an application of the skein relation. If the crossing were reversed, the formula remains the same except for an interchange of \\( A \\) and \\( A^{-1} \\). This symmetry results from rotating the skein relation by \\( \pi/2 \\). If \\( D' \\) is the reflection of \\( D \\) (with all crossings flipped), then \\( \langle D' \rangle \\) is obtained by exchanging \\( A \\) and \\( A^{-1} \\) in \\( \langle D \rangle \\).

This lemma is used in subsequent calculations, including the bracket polynomial of a two-component link and a trefoil knot. For example:

<div class="centered_image">
  {{< paige/figure caption="Two-Component Link Bracket Polynomial" >}}
  {{< paige/image alt="Two-Component Link" breakpoints=true class="object-fit-cover rounded-4" fetchpriority="high" height="20rem" loading="eager" process="webp" src="./jonespics/kauff4.svg" width="100%" >}}
  {{< /paige/figure >}}
</div>

For the trefoil knot:

<div class="centered_image">
  {{< paige/figure caption="Trefoil Knot Bracket Polynomial" >}}
  {{< paige/image alt="Trefoil Knot" breakpoints=true class="object-fit-cover rounded-4" fetchpriority="high" height="20rem" loading="eager" process="webp" src="./jonespics/kauff5.svg" width="100%" >}}
  {{< /paige/figure >}}
</div>


{{< paige/scrolltotop >}}
