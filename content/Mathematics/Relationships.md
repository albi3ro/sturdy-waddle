+++
title = "Relationships"
weight = 1
+++


## Equivalence Relations
---------------------

Mathematicians have some precise words to say whether something is
identical to, indistinguishable from, or just for all intents and
purposes equivalent to something else. So let’s go over those words.


<div class="definition">
An <b>Equivalence Relation</b> $ \sim $ is a property between two objects
that is
<ul>
<li> <b>Reflexive</b> $a \sim a$ </li>
<li> <b>Symmetric</b> $a \sim b \rightarrow b \sim a$ </li>
<li> <b>Transitive</b> If $a\sim b$ and $b \sim c$ then $a \sim c$ </li>
</ul>
</div>

Say my equivalence relation is “is the same color as". Then

-   ocean $ \sim $ sky

-   grass $ \sim $ trees

-   sunburn $ \sim $ lobster

Or I could use an equivalence relation that is “could be deformed into
without cutting, tearing, or gluing”. Then


|    |   |  |
| ---| ---| ---|
| <img src="/img/shawl.JPG" alt="drawing" style="width:200px; float: right;"/> | <font size="+5"> $\sim$ </font> | <img src="/img/yarn.JPG" alt="drawing" style="width:200px; float: left;"/> |



Let’s treat these as “ideal" objects, and forget about the fact the
shawl is created from multiple different yarns, and that yarn itself is
constructed from a vast number of individual fibers.

| | | | | |
| --- | --- | --- | --- | --- |
| <img src="/img/mug.JPG" alt="drawing" style="width:100px;"/> | <font size="+5"> $\sim$ </font> | <img src="/img/donut.png" alt="drawing" style="width:100px;"/> | <font size="+5"> $\nsim$ </font> | <img src="/img/not_a_donut.jpg" alt="drawing" style="width:100px;"/> |


## Equivalence Classes
-------------------

An equivalence relation can be used to define **equivalence classes**.

<div class="definition">
Given a set $S$ and a equivalence relation $\sim$ on elements in $S$,
given an element $a\in S$, the <b>equivalence class</b>
$[ a ] = \{ b \in S | b \sim a\}$. </div>

For $[a]$, $a$ is called the *character* of that specific equivalence
class, but we can use difference characters to represent the same
equivalence class. For example, if $a\sim b$, then $[a]$ and $[b]$ are
the same thing.

An equivalence classes groups a bunch of things together based on
similarity. For example, we could use the equivalence relation “is same
food group”. Then $[$apple$]$ would represent all fruits. I could equally
write $[$orange$]$ and mean the exact same thing. But $[$croissant$]$ would
represent a different equivalence class, one that makes loaves of bread,
tarts, scones, and muffins indistinguishable.

We do this all the time, even if we don’t know it has the formal
mathematical name of “equivalence class”. The term “whales” is just our
way of grouping into a pile all humpbacks, blue whales, and right
whales, given the equivalence relationship, “eats same way”. Well, maybe
the relationship has a few more qualifiers.

Given a set and an equivalence relation, we can create a new set whose
members are equivalence classes. For example, let’s say our initial set
is everything on Earth, and the equivalence relation is “is the same
color as”. We would end up with a set where one element was “blue
things”, another “red things”, another “green things”. For the purposes
of this explanation, let’s simplify everything by saying objects will be
either blue or green or some other nice pure color, not like those paint
swatches you see at a hardware store with 150 shades of white.

For a math example, let the set be Integers $\mathbb{Z}$ and the
equivalence relation be “same parity”. $1 \sim 3 \sim 5 \nsim 2$. Now we
have a new set with two elements, $[1]$ and $[2]$.

## Quotient Space
--------------

A **Quotient space** $S/\sim$ for a set $S$ and an equivalence relation
$\sim$ is the set formed by equivalences classes in $S$ under $\sim$.

Going back to the Integers $\mathbb{Z}$ and the equivalence relation
“same parity”, $\mathbb{Z}/ \sim  \approx \mathbb{Z}_2$. I use $\approx$
as the answer isn’t the group $\mathbb{Z}_2$, but just equivalent to
$\mathbb{Z}_2$. Instead, it’s a group composed of the elements $[1]$ and
$[2]$, where each element is an equivalence class. This distinction
might seem like a silly bit of finicky-ness here. When we are dealing
with a set of loops, later on, I want you to remember that each member
of the set is a geometric thing, or a collection of geometric things,
though we map those objects onto numbers to be able to quantify and say
things about them.

So far, these have been fun little real-world examples, but our
equivalence relations can also divide materials up into similar phases,
divide Hamiltonians up into groups with the same symmetries, or identify
all wavefunctions equivalent up to a phase.
