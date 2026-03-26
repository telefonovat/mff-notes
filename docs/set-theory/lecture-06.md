## Lecture 6

### Table of contents

- [Cardinalities](#cardinalities)
- [Cantor-Bernstein Theorem](#cantor-bernstein-theorem)
- [Blackboard images](#blackboard-images)

### Cardinalities

#### Comparing cardinalities

Def: Sets $x,y$ have the same cardinality denoted as $x \approx y$ iff there exists an injective mapping of $x$ onto $y$.(So a bijection)

"$x$ is equivalent to $y$"

A set $x$ has cardinality smaller than or equal to the cardinality of $y$ denoted as $x \preceq y$ iff there exists an injective mapping from $x$ to $y$.

"$x$ is subvalent to $y$"

$x$ has cardinality smaller than $y$ iff $x \preceq y \wedge \neg (x \approx y)$

Observation: $x \subseteq y \rightarrow x \preceq y$
Proof: By the identity relation.

Question: What about $x \subset y \rightarrow x \prec y$?
Answer: $x \subset y \rightarrow x \preceq y$ but not necessarily $x \prec y$

Question: Is $\preceq$ trichotomic?
Answer: In ZF, it is undecidable.

Lemma: If $x,y$ are sets,

1. $x \approx y$
2. $x \approx y \rightarrow y \approx x$
3. $(x \approx y \wedge y \approx z) \rightarrow x \approx z$
4. $x \approx x$
5. $(x \approx y \wedge y \approx z) \rightarrow x \approx z$

Remark: Is $\preceq$ weakly anti-symmetric? No, consider $\{\phi\}$ and $\{\{\phi\}\}$

Proof:

1. Use identity relation
2. Use the fact that if $f$ is bijective, $f^{-1}$ is also bijective.
3. If $f,g$ are bijective, $f \circ g$ is bijective.
4. Use identity again
5. If $f,g$ are injective, $f \circ g$ is injective.

Observation: $x \approx y \rightarrow (x \preceq y \wedge y \preceq x)$

Question: What about $x \approx y \leftarrow (x \preceq y \wedge y \preceq x)$?
Answer: It holds and this is called the Cantor-Bernstein Theorem.

### Cantor-Bernstein Theorem

#### Graph-theoretic proof

To be filled in. I will do it later.

#### Proof using the fixed-point lemma

Def: A mapping $H: \mathbb{P}(x) \rightarrow \mathbb{P}(x)$ is monotone with respect to inclusion iff for every $u,v \in x$, we have $u \subseteq v \rightarrow H(u) \subseteq H(v)$ 

Lemma: If $H: \mathbb{P}(x) \rightarrow \mathbb{P}(x)$ is monotone with respect to inclusion, then there exists $c \subset x$ such that $H(c)=c$. ("$c$ is a fixed point")

Exercise: For $h:[0,1] \rightarrow [0,1]$ that is non-decreasing(not necessarily continuous), $h$ has a fixed point.

Exercise: $A \subseteq \mathbb{P}(x)$, then $sup_{\subseteq}A = \cup A$. Similarly, $inf_{\subseteq} A = \cap A$. ("A complete lattice")

We will use the above exercise in the proof of the lemma.

Proof of the lemma: 

Let $A = \{u;u \subseteq x \wedge u \subseteq H(u)\}$
Let $c = \cup A(= sup A)$

Now $c \subseteq x$(Everything in $A$ is a subset of $x$)

Let $u \in A$. Then from $u \subset eq c$, we get $u \subseteq x$.

Now $u \subseteq H(u) \subseteq H(c)$ (Since $u \subseteq c$ and from the exercise above)

So, $H(c)$ is an upper bound of A. So $c \subseteq H(c)$ that is $c$ is a supremum of $A$.

By the monotonicity of $H$, we have $H(c) \subseteq H(H(c))$($u = c$, $v = H(c)$ in the definition)

So, $H(c) \in A$.

Then $H(c) \subseteq c$ because c is an upperbound of A.

Combined with $c \subseteq H(c)$, $c = H(c)$ so $c$ is a fixed-point.

--------
Now let us prove Cantor-Bernstein.

Proof:

Let $f:x \rightarrow y, g: y \rightarrow x$ be injective mappings.
We will use "induced" mappings 

$$
\overrightarrow{f}: \mathbb{P}(x) \rightarrow \mathbb{P}(y), u \rightarrow f[u]
$$

As an illustration, for $u=\{1,2,3\} \rightarrow \{f(1),f(2),f(3)\} = f[u]$

Similarly define $\overrightarrow{g}$

Observation: $\overrightarrow{f}$ and $overrightarrow{g}$ are monotone with respect to inclusion.

Now, we define $H:\mathbb{P}(x) \rightarrow \mathbb{P}(x)$ as follows.

For $u \subseteq x$, let $H(u) = X - g[y -f[u]]$.

Firstly, check if $H$ is monotone with respect to inclusion.

Let $u_1 \subseteq u_2 \subseteq x$

Since $\overrightarrow{f}$ is monotone, $f[u_1] \subseteq f[u_2]$.

So $y-f[u_1] \supseteq y - f[u_2]$

Then, $g[y - f[u_1]] \supseteq g[y - f[u_2]]$

$H(u_1) \subseteq H(u_2)$ ($-$ reverses the direction of inclusion)

By the lemma, $H$ has a fixed-point $c$ so $c =H(c) =X - g[y-f[c]]$

So $X - c = g[y - f[c]]$

We define $h: x \rightarrow y$ as follows.

$h(c) = f(a)$ if $a \in c$ and $g^{-1}(a)$ if $a \in X -c$

This is surjective.

Exercise: verify that this is injective.


#### Examples and applications of Cantor-Bernstein

We define $\omega = \mathbb{N}_0$ as the natural numbers including $0$.

$w \approx w \times w$

We define the map $f: \omega \rightarrow \omega \times \omega$ such that $f(u) = (0,u)$

Also $g: \omega \times \omega \rightarrow \omega$ such that $g((m,n))= 2^m . 3^n$

Both of these maps are injective.

A bijection is also possible: $h: \omega \times \omega \rightarrow \omega$ such that $h((m,n)) = 2^m(2n+1) -1$

Exercise: Verify that $g$ is injective and $h$ is a bijection

Exercise: Prove that $[0,1]$ and $[0,1]^2$ have the same cardinality. 

Remark: Don't try to define a bijection. Much easier to define 2 injective mappings for this problem.

Exercise Prove that $\mathbb{N} \approx \mathbb{Q}$

Exercise: Think about how to define finite sets with the tools we have. How do we write "x is a finite set"? Try exploring if and how we can use the following tools

- Orderings
- Mappings
- Assuming $\mathbb{N}$

In each possibility, what can we do?




### Blackboard Images

Incomplete. I keep forgetting to take pictures.


[Download Lecture 6 (PDF)](set_theory_lecture_06.pdf)
