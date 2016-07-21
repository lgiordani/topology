# Topology without tears
## Leonardo Giordani personal notebook

## 1.1 Topology

### 1.1.1 Definitions

Let $X$ be a non-empty set. A set $\tau$ of subsets of $X$ is said to be a **topology** on $X$ if

1. $X$ and the empty set, $\varnothing$, belong to $\tau$,
2. the union of any (finite or infinite) number of sets in $\tau$ belongs to $\tau$, and
3. the intersection of any two sets in $\tau$ belongs to $\tau$.

The pair $(X, \tau)$ is called a **topological space**.

### 1.1.6 Definitions

Let $X$ be any non-empty set and let $\tau$ be the collection of all subsets of $X$. Then $\tau$ is called the **discrete topology** on the set $X$. The topological space $(X, \tau)$ is called a **discrete space**.

### 1.1.7 Definitions

Let $X$ be any non-empty set and $\tau = \{X, \varnothing\}$. Then $\tau$ is called the **indiscrete topology** and $(X, \tau)$ is said to be an **indiscrete space**.

### 1.1.8 Example (Proof)

If $X = \{a, b, c\}$ and $\tau$ is a topology on $X$ with $\{a\} \in \tau$, $\{b\} \in \tau$, and $\{c\} \in \tau$, prove that $\tau$ is the discrete topology.

**Given terms**

We are given the set $X = \{a, b, c\}$, a topology $\tau$ on it, and three sets $\{a\}, \{b\}, and \{c\}$ that belong to $\tau$.

The _topology_ term is defined in 1.1.1

The _discrete topology_ term is defined in 1.1.6

We shall prove that $\tau$ is the discrete topology.

**Proof**

To prove that $\tau$ is the discrete topology it is sufficient to show that all subsets of $X$ are in $\tau$, which is the definition of discrete topology.
Since the sets $\{a\}$, $\{b\}$, and $\{c\}$ belong to a topology we know from 1.1.1.2 that the union of those set belongs to the topology as well.
Thus we can create the sets $\{a, b\}$, $\{a, c\}$, $\{b, c\}$, and $\{a, b, c\}$ that are unions of the three sets and that belong to $\tau$.
The empty set belongs to $\tau$ because of 1.1.1.1.
The listed sets are exactly all the subsets of $X$. $\square$

### 1.1.9 Proposition

If $(X, \tau)$ is a topological space such that, for every $x \in X$, the singleton set $\{x\}$ is in $\tau$, then $\tau$ is the discrete topology.

**Given terms**

We are given a set $X$, a topology $\tau$ on it, and we know that every singleton set $\{x\}$ of $X$ belongs to $\tau$.

The _topology_ term is defined in 1.1.1

The _discrete topology_ term is defined in 1.1.6

We shall prove that $\tau$ is the discrete topology.

**Proof**

Suppose the topology $\tau$ contains every singleton of $X$, but $\tau$ is not the discrete topology, that is, $\tau$ does not contain all subsets of $X$.
In this case, we could find a set of $s \subset X$ which is not contained in $\tau$.
Being $s$ a subset of $X$ it is a union of some singletons of $X$, but since all singleton of $X$ are in $\tau$, according to 1.1.1.2 their union is in $\tau$ as well, which contradicts the hypothesis.
Thus, $\tau$ is the discrete topology. $\square$

## 1.2 Open Sets, Closed Sets, and Clopen Sets

### 1.2.1 Definitions

Let $(X, \tau)$ be any topological space. Then the members of $\tau$ are said to be **open sets**.

### 1.2.2 Proposition

If $(X, \tau)$ is any topological space, then

1. $X$ and $\varnothing$ are open sets,
2. the union of any (finite or infinite) number of open sets is an open set, and
3. the intersection of any finite number of open sets is an open set.

**Given terms**

We are given a topological space.

The _topological space_ is defined in 1.1.1

We shall prove the three points of the preposition.

**Proof**

1.2.2.1 and 1.2.2.2 are trivial consequences of definitions 1.1.1.1, 1.1.1.2, and 1.2.1.
1.2.2.3 is not trivial, since 1.1.1.3 states that "the intersection of any two sets in $\tau$ belongs to $\tau$".
If the intersection of any two sets in $\tau$ still belongs to $\tau$, however, this means that intersecting the result with another set in $\tau$ still produces a set in $\tau$. By induction, thus, we may state that the intersection of any finite number of elements in $\tau$ si still in $\tau$, that is, is an open set.

### 1.2.4 Definition

Let $(X, \tau)$ be a topological space. A subset $S$ of $X$ is said to be a **closed set** in $(X, \tau)$ if its complement in $X$, namely $X \setminus S$, is open in $(X, \tau)$.


