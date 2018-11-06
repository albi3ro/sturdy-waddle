+++
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

$ c \in A \cup B $ if $ a \in  A $ **OR** $a \in B$. $A\cup B$ is called the
**union** of $A$ and $B$.

\( c \in A \cap B \)

 if $a \in B$ **AND** $a \in B$. $A \cap B$ is called
the **intersection** of $A$ and $B$.

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

     Notation               Name                                    Example Elements
  -------------- -------------------------- -----------------------------------------------------------------
   $\mathbb{R}$        the Real line         1, $\pi$, $\sqrt{2}$, $569543/3874329$, and $.3234898957786...$
   $\mathbb{Z}$         the Integers                                $-1, 0, 1, 2,...$
   $\mathbb{Q}$        The Rationals                           $p/q : p,q \in \mathbb{Z}$
      $S^1$       The surface of a circle.                            $e^{i \phi} $
      $S^2$       The surface of a sphere.  

  : The names of some common special sets often
  encountered.[]{data-label="tab:sets"}

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
