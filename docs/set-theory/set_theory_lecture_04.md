## Lecture 4

### Table of contents

- [Relations](#relations)
- [Orderings](#orderings)
- [Blackboard images](#blackboard-images)

### Relations

#### Relations


A class $R$ is a binary relation if $R \subseteq V x V$.
Here we introduce some notation as a shortcut, namely, $xRy$ as a shortcut for $(x,y) \in R$.

We define an n-ary relation similarly if $R \subseteq V^n$.

Some examples:

Membership relation E aka $\{ (x,y); x \in y\}$

Identity Id aka $\{ (x,y); x= y\}$

We further define some extra concepts.

If X is a relation on an arbitrary class, then $Dom(X)$ is $\{ u; (\exists v)(u,v) \in X\}$
Also known as the domain of X.

Similarly the range or $Rng(X)$ is $\{v;(\exists u)(u,v) \in X \}$

If Y is a class, X''Y(X[Y])is $\{z ; (\exists y)(y \in Y) \wedge (y,z) \in X \}$.
Aka the image of class Y by class X

$X\arrowvert_Y$ is $(y,z) ; y \in Y \wedge (y,z) \in X$.
Aka restriction of class X to the class Y.

Remark: As usual we are interested in under what conditions these objects are sets.

#### Domain, Range, image and restriction are sets

Lemma: If $x$ is a set and $Y$ is a class, then $Dom(x), Rng(x), x''Y, x\arrowvert_Y$ are sets.
Proof:

Claim: $Dom(x) \subseteq \cup(\cup x)$
Proof:

If $u \in Dom(x)$, then $(\exists v)$ such that $(u,v) \in x$.

Now recall the definition of the order pair and observe that

$u \in \{u\} \in (u,v) = \{\{u\}, \{u,v\}\}$.
Moreover $(u,v) \in x$.
So, $\{u\} \in \cup x$ and $u \in \cup(\cup x)$.

Similarly, $Rng(x) \subseteq \cup(\cup x)$ because

$v \in \{u,v\} \in (u,v) \in x$

So $v \in \cup(\cup x)$ 

Also,  $x''Y \subseteq Rng(x)$ by the definition and $x\arrowvert_Y \subseteq x$.

Now onto more definitions.

If R,S are relations, we define $R^{-1} := \{(u,v) ; (v,u) \in R \}$.

$R \circ S$ is $\{ (u,v) ; (\exists v) (u,v) \in R \wedge (v,w) \in S  \}$.
Aka composition of R and S.

Exercise: Verify that for every relation R $|\circ| \circ R = R = R \circ | \circ|$(Composing with the identity)

Exercise: Prove that for every pair of sets $x,y$ we have $(x,y) \in E \circ E \leftrightarrow x \in \cup Y$

#### Functions/Mappings

Now, we define a relation $F$ as a mapping or function iff

$$
(\forall u)(\forall v)(\forall w)((u, v) \in F \wedge (u,w) \in F \rightarrow v = w)
$$

Remark: Notice that this is the first part of the axiom schema of replacement.

Remark 2: It is not necessary for F to assign to everything in the set, that is, it may be a partial function.

As a shorthand, we write $F(u) = v$(Or less commonly $uFv$).

We say that $F$ is a mapping  of a class $X$ to(into) a class $Y$ (denoted as $F:X \rightarrow Y$) if $Dom(F) = X$ and $Rng(F) \subseteq Y$.

We say that $F$ is a mapping of class X onto class Y if in addition, the range if exactly $Y$, that is, $Rng(F) = Y$.

We call $F$ injective iff $F^-1$ is a mapping so that

$$
(\forall u)(\forall v)(\forall w)((F(u) = w \wedge F(v) = w) \rightarrow u =v)
$$

Aka every element of $Rng(F)$ has exactly one preimage.

As a detour we extend the language of Set Theory with

$(\exists x \in A) \varphi$ is a shortcut for $(\exists x)(x \in A \wedge \varphi)$.

$(\forall x \in A) \varphi$ is a shortcut for $(\forall x)(x \in A \rightarrow \varphi)$.

Remark: There are no restrictions on $\varphi$. It can be any formula.

#### Image/Preimage of a class

We define the image/preimage of a class $X$ by a mapping $F$ as below.

$F[X]$ instead of $F''X$ is $\{y;(\exists x \in X)(y = F(x)) \}$

$F^{-1}[x]$ instead of $F^{-1}{''X}$ is $\{y; (\exists x \in X) (x = F(y))\}$

#### The class of all mappings

If $A$ is a class and $a$ is a set, then $a_A$ is the class $\{ F; f:a \rightarrow A \}$.
aka the class of all mappings of a to A.

Remark: It is good to consider whether this definition makes sense. Can it be that all such $f$ are proper classes?

Observation: Every mapping $f$ of $a$ to $A$ is a set.

Proof: 

$f \subseteq a \times A$ and $f \subseteq a \times Rng(f)$.

We now claim that $Rng(f)$ is a set.

By the replacement axiom. $Rng(f)$ is a set so $a \times Rng(f)$ is a set

##### Some examples

$\varphi_Y = \{ \phi \}$

For $x \neq \phi$, $x_\phi = \phi$

Now consider $B_A$ for proper class B.

Does $F:B \rightarrow A$ make sense? Can $F$ be a set.

Let's try by contradiction.
Suppose $F$ is a set, therefore the domain is a set.

But $Dom(F) =B$ and B must be a set. So this is a contradiction.

Lemma: 
1. For arbitrary sets $x, y$, the class $x_y$ is a set.
2. If $x \neq \phi$ and Y is a proper class, $x_y$ is a proper class.

Proof:
For part 1,

If $f: x \rightarrow y$, then $f \subseteq x \times y$ so $f \in \mathcal{P}(x \times y)$.

So, $x_y \subseteq \mathcal{P}(x \times y)$. So it is a set!(By separation)

For part 2,

For $y \in Y$ we define a constant mapping $k_y: x \rightarrow Y$ such that $(\forall u \in x)(k_y(u) = y)$.
So, $k_y = x \times \{y\}$.

For $y \neq y'$ we have $k_y \neq k_{y'}$ as $x \neq \phi$.

Let $k$ be $\{k_y ; y \in Y \}$.

$k \subseteq x_Y$.

Now, suppose, $x_Y$ is not a proper class and it is a set.

$k$ is also a set.
Then we define a mapping $F:k \rightarrow Y$ as $F(k_y) = y$.

As $k$ is a set and $F$ is a function, by replacement axiom, $Rng(F)$ is a set.

But $Rng(F) = Y$ by our definition of the mapping.

So $Y$ must also be a set and we come to a contradiction.

##### Alternative proof

As an alternative way, we can also use

$\cup \cup \cup x_Y = x \cup Y$ (if $x \neq \phi$ and $Y \neq \phi$

If $x \cup Y$ is a set, then $Y$ must also be a set!

Exercise: Fill in the details!

### Orderings
#### Preamble

We now describe a special type of relations called orderings(or  orders).

A relation $R \subseteq V \times V$ on a class $A$ can be

##### Reflexive

##### Anti-reflexive

##### Symmetric

##### Weakly anti-symmetric

$$
(\forall x \in A)(\forall y \in A)(xRy \wedge yRx \rightarrow x = y)
$$

##### Anti-symmetric

$$
(\forall x \in A)(\forall y \in A)(xRy \rightarrow \neg yRx)
$$

##### Transitive

##### Trichotomic

$$
(\forall x \in A)(\forall y \in A)(xRy \vee yRx \vee x = y)
$$

Observation: These properties are "hereditary", that is, if they hold for a class A, they hold for a subclass $B \subseteq A$.

Note: The instructor defined only the ones that students did not know. He assumed prior knowledge.

### Blackboard images

[Download Lecture 4 (PDF)](set_theory_lecture_04.pdf)
