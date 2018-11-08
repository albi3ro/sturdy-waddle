D  +++
title = "Sets"
weight = 15
+++

Sets and Maps
=============

A **Set** is one of the most basic structures we can construct in
mathematics.

A set is a collection of indistinguiable objects.

The simplest set is the null set $ \varnothing =${}, the set that
contains no objects.

Or we could have a set with one object, like {$ \emptyset$ }, or { 🐱 }.

We have two basic operations we can perform on sets, union and
intersection.

<div class="definition">
 $A\cup B$ is called the
<b>union</b> of $A$ and $B$.  $ c \in A \cup B $ if $ a \in  A $ <b>OR</b> $a \in B$.</div>

<div class="definition">
 $A \cap B$ is called
the <b>intersection</b> of $A$ and $B$. $ c \in A \cap B $ if $a \in B$ <b>AND</b> $a \in B$.</div>

Time for some examples:

Let $A = $ { 🐶,🐴,🐇,🐡 } and $B= $ { 🐴, 🥦}.

Then $A \cup B = ${🐶,🐴,🐇,🐡, 🥦 }. And $ A\cap B = $ {🐴 }.

You might notice I’m using weird shapes instead of numbers as members of
my sets. I don’t want you to get stuck into thinking that these
definitions and concepts only apply to abstract numbers and the sorts of
things you dealt with in high school. An investigator might very well
look for the *intersection* of those who where at Jimmy’s bar on Friday
night and The Pit on Saturday. LGBTQ stands for the *union* of Lesbians,
Gays, Bisexuals, Transgenders, and Queers.

Seems fairly straightforward. But everything after that we do will be
built on having a solid foundation in sets.


| Notation | Name | Example elements|
| ---- | --- | --- |
| $\mathbb{R}$ | Reals | 1,$\pi$, $\sqrt{2}$, $-\frac{546093}{5496}$ ,0.549502... |
| $\mathbb{Q}$ | Rationals | 98, $-{5}{6}$ ,0.3333... |
| $\mathbb{Z}$ | Integers  | -1, 0, 1, 2, 10949853 |
| $S^1$ | Surface of a circle | $e^{i \phi}$ |


Modern mathematics attempts to build up as much as possible just from
sets. Even our ideas of numbers

When we restrict our discussion of equivalence to just maps between
sets, we get two important definitions,

Given two sets $X$ and $Y$ with an algebraic structure on them $\circ$ ,
for example mulitplication, and a map between them
$\phi:X\rightarrow Y$, $\phi$ is called a **homomorphism** and $X$ and
$Y$ are said to be **homomorphic** to each other if $\phi$ preserves the
structure on $Y$. In other words, for $x_1,x_2 \in X$,
$\phi(x_1)\circ \phi(x_2) = \phi(x_1 \circ x_2) \in Y$.

Homomorphism just goes one way. If we have this property in both
directions, $X\rightarrow Y$ and $Y\rightarrow X$ we use the stricter
condition of **Isomorphism**,

Given two sets $X$ and $Y$ with an algebraic structure on them $\circ$
and a map between them $\phi:X\rightarrow Y$, $\phi$ is called a
**isomorphism** and $X$ and $Y$ are said to be **isomorphic** to each
other if $\phi$ is homomorphic, and there exists an inverse
$\phi^{-1}: Y \rightarrow X$ that is also homomorphic.
