+++
title = "Simplices"
weight = 4
+++


Simplicial Complexes
--------------------

An $n$-Simplex is an set of $(n+1)$ linearly independent points. We can
think of them as $n$-dimensional generalizations of triangles.

For some low dimensional examples,

<img src="/img/top6.svg">

Both unoriented and oriented simplices exist. For our purposes, we will
be using oriented simplices. The orietnation is a positive or negative
sign associated with the set. Permuting the order of the points in the
set can change the orientation.
$$p_1 p_2 = - p_2 p_1 \qquad \qquad p_3 p_4 p_5 = - p_4 p_3 p_5 = p_5 p_3 p_4$$

<img src="/img/top7.svg">

While we can see direction in one and two dimensions, this concept is
trickier to conceptualize in higher dimensions. In higher dimensions,
instead of thinking pictorially, we need to just think in terms of even
or odd permutations of an ordered set.
$$p_1 p_2 p_3 p_4 p_5 = - (p_2 p_1) p_3 p_4 p_5$$

By adding multiple simplices of the same dimension together, we can form
a **chain**. For example, this is a 2-chain,
$$p_1 p_2 p_2 + p_2 p_3 p_4$$

<img src="/img/top8.svg">

Each simplex gives us a collection of points. From that collection of
points, we can decide to just choose a subset of those and look at those
instead. This subset is a **face** of the simplex. For example, if we
look at the three dimensional simplex above, $p_6 p_7 p_8 p_9$, we could
choose the 2-face $p_6 p_7 p_8$. All the faces make up the boundaries
and edges of an object. We should be able to determine things about the
boundaries of an object that are independent of the particular way we
write in down but just dependent on the global, qualitative features of
the object. This will show up in how an object relates to its faces.

To study how an object relates to its faces, we need to introduce a
boundary operator $ \partial: \sigma_n \rightarrow \sigma_{n-1} $

$$ \partial \left(p_1 \dots p_n \right)
  = \sum_{i=1}^n (-1)^{i} p_1 \dots \hat{p_i} \dots p_n $$

where $\hat{p_i}$ is ommitted. For example, $$\begin{aligned}
  \partial(p_0) &= 0 \\
  \partial(p_1 p_2) & = p_2 - p_1 \\
  \partial(p_1 p_2 p_3) & = -p_2 p_3 + p_1 p_3 - p_1 p_2\end{aligned}$$
The boundary of a boundary is always zero,

$$
    \partial \partial \sigma =0.$$

We can verify this for the boundaries just calculated, $$\begin{aligned}
  \partial \partial (p_0 )& = \partial 0  &= 0 \\
  \partial \partial (p_1 p_2 )&= \partial (p_2 - p_1) &= 0 \\
  \partial \partial (p_1 p_2 p_3 )&= \partial (-p_2 p_3 + p_1 p_3 - p_1 p_2) &=
    p_2 - p_3 -p_1 + p_3  + p_1 -p_2 =0 ,\end{aligned}$$ or in general
for any dimension.

<div class="definition">
A <b>simplicial complex</b> is a set of of simplices $\kappa$ such that

<ol>
<li>For every simplex $\sigma \in \kappa$, every face of the simplex is
    also in $\kappa$</li>
<li>The intersection of two simplices is a face of both simplces,
    $\sigma_1 \cap \sigma_2 \in \partial \sigma_1 , \partial \sigma_2$</li>
</ol>
</div>

For example,

<img src="/img/top9.svg">

| dim 0 | dim 1 | dim 2 |
| --- | --- | --- |
| $p_0$ |  $p_0 p_1$  | $p_1 p_2 p_3 $|
|   $p_1$ |  $p_1 p_2$  | $p_2 p_3 p_4 $|
|   $p_2$  | $p_2 p_3$ | |
|   $p_3$  | $p_3 p_4$  ||
|   $p_4$ |  $p_4 p_2$  ||
|          | $p_1 p_3$  ||

is a simplicial complex. If we take the intersection of the simplices
$p_1 p_2 p_3$ and $p_2 p_3 p_4$, we get $p_2 p_3$, which is a face of
both simplices and in the simplicial complex.

But

<img src="/img/top10.svg">

is not a simplicial complex. What even is the intersection of $p_0 p_5$
and $p_1 p_2$? It’s certainly not a face of either simplex.

The simplicial complex

<img src="/img/top11.svg">

is equivalent to a torus. You can see that that edges are in fact the
same points. Since I couldn’t figure out how to perform this
manipulation with computer graphics, here’s the manipulation with good,
old fashioned arts and crafts,

<img src="/img/flat_torus.JPG" style="width: 20em">
<img src="/img/torus_1curl.JPG" style="width: 20em">
<img src="/img/torus_2curl.JPG" style="width: 20em">

I’ll often use this simplicial complex as it’s relatively simple, yet it
still has some interesting structure.

### The group of cycles and the group of boundaries

Let’s take a chain. For example,
$$\sigma_1=  p_7 p_6 + p_6 p_5 + p_5 p_7$$ in the torus. Two things
about this chain are relevantly interesting to us. First,
$$\partial \sigma_1 = 0.$$ The boundary of the chain is zero. You can
verify this for yourself. Second,
$$\exists \sigma_2 \qquad \text{such that} \qquad \partial \sigma_2 = \sigma_1.$$
In particular, $\sigma_2 = p_7 p_6 p_5$, but that fact is not as
important as the fact that *it exists*.

The first property defines **Cycles**.

<div class="definition">
A <b>Cycle</b> of dimension $d$ is a chain $\sigma$ in a
simplicial complex such that $\partial \sigma =0$.
</div>

We can add any two cycles of the same dimension together and get another
cycle just because the boundary operator is distributive. This means we
have a group, particularly the group $Z_d (T)$, where $T$ is the given
topology and $d$ is the dimension.

The second property defines **Boundaries**.

<div class="definition">
If $\partial \sigma_2 = \sigma_1$ for some $\sigma_2$, then $\sigma_1$
is a <b>boundary</b>.
</div>

If a chain is the derivative of something else, then it is a boundary.
More formally, it’s the image of the $\partial$ operator. Boundaries of
a certain dimension again will form a group $B_d (T)$, because of the
distributivity of the boundary operator.

Since we know from above that the second derivative
of every chain is zero, and every boundary is the derivative of a chain,
then the derivative of every boundary is zero. Every boundary is
then.... you guessed it... I hope, or I failed in explaining this ... a
cycle.

**BUT** not every cycle is a boundary.

To see this, let us go back to our trusty torus and look at the cycle
$$  p_1 p_7 + p_7 p_8 + p_8 p_1.$$

   Go ahead an verify that this is indeed
a cycle. That is a rather straight forward calculation. And then, waste
some period of time trying to find a combination of simplices that will
give that particular chain upon derivation. Then give up and say it’s
impossible. Physicist’s proof.

You can think of every boundary being able to be continuously deformed
to a point through the surface that it borders. But that chain above can’t be deformed away to a point because it
wraps around the torus. Only cutting and glueing the torus would allow
you to deform that cycle down into a point.

Till I write more, here's an example of performing the group operation within the group of cycles.

| | | |
|--- | --- | --- |
|<img src="/img/top12.svg">| <img src="/img/top13.svg"> | <img src="/img/top14.svg"> |
