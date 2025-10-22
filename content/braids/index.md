+++
title = "Braids"
weight = 30
author = ["Victoria Ordonez"]
draft = false
+++

## Introduction {#introduction}

The best way to visualize a braid is to imagine a cube, B, whose coordinates
in \\(\mathbb{R}^{3}\\) can be defined as followed: \\[ B = \\{(x,y,z)|0 \leq x,y,z
  \leq 1\\}\\] At the top of the cube and at the base of the cube, we will mark
\\(n\\) points, \\(A\_{1},...,A\_{n}\\) and \\(A^{'}\_{1}, ... ,A^{'}\_{n}\\),
respectively. Let,

\begin{align\*}
A\_{1} &=\left(\frac{1}{2}, \frac{1}{n+1},1 \right), ... , A\_{n} = \left( \frac{1}{2}, \frac{n}{n+1},1 \right)   \\\\
A^{'}\_{1} &=\left(\frac{1}{2}, \frac{1}{n+1},0\right), ... ,A^{'}\_{n} =   \left(\frac{1}{2},\frac{n}{n+1},0 \right)
\end{align\*}

<div class="centered_image">
{{< paige/figure caption="Cube B" >}}
{{< paige/image alt="Landscape" breakpoints=true class="object-fit-cover rounded-4" fetchpriority="high" height="20rem" loading="eager" process="webp" src="./images/cube_b.svg" width="100%" >}}
{{< /paige/figure >}}
</div>

These points will act as fixed endpoints at the top and bottom of the cube,
which we will join with \\(n\\) polygonal arcs. \\(A\_{1},...,A\_{n}\\) to \\(A^{'}\_{1},
... ,A^{'}\_{n}\\) are joined with \\(n\\) polygonal arcs, such that:

\\(\hspace{1cm}\enclose{circle}{1}\\) The joined polygonal arcs do not mutually intersect each other <br />
\\(\hspace{1cm}\enclose{circle}{2}\\) \\(A\_{i}\\) to \\(A\_{j}\\) cannot be joined  <br />
\\(\hspace{1cm}\enclose{circle}{3}\\) \\(A\_{i}\\) to \\(A^{'}\_{i}\\) don't have to be joined, meaning \\(A\_{i}\\) can be joined to \\(A^{'}\_{j}\\) <br />
\\(\hspace{1cm}\enclose{circle}{4}\\) If we were to take any plane,\\(E\\), that's parallel to the top and bottom of the cube, \\(E\\) should intersect each polygonal arc at one and only one point <br />

<div class="centered_image">
{{< paige/figure caption="Braid" >}}
{{< paige/image alt="Landscape" breakpoints=true class="object-fit-cover rounded-4" fetchpriority="high" height="20rem" loading="eager" process="webp" src="./images/b2.svg" width="100%" >}}
{{< /paige/figure >}}
</div>

You can think of \\(\enclose{circle}{4}\\) as stating that the polygonal arcs cannot
go down the cube and then back up, considering that if that were to happen a
plane \\(E\\) would intersect the arc at more than one point. Let's call these
polygonal arcs, strings. After dividing \\(B\\) by \\(E\\), we can say these \\(n\\) strings
in \\(B\\) are an \\(n-braid\\).


### Regular Diagram of Braid {#regular-diagram-of-braid}

Just like with knots, it is easier to work with projections of n-braids than
the actual braid. Therefore, in order to obtain a regular diagram of the
braid we can project it onto the \\(y-z\\) plane. Figure "Regular Diagram of Braid" is the projection
of Figure "Equivalent Braids with Fixed Endpoints" onto the \\(y-z\\) plane.

<div class="centered_image">
{{< paige/figure caption="Regular Diagram of Figure" >}}
{{< paige/image alt="Landscape" breakpoints=true class="object-fit-cover rounded-4" fetchpriority="high" height="30rem" loading="eager" process="webp" src="./images/b3.svg" width="100%" >}}
{{< /paige/figure >}}
</div>


### Trivial n-Braid {#trivial-n-braid}

We will later see in the section about Alexander's Theorem  that we can use the 1-strand trivial braid
to create the unknot, so in a way, just like there exists the unknot, there
also exists the trivial braid.  If we were to connect \\(A\_{1}\\) to \\(A^{'}\_{1}\\),
\\(A\_{2}\\) to \\(A^{'}\_{2}\\), ..., \\(A\_{n}\\) to \\(A^{'}\_{n}\\),with straight strings, we
would get the trivial n-braid:

<div class="centered_image">
{{< paige/figure caption="Trivial Braid" >}}
{{< paige/image alt="Landscape" breakpoints=true class="object-fit-cover rounded-4" fetchpriority="high" height="20rem" loading="eager" process="webp" src="./images/trivial_braid.svg" width="100%" >}}
{{< /paige/figure >}}
</div>


### Elementary Moves &amp; Braids {#elementary-moves-and-braids}

Suppose we are given two n-braids in a cube. If performing elementary knot
moves to the strings of each braid, such that the endpoints remain fixed and
the strings remain in the cube, transforms one braid into the other, then the
two n-braids are equivalent.

The figure below shows an example of elementary moves being applied to (a) to
demonstrate that it is the trivial 2-braid.

<div class="centered_image">
{{< paige/figure caption="Trivial 2-Braid" >}}
{{< paige/image alt="Landscape" breakpoints=true class="object-fit-cover rounded-4" fetchpriority="high" height="20rem" loading="eager" process="webp" src="./images/b4.svg" width="100%" >}}
{{< /paige/figure >}}
</div>

Similarly, two braids whose endpoints are fixed can be said to be equivalent if
they can continuously be deformed from one to the other without any of the
strings intersecting each other as seen in Figure "Equivalent Braids with Fixed Endpoints".

<div class="centered_image">
{{< paige/figure caption="Equivalent Braids with Fixed Endpoints" >}}
{{< paige/image alt="Landscape" breakpoints=true class="object-fit-cover rounded-4" fetchpriority="high" height="20rem" loading="eager" process="webp" src="./images/b5.svg" width="100%" >}}
{{< /paige/figure >}}
</div>


### Braid Permutation {#braid-permutation}

Suppose a n-braid, \\(\alpha\\), has strings connected such that \\(A\_{1}\\) connects
to \\(A^{'}\_{i\_{1}}\\), \\(A\_{2}\\) connects to \\(A^{'}\_{i\_{2}}\\), more generally,
\\(A\_{j}\\) connects to \\(A^{'}\_{i\_{j}}\\). We can assign \\(\alpha\\) a permutation:

\begin{pmatrix}
 1 & 2 & . & . & . & n\\\\
 i\_{1} & i\_{2} & . & . & . & i\_{n}
\end{pmatrix}

\\[{\text{Braid Permutation of  } \alpha}\\]

This permutation is called the braid permutation and is a braid
invariant. Another way to think about the permutation of a braid is to imagine
the first row to be the strings of the braid and the second row to be the
endpoints of each of the respective strings. In other words, for \\(\alpha\\), we
know the first string ends up at endpoint \\(i\_{1}\\), the second string ends up at
endpoint \\(i\_{2}\\), and so on. Every single braid has a braid permutation. For
example:

\\(\hspace{1cm}\\) The trivial braid (Figure "Trivial Braid") corresponds to the identity
permutation:

\begin{pmatrix}
1 & 2 & . & . & . & n\\\\
1 & 2 & . & . & . & n
\end{pmatrix}

\\[{ \text{Identity  Permutation}}\\]

\\(\hspace{1cm}\\) The braid in Figure "Braid" has the braid permutation:

\begin{pmatrix}
 1 & 2\\\\
 2 & 1
\end{pmatrix}

\\[{\text{Braid Permutation of Figure "Braid"}}\\]


## Braid Group (\\(B\_{n}\\)) {#braid-group--b-n}

\\(\hspace{1cm}\\) Let \\(B\_{n}\\) be the set of all n-braids, ie. all the equivalence
classes of these braids, where \\(n\\) is the number of strings in the braids. Just
like with every group, the braid group has an operation, an identity element, an
inverse, and has associativity under the operation.

\\(\hspace{1cm}\\) The operation of the braid group is the product of two elements
in \\(B\_{n}\\), where both elements have the same number of \\(n\\) strings. In order to
define the product of these two elements, let's take two n-braids \\(\alpha\\) and
\\(\beta\\). Their product, \\(\alpha \beta\\), will be created by the stacking of
\\(\alpha\\) vertically on top of \\(\beta\\), such that the base of \\(\alpha\\) aligns
with the top of \\(\beta\\). This will create a rectangular solid representing
\\(\alpha \beta\\) that can then be shrunk to keep the original dimensions of
\\(\alpha\\) and \\(\beta\\), as shown in the figure on the next page.

<div class="centered_image">
{{< paige/figure caption="Product of two 3-Braids" >}}
{{< paige/image alt="Landscape" breakpoints=true class="object-fit-cover rounded-4" fetchpriority="high" height="20rem" loading="eager" process="webp" src="./images/b6.svg" width="100%" >}}
{{< /paige/figure >}}
</div>

\\(\hspace{1cm}\\) It is important to note that \\(\alpha \beta \neq \beta \alpha\\), generally.

\\(\hspace{1cm}\\) We will now show that the action of the product is associative,
even though it is not always commutative. Because all we are doing is stacking
braids on top of each other and we are not changing the order of the stacking,
we are not changing the braid that is being created, meaning \\((\alpha \beta)
\gamma = \alpha (\beta \gamma)\\). This can be seen in Figure "Associativity of Braids"
below. However, as mentioned above changing the order in which you
stack/multiply your braids does not always create the same braid, so the action
of the product is not always commutative.

<div class="centered_image">
{{< paige/figure caption="Associativity of Braids" >}}
{{< paige/image alt="Landscape" breakpoints=true class="object-fit-cover rounded-4" fetchpriority="high" height="20rem" loading="eager" process="webp" src="./images/b7.svg" width="100%" >}}
{{< /paige/figure >}}
</div>

\\(\hspace{1cm}\\) The identity/unit element of the braid group is simply the
trivial braid, considering for any braid \\(\alpha\\), \\(\alpha e = \alpha = e
\alpha\\). This is shown in the figure below. We know this is true,
since multiplying \\(\alpha\\) by \\(e\\) does not affect \\(\alpha\\), but rather elongates
it, which can be mitigated, considering we can shrink the product of our two
braids back to the original size of \\(\alpha\\).

<div class="centered_image">
{{< paige/figure caption="The Trivial Braid is the Identity" >}}
{{< paige/image alt="Landscape" breakpoints=true class="object-fit-cover rounded-4" fetchpriority="high" height="20rem" loading="eager" process="webp" src="./images/b8.svg" width="100%" >}}
{{< /paige/figure >}}
</div>

\\(\hspace{1cm}\\) Now to find the inverse element of \\(\alpha\\), we need to consider
the mirror image \\(\alpha^{-1}\\) of \\(\alpha\\). Based on this, we know that \\(\alpha
\alpha^{-1} = e = \alpha^{-1} \alpha\\). This is shown in the figure below.

<div class="centered_image">
{{< paige/figure caption="α α⁻¹ = e" >}}
{{< paige/image alt="Landscape" breakpoints=true class="object-fit-cover rounded-4" fetchpriority="high" height="20rem" loading="eager" process="webp" src="./images/b9.svg" width="100%" >}}
{{< /paige/figure >}}
</div>

\\(\hspace{1cm}\\) We can tell the figure above is the trivial knot by taking the first
string and pulling it to the left, so that the first string ends up being a
straight line. The same logic can be applied to the third string and pulling it
all the way to the right so that the third string becomes a straight
line. Finally, by straightening out the second string we can achieve the trivial
knot. We have now discussed all the requirements of the braid group, and I will
now introduce the two simplest braid groups:

\\(\hspace{1cm}\\) The 1-braid group \\(B\_{1}\\), contains only one element,
specifically the trivial braid. Thus, \\(B\_{1}\\) is defined by \\(B\_{1} = e\\).

\\(\hspace{1cm}\\) The elements of 2-braid group \\(B\_{2}\\) can be described by the two
types of twists, the right twist and the left twist, as shown in the figure below. 

<div class="centered_image">
{{< paige/figure caption="The Two Types of Braids in \\(B\_{2}\\)" >}}
{{< paige/image alt="Landscape" breakpoints=true class="object-fit-cover rounded-4" fetchpriority="high" height="20rem" loading="eager" process="webp" src="./images/b10.svg" width="100%" >}}
{{< /paige/figure >}}
</div>

\\(\hspace{1cm}\\) With any combination of these two types of twists, we will
achieve any braid in \\(B\_{2}\\). Therefore, we can also say two 2-braids are
equivalent if they have been twisted in the same direction the same number of
times. Now that we've started looking at more complex braids, we're going to
want a way to describe these braids without drawing the entire diagram. Thus,
come in braid generators.


### Braid Generators {#braid-generators}

\\(\hspace{1cm}\\) To understand braid generators, let's now divide our braids into
rows, such that every row contains only one crossing. We'll start with braids in
\\(B\_{2}\\). This can be visualised in the figure below

<div class="centered_image">
{{< paige/figure caption="Twists with Rows" >}}
{{< paige/image alt="Landscape" breakpoints=true class="object-fit-cover rounded-4" fetchpriority="high" height="20rem" loading="eager" process="webp" src="./images/b11.svg" width="100%" >}}
{{< /paige/figure >}}
</div>

\\(\hspace{1cm}\\) We will define both of these braids, as having \\(m\\) twists.

\\(\hspace{1cm}\\) In our braid on the left, which consists of only left twists, we
will see the second strand crossing over the first strand in every row. We will
call each of these rows/crossings \\(\sigma\_{1}\\). In our right braid, which
consists of only right twists, we will see the first strand crossing over the
second strand in every row. We will call each of these rows/crossings
\\(\sigma\_{1} ^{-1}\\). Because each of these braids have \\(m\\) rows/ crossings, we
can represent the braid on the left as \\(\sigma\_{1}^{m}\\) and the braid on the
right as \\(\sigma\_{1}^{-m}\\). These sigmas are called braid generators, as these
two types of crossings are the only ones we need to define any braid. We've now
defined the difference between \\(\sigma\_{1}\\) and \\(\sigma\_{1}^{-1}\\), as the
difference in the crossings, but what's the difference between \\(\sigma\_{1}\\) and
\\(\sigma\_{2}\\). \\(\sigma\_{1}\\) deals with the first two strands of a braid, where as
\\(\sigma\_{2}\\) deals with the second strand and the third strand of a braid. Thus,
\\(\sigma\_{1}\\) and \\(\sigma\_{1}^{-1}\\) can define \\(B\_{2}\\), but once we reach
\\(B\_{3}\\), which has 3 strands, we're going to need \\(\sigma\_{1},\sigma\_{2}\\), and
their respective inverses. We can generalize \\(\sigma\_{i}\\) by saying that it
along with its inverse deal with the \\(i^{th}\\), and the \\(i^{th} +1\\) strings, as
shown in Figure "Braid Generators" below.

<div class="centered_image">
{{< paige/figure caption="Braid Generators" >}}
{{< paige/image alt="Landscape" breakpoints=true class="object-fit-cover rounded-4" fetchpriority="high" height="20rem" loading="eager" process="webp" src="./images/b12.svg" width="100%" >}}
{{< /paige/figure >}}
</div>

\\(\hspace{1cm}\\) Let's now look at an example of how braid generators are used to
describe braids. In the figure below, we will see a braid in \\(B\_{4}\\) that can
be described by braid generators as \\(\sigma\_{3}^{-1}
\sigma\_{1}\sigma\_{2}\sigma\_{3}\sigma\_{2}^{-1}\\).

<div class="centered_image">
{{< paige/figure caption="Using Braid Generators to Describe a Braid in \\(B\_{4}\\)" >}}
{{< paige/image alt="Landscape" breakpoints=true class="object-fit-cover rounded-4" fetchpriority="high" height="20rem" loading="eager" process="webp" src="./images/b13.svg" width="100%" >}}
{{< /paige/figure >}}
</div>

\\(\hspace{1cm}\\) Taking this row by row, we see that the first row deals with
third and fourth strand, therefore, we will use either \\(\sigma\_{3}\\) or
\\(\sigma\_{3}^{-1}\\) to describe. However, because the third strand is crossing
over the fourth strand, it will be \\(\sigma\_{3}^{-1}\\). The second row deals with
the first and second strand. Thus, we know we will use either \\(\sigma\_{1}\\) or
\\(\sigma\_{1}^{-1}\\). Since the second strand is crossing over the first strand, we
know we will use \\(\sigma\_{1}\\). This logic can be applied to the rest of the rows
and we can see how \\(\sigma\_{3}^{-1}
\sigma\_{1}\sigma\_{2}\sigma\_{3}\sigma\_{2}^{-1}\\) describes this braid.


### Braid Relations {#braid-relations}

\\(\hspace{1cm}\\) \\(B\_{n}\\) is defined by the following presentation: \\[B\_n = \left(
\sigma\_1, \sigma\_2, \dots, \sigma\_{n-1} \\; \biggm| \\; \begin{aligned}
\sigma\_i\sigma\_j &= \sigma\_j\sigma\_i &&\text{for } |i-j| \geq 2,
\\\ \sigma\_i\sigma\_{i+1}\sigma\_i &= \sigma\_{i+1}\sigma\_i\sigma\_{i+1} &&\text{for
} 1 \le i \le n-2 \end{aligned} \right).\\] As we can see, \\(B\_{n}\\) only needs two
types of relations to be defined. The first relation \\(\sigma\_{i}\sigma\_{j} =
\sigma\_{j}\sigma\_{i}\\) only applies to \\(B\_{n \geq 4 }\\). This is because the
smallest generators that satisfy the condition of this relation are \\(\sigma\_{1}\\)
and \\(\sigma\_{3}\\), and \\(B\_{n}\\) only has \\(n-1\\) generators, so \\(\sigma\_{3}\\) only
exists starting from \\(B\_{4}\\). The second relation
\\(\sigma\_{i}\sigma\_{i+1}\sigma\_{i} = \sigma\_{i+1}\sigma\_{i}\sigma\_{i+1}\\) only
applies to \\(B\_{n \geq 3}\\). This is again because the smallest generators that
satisfy the condition of this relation are \\(\sigma\_{1}\\) and \\(\sigma\_{2}\\), which
only exist starting from \\(B\_{3}\\)

\\(\hspace{1cm}\\) We will now show that the first type of relation is true by
looking at the figure below.

<div class="centered_image">
{{< paige/figure caption="First Braid Relation" >}}
{{< paige/image alt="Landscape" breakpoints=true class="object-fit-cover rounded-4" fetchpriority="high" height="20rem" loading="eager" process="webp" src="./images/b14.svg" width="100%" >}}
{{< /paige/figure >}}
</div>

\\(\hspace{1cm}\\) We can see that \\(\sigma\_{1}\sigma\_{3} = \sigma\_{3}\sigma\_{1}\\) in
the figure, since we can squeeze the first twist and second twist in
\\(\sigma\_{1}\sigma\_{3}\\) down and up, respectively. Likewise, to show
\\(\sigma\_{3}\sigma\_{1} = \sigma\_{1}\sigma\_{3}\\), we can squeeze the first twist
and second twist in \\(\sigma\_{3}\sigma\_{1}\\) up and down, respectively. Now we
will look at the second type of relation in the figure below.

<div class="centered_image">
{{< paige/figure caption="Second Braid Relation" >}}
{{< paige/image alt="Landscape" breakpoints=true class="object-fit-cover rounded-4" fetchpriority="high" height="20rem" loading="eager" process="webp" src="./images/b15.svg" width="100%" >}}
{{< /paige/figure >}}
</div>

\\(\hspace{1cm}\\) The best way to see that \\(\sigma\_{1}\sigma\_{2}\sigma\_{1} =
\sigma\_{2}\sigma\_{1}\sigma\_{2}\\) is to look at
\\(\sigma\_{1}\sigma\_{2}\sigma\_{1}\\). If we take the third strand, and pull it up
and to the left, and then take the second strand and pull it down and to the
right, we will achieve \\(\sigma\_{2}\sigma\_{1}\sigma\_{2}\\). Similarly, to show that
\\(\sigma\_{2}\sigma\_{1}\sigma\_{2} = \sigma\_{1}\sigma\_{2}\sigma\_{1}\\), we will look
at \\(\sigma\_{2}\sigma\_{1}\sigma\_{2}\\) and pull the third strand down and to the
right and the second strand up and to the left. These same motions can be
applied to show that the second example, \\(\sigma\_{2}\sigma\_{3}\sigma\_{2} =
\sigma\_{3}\sigma\_{2}\sigma\_{3}\\) is true, as well.


## Knots &amp; Braids {#knots-and-braids}


### Braid Closure {#braid-closure}

Let's imagine we have a regular diagram of a braid, by connecting the
endpoints of the braid, with parallel arcs, as shown in the figure below, we
create a closed braid. This closed braid will either be a knot or a link.

<div class="centered_image">
{{< paige/figure caption="Closed Braid" >}}
{{< paige/image alt="Landscape" breakpoints=true class="object-fit-cover rounded-4" fetchpriority="high" height="20rem" loading="eager" process="webp" src="./images/closed_braid.svg" width="100%" >}}
{{< /paige/figure >}}
</div>

\\(\hspace{1cm}\\) It is important to note that these arcs should connect the
endpoints of the braid, such that, an endpoint \\(A\_{i}\\) at the top of the braid
has an arc connecting to the endpoint \\(A'\_{i}\\) at the bottom of the
braid. Another way to think about this is by looking at Figure "Closed Braid".  We see
that the outermost arc connects endpoint \\(A\_{1}\\) to endpoint \\(A'\_{1}\\), similarly
the endpoint \\(A\_{2}\\) is connected to the endpoint \\(A'\_{2}\\), and the endpoint
\\(A\_{3}\\) is connected to the endpoint \\(A'\_{3}\\), by the middle and innermost arcs
respectively.

\\(\hspace{1cm}\\) The orientation of the closed braid is usually defined by
assigning each string an orientation that starts from \\(A\_{i}\\) and then moving
downwards along the corresponding string. Thus, we can create oriented knots or
link from braids.


### Alexander's Theorem {#alexander-s-theorem}

\\(\hspace{1cm}\\) Alexander's Theorem states that every knot or link in \\(S^{3}\\) can
be represented as a closed braid.

<div class="centered_image">
{{< paige/figure caption="The Trivial 1-Braid" >}}
{{< paige/image alt="Landscape" breakpoints=true class="object-fit-cover rounded-4" fetchpriority="high" height="20rem" loading="eager" process="webp" src="./images/trivial_1_braid.svg" width="100%" >}}
{{< /paige/figure >}}
</div>

\\(\hspace{1cm}\\) One of the simplest examples of showing a knot or link can be
represented by a closed braid is by taking the trivial braid and closing it. If
the trivial braid has only one string as in Figure "The Trivial 1-Braid", by closing it we
create the unknot. If the trivial braid has n-strings as in Figure "Trivial Braid" above, by
closing it, we create the n-component unlink.

\\(\hspace{1cm}\\) The proof for Alexander's Theorem is algorithmic and very long
and tedious, so I won't explain it here, but I highly suggest reading Birman's
proof [[5]](#references), if that's what you're looking for.


### Markov's Theorem {#markov-s-theorem}

\\(\hspace{1cm}\\) Markov's Theorem states that if B and C are closed braids
representing the same isotopy class of oriented links, then it is possible to
transform B into C by a sequence of braid isotopies and Markov moves (a Markov
sequence).

<div class="centered_image">
{{< paige/figure caption="Markov Moves" >}}
{{< paige/image alt="Landscape" breakpoints=true class="object-fit-cover rounded-4" fetchpriority="high" height="20rem" loading="eager" process="webp" src="./images/b16.svg" width="100%" >}}
{{< /paige/figure >}}
</div>

\\(\hspace{1cm}\\) There are two markov moves, \\(M\_{1}\\) and \\(M\_{2}\\). \\(M\_{1}\\) is the
operation that transforms an element, \\(\beta\\), of the braid group \\(B\_{n}\\) into
the n-braid \\(\gamma \beta \gamma ^{-1}\\), where \\(\gamma\\) is an element of
\\(B\_{n}\\). This can be shown in part a of Figure "Markov Moves" above. As we can see \\(\beta =
\sigma\_{2} \sigma\_{1}^{-1} \sigma\_{2}\\) becomes \\(\sigma\_{2} \sigma\_{1}^{-1}
\sigma\_{2}\sigma\_{1}^{-1}\sigma\_{2} \sigma\_{2}^{-1}\sigma\_{1}\\), which is equal
to \\(\gamma \beta \gamma ^{-1}\\), where \\(\gamma = \sigma\_{2} \sigma\_{1}^{-1}\\),
after \\(M\_{1}\\) is applied.

\\(\hspace{1cm}\\) \\(M\_{2}\\) is the operation that transforms a n-braid, \\(\beta\\), into
either a \\(\beta \sigma\_{n}\\) or a \\(\beta \sigma\_{n}^{-1}\\), (n+1) braid, where
\\(\sigma\_{n}\\) is a generator of \\(B\_{n+1}\\). This can be shown in part b of Figure "Markov Moves". As we can see \\(\beta =
\sigma\_{2}\sigma\_{1}^{-1}\sigma\_{2}\sigma\_{1}^{-1}\\), which is an element of
\\(B\_{3}\\) turns into \\(\beta\sigma\_{n}\\) or \\(\beta\sigma\_{n}^{-1}\\), which is an
element of \\(B\_{4}\\) after M2.

\\(\hspace{1cm}\\) Thus, Markov's Theorem allows us to determine when two braids
represent the same knot or link. The proof of Markov's Theorem is even longer
than the proof for Alexander's Theorem, so again I will not be explaining it
here. However, a great proof in terms of seifert circles and reidemeister moves
can be found in [[6]](#references).


## Conclusion {#conclusion}

\\(\hspace{1cm}\\) In this paper, we introduced braids, their properties, and the
braid group. We also discuss how closed braids can represent any knot or link,
and that there exist moves that allow us to determine when two braids represent
the same knot or link. Because the braid group exists, we can study knots
algebraically instead of just topologically, which gives us more to work
with. There are also other braid invariants that we have not discussed, but that
can also be applied to knots, which give us even more resources to study knots,
as well.


## References {#references}

1.  Jones , V. F. R. (2005). The Jones Polynomial. University of California at
    Berkely Department of Mathematics.<https://math.berkeley.edu/~vfr/jones.pdf>.
2.  Jones , V. F. R. (2014). The Jones Polynomial for Dummies. University of
    California at Berkely Department of
    Mathematics.<https://math.berkeley.edu/~vfr/jonesakl.pdf>.
3.  Murasugi, K., &amp;amp; Murasugi, K. (2008). The Jones Revolution. In Knot
    theory and its applications (pp. 217–247). essay,
    Birkhäuser. <https://www.maths.ed.ac.uk/~v1ranick/papers/murasug3.pdf>.
4.  Glasscock, D. (2012, June). What is a braid group? - Ohio State
    University. Retrieved April 25, 2023, from
    <https://math.osu.edu/sites/math.osu.edu/files/BraidGroup.pdf>
5.  Birman, J. S., &amp;amp; Brendle, T. E. (2005, February 26). Braids: A
    survey. arXiv.org. Retrieved April 28, 2023, from
    <https://arxiv.org/abs/math/0409205>
6.  Traczyk, P. (1998). A new proof of Markov's braid theorem. Banach Center
    Publications, 42(1),
    409–419. <https://doi.org/http://matwbn.icm.edu.pl/ksiazki/bcp/bcp42/bcp42127.pdf>
7.  Kamada, S. (2002). Braid and knot theory in dimension four. Mathematical
    Surveys and
    Monographs, 95. <https://doi.org/https://www.ams.org/books/surv/095/surv095-endmatter.pdf>
8.  Kim, S., &amp;amp; Manturov, V. O. (2022, June 2). Lecture 6. Alexander's
    theorem and Markov's theorem - tsinghua university. Retrieved April 28,
    2023, from
    <https://ymsc.tsinghua.edu.cn/__local/B/9E/5A/3D8685AA0880367961727C3556C_7E5D1E08_77B71.pdf>

{{< paige/scrolltotop >}}
