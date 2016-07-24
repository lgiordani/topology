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

**Proof**

Given terms:
* We are given the set $X = \{a, b, c\}$, a topology $\tau$ on it, and three sets $\{a\}, \{b\}, and \{c\}$ that belong to $\tau$.
* The _topology_ term is defined in 1.1.1
* The _discrete topology_ term is defined in 1.1.6
* We shall prove that $\tau$ is the discrete topology.

To prove that $\tau$ is the discrete topology it is sufficient to show that all subsets of $X$ are in $\tau$, which is the definition of discrete topology.
Since the sets $\{a\}$, $\{b\}$, and $\{c\}$ belong to a topology we know from 1.1.1.2 that the union of those set belongs to the topology as well.
Thus we can create the sets $\{a, b\}$, $\{a, c\}$, $\{b, c\}$, and $\{a, b, c\}$ that are unions of the three sets and that belong to $\tau$.
The empty set belongs to $\tau$ because of 1.1.1.1.
The listed sets are exactly all the subsets of $X$. $\square$

### 1.1.9 Proposition

If $(X, \tau)$ is a topological space such that, for every $x \in X$, the singleton set $\{x\}$ is in $\tau$, then $\tau$ is the discrete topology.

**Proof**

Given terms:
* We are given a set $X$, a topology $\tau$ on it, and we know that every singleton set $\{x\}$ of $X$ belongs to $\tau$.
* The _topology_ term is defined in 1.1.1
* The _discrete topology_ term is defined in 1.1.6
* We shall prove that $\tau$ is the discrete topology.

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

**Proof**

Given terms:
* We are given a topological space.
* The _topological space_ is defined in 1.1.1
* We shall prove the three points of the preposition.

1.2.2.1 and 1.2.2.2 are trivial consequences of definitions 1.1.1.1, 1.1.1.2, and 1.2.1.
1.2.2.3 is not trivial, since 1.1.1.3 states that "the intersection of any two sets in $\tau$ belongs to $\tau$".
If the intersection of any two sets in $\tau$ still belongs to $\tau$, however, this means that intersecting the result with another set in $\tau$ still produces a set in $\tau$. By induction, thus, we may state that the intersection of any finite number of elements in $\tau$ si still in $\tau$, that is, is an open set.

### 1.2.4 Definition

Let $(X, \tau)$ be a topological space. A subset $S$ of $X$ is said to be a **closed set** in $(X, \tau)$ if its complement in $X$, namely $X \setminus S$, is open in $(X, \tau)$.

### 1.2.5 Proposition

If $(X, \tau)$ is any topological space, then

1. $\varnothing$ and $X$ are closed sets,
2. the intersection of any (finite or infinite) number of closed sets is a closed set and
3. the union of any finite number of closed sets is a closed set

**Proof**

Given terms:
* The _topological space_ is defined in 1.1.1

1.2.5.1 is a trivial consequence of 1.2.2 and 1.2.4. $\varnothing$ and $X$ belong to the topology by definition. $\varnothing$ is the complement in $X$ of $X$, and $X$ is the complement in $X$ of $\varnothing$, so they are also closed sets.

To demonstrate (2) let us consider the intersection of an indexed family of closed sets $\cap_{i \in I}S_i$. The complement of such intersection by De Morgan's laws is the union of the complements, that is $X \setminus \cap_{i \in I}S_i = \cup_{i \in I}(X \setminus S_i)$, and since all $S_i$ sets are closed their complements are open, and by definition of topology their union still belongs to the topology. Since the complement of the intersection is an open set, by definition the intersection is a closed set.

To demonstrate (3) let us consider $S_1$, $S_2$, ..., $S_n$ closed sets. By definition the complement in $X$ of $S_j$ with $j = 1, ..., n$ is an open set. Thus by definition of topology the intersection of all the complements is still an open set, that is $(X \setminus S_1) \cap (X \setminus S_2) \cap ... \cap (X \setminus S_n) \in \tau$. Since the intersection of complements is the complement of the union we can write that $X \setminus (S_1 \cup S_2 \cup ... \cup S_n) \in \tau$. Since the complement of the union of $S_1$, $S_2$, ..., $S_n$ is an open set the union is a closed set.

$\square$

### 1.2.6 Definition
A subset $S$ of a topological space $(X, \tau)$ is said to be **clopen** if it is both open and closed in $(X, \tau)$.

## 1.3 The Finite-Closed Topology

### 1.3.1 Definition
Let $X$ be any non-empty set. A topology $\tau$ on $X$ is called the **finite-closed** topology or the **cofinite** topology if the closed subsets of $X$ are $X$ and all finite subsets of $X$; that is, the open sets are $\varnothing$ and all subsets of $X$ which have finite complements.

### 1.3.3 Example (Proof)

Let $\tau$ be the finite-closed topology on a set $X$. If $X$ has at least 3 distinct clopen subsets, prove that $X$ is a finite set.

**Proof**

Given terms:
* $X$ is a generic set
* $\tau$ is a finite-closed topology on $X$
* $X$ has at least 3 distinct clopen subsets, that is they and their complements belong to $\tau$.

Two clopen subsets are contained in every set by definition of topology, namely $X$ itself and $\varnothing$, so we know that $X$ contains another set $S$ which is open and closed. By definition of finite-closed topology, $\tau$ contains all subsets of $X$ which have finite complements. Since $S$ is both open and closed we may say that $S$ is a finite subset of $X$ (closed) which has finite complement $X \setminus S$ (open). Let us consider the union of the two finite sets $S \cup (X \setminus S) = X$. Being the union of two finite sets, $X$ is finite. \square

### 1.3.4 Definitions

Let $f$ be a function from a set $X$ into a set $Y$.

1. The function $f$ is said to be **one-to-one** or **injective** if $f(x_1) = f(x_2)$ implies $x_1 = x_2$, for $x_1, x_2 \in X$;
2. The function $f$ is said to be **onto** or **surjective** if for each $y \in Y$ there exists an $x \in X$ such that $f(x) = y$;
3. The function $f$ is said to be **bijective** if it is both **one-to-one** and **onto**.

### 1.3.5 Definitions
Let $f$ be a function from a set $X$ into a set $Y$.

The function $f$ is said to have an **inverse** if there exists a function $g$ of $Y$ into $X$ such that $g(f(x)) = x$, for all $x \in X$ and $f(g(y)) = y$, for all $y \in Y$. The function $g$ is called an inverse function of $f$.

### 1.3.6 Proposition
Let $f$ be a function from a set $X$ into a set $Y$.

1. The function $f$ has an inverse if and only if f is bijective.
2. Let $g_1$ and $g_2$ be functions from $Y$ into $X$. If $g_1$ and $g_2$ are both inverse functions of $f$, then $g_1 = g_2$; that is, $g_1(y) = g_2(y)$, for all $y \in Y$.
3. Let $g$ be a function from $Y$ into $X$. Then $g$ is an inverse function of $f$ if and only if $f$ is an inverse function of $g$.

**Proof**

Given terms:
* $f$ is a generic function from a set $X$ to a set $Y$

To prove 1.3.6.1 let us consider the definition of bijective and inverse. A function $f$ is said to be bijective is it is both one-to-one and onto. A function $f$ from $X$ to $Y$ has an inverse function $g$ from $Y$ to $X$ if $g(f(x)) = x$ for all $x \in X$ and $f(g(y)) = x$ for all $y \in Y$. Suppose $f$ is not one-to-one: we may find two elements $x_1, x_2 \in X$ so that $x_1 \neq x_2$ but $f(x_1) = f(x_2)$. If $f$ has an inverse function $g$ applying $g$ to both terms results in $g(f(x_1)) = g(f(x_2))$, which by definition of inverse leads to $x_1 = x_2$, which is a contradiction. Suppose now that $f$ is not onto: there exists a $y_0 \in Y$ such that $f(x) \neq y_0$ for all $x \in X$. If $f$ has an inverse $g$ then $f(g(y_0)) = y_0$ by definition of inverse. Setting $x_0 = g(y_0)$ we find a value $x_0 \in X$ which contradicts the hypothesis.

To prove 1.3.6.2 we can use 1.3.6.1 that states that $f$ is bijective, since there exist an inverse function. By definition of inverse function we know that $g_1(f(x)) = x$ and $g_2(f(x)) = x$ for all $x \in X$. So we may state that $g_1(f(x)) = g_2(f(x))$ for all $x \in X$. The onto property of $f$ also states that for each $y \in Y$ there exists an $x \in X$ such that $f(x) = y$, so the above equality becomes $g_1(y) = g_2(y)$ for all $y \in Y$.

Suppose $g$ is an inverse function of $f$, but $f$ is not an inverse function of $g$. From the second sentence we know that there exist a $y_0 \in Y$ such that $f(g(y_0)) \neq y_0$. Since $g$ is an inverse of $f$, this last one is bijective from 1.3.6.1, so we know that there exist an $x_0 \in X$ such that $f(x_0) = y_0$. Now applying $g$ to both terms we obtain $g(f(x_0)) = g(y_0)$ and applying $f$ that $f(g(f(x_0))) = f(g(y_0))$. From the hypothesis this can be recuded to $f(x_0) = f(g(y_0))$ and further to $y_0 = f(g(y_0))$ which is a contradiction. \square

### 1.3.7 Definition

Let $f$ be a function from a set $X$ into a set $Y$ . If $S$ is any subset of $Y$ , then the set $f^−1(S)$ is defined by

$f^−1(S) = {x : x \in X \and f(x) \in S}$

The subset $f^−1(S)$ of $X$ is said to be the inverse image of $S$.

### 1.3.9 Example (Proof)

Let $(Y, \tau)$ be a topological space and $X$ a non-empty set. Further, let $f$ be a function from $X$ into $Y$. Put $\tau_1 = {f^−1(S) : S \in \tau }$. Prove that $\tau_1$ is a topology on $X$.

Given terms:

* $(Y, \tau)$ is a topological space
* $X$ is a generic non-empty set
* $f$ is a function from $X$ into $Y$
* $\tau_1$ is the inverse image of the topology $\tau$ (according to the function $f$)
* We must prove that $\tau_1$ is a topology on $X$

The definition of topology is in 1.1.1.

Condition 1.1.1.1 states that $X$ and $\varnothing$ belong to $\tau_1$. We know that $f^-1(Y) = X$ by definition of $f$, so $X$ belongs to $\tau_1$. The function $f$ is defined from $X$ to $Y$, that means that the whole set $X$ is mapped to $Y$. It is not stated if the mapping is bijective, but we know that $X$ and $Y$ are fully covered by the function. Furthermore, $f^-1(\varnothing) = \varnothing$ because if the function is not applied to any value, no values are being returned. It is important here to understand that the function $f$, when applied on a topology, works on sets and not elements.

Condition 1.1.1.2 states that the union of any (finite or infinite) number of sets in $\tau_1$ belongs to $\tau_1$. Take ${A_j: j \in J}$ which is a collection of sets contained in $\tau_1$ indexed by a set $J$. The condition requires that $\cup_{j \in J}A_j \in \tau_1. Now, $A_j = f^-1(B_j)$ where $B_j \in \tau$, so we may write that $\cup_{j \in J}A_j = \cup_{j \in J}f^-1B(j) = f^-1(\cup_{j \in J}B_j). Since $B_j \in \tau$ and $\tau$ is a topology we know that $\cup_{j \in J}B_j \in \tau$, and, by definition of $\tau_1$, $f^-1(\cup_{j \in J}B_j) \in \tau_1$.

Condition 1.1.1.3 states that the intersection of any two sets in $\tau_1$ belongs to $\tau_1$. Consider $A_1$ and $A_2$ subsets of $\tau_1$. We may write that $A_1 = f^-1(B_1)$ and $A_2 = f^-1(B_2)$ with $B_1, B_2 \in \tau$. Thus $A_1 \cap A_2 = f^-1(B_1)$ \cap f^-1(B_2) = f^-1(B_1 \cap B_2)$, but since $B_1 \cap B_2 \in \tau$, by definition of $\tau_1$ we know that $f^-1(B_1 \cap B_2) \in \tau_1$. \square

### Exercise 1.3.1.1

Let $f$ be a function from a set $X$ into a set $Y$ . Then we state that

$f^-1(\cup_{j \in J}B_j) = \cup_{j \in J}f^-1(B_j)$

and

$f^-1(B_1 \cap B_2) = f^-1(B_1) \cap f^-1(B_2)$

for any subsets $B_j$ of $Y$ , and any index set $J$. Prove it

**Proof**

Given terms:

* $f$ is a function from $X$ to $Y$
* $B_j$ is a subset of $Y$
* $J$ is a generic index set

Being $f$ a generic function let us conrider a generic relation $R$ and prove that

$R[\cup_{i \in I}S_i] = \cup_{i \in I}R[B_i]$

Let us take $t \in $R[\cup_{i \in I}S_i]$. This means that $\exists s \in \cup_{i \in I}S_i : t \in R[s]$, which means that $\exists i \in I : \exists s in S_i : t \in R[s]$. But this means that $\exists i \in I : t \in R[S_i], which is the definition of set union, and then $t \in \cup_{i \in I}R[S_i]$.

Then let us prove that 

$R[S_1 \cap S_2] \subseteq R(S_1) \cap R(S_2)$

Consider that $S_1 \cap S_2 \subseteq S_1$, thus $R[S_1 \cap S_2] \subseteq R[S_1]$. Consider also that $S_1 \cap S_2 \subseteq S_2$, thus $R[S_1 \cap S_2] \subseteq R[S_2]$. This means that $R[S_1 \cap S_2] \subseteq R[S_1] \cap R[S_2]$. \square

