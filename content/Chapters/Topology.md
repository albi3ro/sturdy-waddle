+++
title = "Topology"
weight = 15
+++

Topology is a minimal amount of structure put onto sets. Once we have
sets, we can start arranging the objects in them and assigning more
information to the objects in the sets.

<div class="definition"> A <b>Topological Space</b> is a set $X$ and a collection
of subsets of $X$, $T$, such that
<ol>
<li>The empty set $\varnothing \in T$.</li>
<li>$X \in T$. </li>
<li>  The intersection of a <i>finite</i> number of sets in $T$ is also in $T$.
    $$\cap_{T_i\in T}^{N < \infty} T_i \in T$$. </li>
<li>  The union of <i>up to an infinite number</i> of sets in $T$ is also in
    $T$. $$\cup_{T_i \in T} T_i \in T$$. </li>
</ol>
</div>

 A **Trivial Topology** is when, for a given set $X$,
the topology only contains $X$ and the null set $\varnothing$.

<img src="/img/top1.svg">

or a given set $X$, its **discrete topology** is the
collection of all subsets of $X$.

<img src="/img/top2.svg">

Here’s an example of a 3-element set that is neither
the trivial nor discrete topology.

<img src="/img/top3.svg">


We can also have topological spaces for continuous sets, like
$\mathbb{R}$ or $\mathcal{S}^1$.

<div class="definition">
For $\epsilon > 0$, an <b>open ball</b> at point $p_1$ of radius $\epsilon$
is all points $B_{\epsilon}(p_1)= \{p_i \large| |p_i - p_1|<\epsilon \}$.
</div>

<div class="definition">
The <b>Standard Topology</b> for a given set $X$ is the
set, the null set, all open balls, and all finite unions of open balls. </div>

The standard topology is quite useful for limits and Calculus, since for
any $\epsilon >0$, we can always find points $p_1, p_2$ such that
$|p_1 - p_2| <\epsilon$.

## Comparing Topologies


In the Section on Sets, we defined two terms for comparing sets with an
algebraic structure, *homomorphism* and *isomorphism*. After we have
attached a topology to the set, we have analogous concepts.

Two topologies $X$ and $Y$ are **homeomorphic** if there exists a
function $f: X \rightarrow Y$ and inverse function
$f^{-1}: Y \rightarrow X$ that are both continuous.

The difference between *homomorphic*, and *homoemoprhic* . *Homomorphic* and *Isomorphic* are general categorization terms
that apply to sets, research **Category Theory** for more information.
*Hom**E**omorphic* applies specifically to topolog**Y** and
geometr**Y**.  There exists another terms that also sounds quite similar and that is easily mixed up with these, <b>homotopy</b>.  Homotopy is also used to compare topologies to each other, but this single term will require an entire an entire section to itself.  

Properties of Topologies
------------------------

While to prove two topologies homeomorphic, we need to find a map $f$
between them and it’s inverse, we have more painless ways to prove that
two topologies are not homeomorphic. We have properties of topologies
that are held invariant under isomorphism. If we can show that two
different topologies have different properties, then we know that they
can’t be isomorphic to each other. If two topologies agree on every
known property, then they probably are isomorphic to each other, but
mathematicians love their counterexamples, so don’t count on it.

A topology is called **compact** if every open cover has a finite
subcover.

That was the formal definition, but what does it mean? Sometimes my desk
seems like it has an infinite amount of papers spread out over it. Let
us suppose that my desk literally does have an infinite number of papers
covering it. I could take either a finite number of papers or an
infinite number of papers to cover my desk, but either way, I could
always find a finite subset of those that still cover the desk.

As opposed to my desk, the real line with the standard topology is not
compact. Suppose I choose the infinite cover of the real line
$\mathbb{R}$,

<img src="/img/top4.svg">

I have covered the real line with an infinite number of sets, but if I
take even one away, $\mathbb{R}$ will no longer be covered. The cover
presented above does not have a *finite* subcover. Since *every* cover
has to have a finite subcover for a topology to be compact, we just to
show one counter-example to show that a topology is not compact. Hence,
Reals equipped with the standard topology is not compact. QED.

Quod Erat Demonstrandum. Not Quantum Electro-Dynamics. Much as I like me
some relativistic light-matter interactions.

Moral of the story: don’t play strip poker with the Real Numbers. If
they started covered up, no matter how much they lose, there would
always be more clothing to remove.

Also known as **$T_2$**, every two points in a **Hausdorff** space have
disjoint neighborhoods.

A topological space of dimension $n$ is said to be **Orientable** is it
can be covered by a nowhere vanishing $n$-form.

This $n$-form could potentially be the orientation of the space, though
others might exist.

### Euler Character and Gauss-Bonnett Formula

Coordinate Systems
------------------

Once we have a topology for a set, we can put even more information on
the object via a coordinate system. At least in some circumstances. A
topology gave us an idea of which objects are “neighbors" and “next to
each other". If two objects are usually in subsets together, then they
are adjacent. A coordinate system gives a precise way to quantify this.

So in what circumstances can we do this? When we are dealing with a
**manifold**.

If a condition holds **locally**, then for every point $p\in X$, $p$ is
in some open set such that the condition holds on that open set.

A **Manifold** is a topological space that locally looks like Euclidean
space, $\mathbb{R}^n$, for some $n$.

The Standard Topology, could be a manifold,
depending on the underlying set. For example, $X=\mathbb{R}$ equipped
with the standard topology is a manifold, but the standard topology on a continuous set like

<img src="/img/top5.svg">

is not a manifold because the point where the circles are joined no
longer looks like a line. Our previous example of the discrete topology is not a manifold, but the trivial topology on even a finite set is equivalent to a 0-dimensional manifold.  

<div class="definition">
A <b>Chart</b> of a topology is a map $\phi: U \rightarrow V$, where $U$ is
an open set in the topology, and $V$ is an open set in $\mathbb{R}^n$.
$\phi$ must be one-to-one and onto, thus defining a homeomorphism.
</div>

<div class="definition">
An <b>Atlas</b> is a collection of charts covering the entirity of a
topological space. If two charts overlap on a set $U \cap V$, where
$\phi:U\rightarrow \mathbb{R}^n$ and $\psi:V\rightarrow \mathbb{R}^n$,
then the transition function
$\phi \circ \psi^{-1}: \mathbb{R}^n \rightarrow \mathbb{R}^n$ must be
defined on $U\cap V$, be continuous, and be differentiable.
</div>

 While the mathematical terminology might seem strange and at odds
with our conception from the English terms, the mathematical abstraction
and everyday object have much in common. The atlas is the comprehensive
book of everything put together, all the charts. We need more than one
chart because I don’t want United States highways at the same time I’m
planning how to get around on the Tokyo subway. Also, because latitude
and longitude are ill-defined on the north pole.

<img src="/img/atlas2.png">
