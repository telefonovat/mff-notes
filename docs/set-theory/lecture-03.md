## Lecture 3

### Table of contents
I forgot to take pics so no images this lecture. :(

- [Axioms](#axioms)

### Axioms

#### Axiom of Foundation(Regularity)

$$
(\forall a)(a \neq \phi \rightarrow (\exists x)(x \in a \wedge x \cap a = \phi))
$$

"Every non-epty set has an element that is disjoint with it".

Remark: This allows us a global characterisation of the universe of 'sets'

Exercise: Prove that this axiom forbids the existence of finite cycles of the relation $\in$.
Formally, $y_1,y_2,...,y_n$ such that $y_1 \in y_2 \wedge y_2 \in y_3 \wedge ... \wedge y_n \in y_1$. When $n = 1$, $y \in y$.

We have some more axioms - namely infinity and choice but we leave them until later lectures

Exercise: Prove that a set of all sets does not exists.
### Classes

We now introduce the notion of classes.

Formally, if $\varphi(x)$ is a formula, $\{x;\varphi(x)\}$ denotes the "collection" of sets satisfying $\varphi(x)$. Other variables may be in $\varphi$ as parameters.

If $\varphi(x)$ is of the form $x \in a \wedge \psi(x)$, then the collection is defined and it is a set.(By the axiom of separation)

$\{ x; \varphi(x)\}$ is a class term and the collection it denotes is a class determined by the formula $\varphi(x)$.

Observation: If $y$ is a set, $x= \{x;x \in y \wedge x = x \}$ so every set is also a class.

We now define a special type of class. A proper class is a class that is not a set.

Formally, we extend the language as follows.

In formulae in the place of free variables, we will admit class terms and class variables. 
Class varibles are denoted by large letters.(E.g $X, Y$)

For atomic formula, we define the following

$$
x=y,x \in y, x= X, x \in X, X \in x, x = y, X \in Y
$$

And expressions obtained by substituting $\{x;\varphi(x)\}$ for X and $\{y;\varphi(y)\}$ for Y.

Remark: Proper classes cannot be elements

In addition, other formula of this extended language can be obtained using logical connectives and quantifiers.

#### Elimination of class terms

Let $x,y,z,X,Y$ be variables(set/class) and $\varphi(x), \psi(y)$ be formulae of the basic language where $X$ is $\{x;\varphi(x)\}$ and $Y$ is $\{y;\psi(y)\}$.

$z \in X$ stands for $z \in \{x;\varphi(x)\}$
aka "z is an element of the class of all sets satisfying $\varphi(x)$"
We replace this with $\varphi(z)$ or more precisely $\varphi(x/z)$

$z = X$ stands for $z = \{x; \varphi(x)\}$
aka "z is equal to the class of all sets satisfying $\varphi(x)$"

We replace this with
$(\forall u)(u \in z \leftrightarrow \varphi(u))$
Where $u$ is a new variable that is not free in $\varphi$

$X \in Y$ is $\{x;\varphi(x)\} \in \{y;\psi(y)\}$

We place it with
$$
(\exists u)(u = \{x;\varphi(x)\} \wedge u \in \{y;\psi(x)\})
$$

And then further by
$$
(\exists u)(\forall v)(v \in u \leftrightarrow \varphi(v)) \wedge \psi(u)
$$

$X \in y$ stands for $\{ x;\varphi(x)\} \in y$.
Replace this with
$(\exists u)((\forall v)(v \in u \leftrightarrow  \varphi(v)) \wedge u \in Y)$ (We skipped one step)

$X = Y$ stands for $\{x;\varphi(x)\}=\{y;\psi(y)\}$
Replace this by

$$
(\forall u)(\varphi(u) \leftrightarrow \psi(u))
$$

Meta-observation: Formulae of the extended language determine the same classes as the formula of the basic language.

E.g $\{x; x \notin \{z;\psi(z)\}\}$

#### Class operations

We now generalise operations on sets.

Def: $A \cap B$ is $\{x; x \in A \wedge x \in B \}$

Def: $A \cup B$ is $\{x;x \in A \vee x \in B\}$

Def: $A - B$ is $\{x;x \in A \wedge x \notin B \}$

If $A = \{x;\varphi(x)\}$, $B = \{y;\psi(y)\}$, then $A \cap B = \{z;\varphi(z) \wedge \psi(z)\}$ and similarly for other operations


#### Universal Class

$\{ x | x = x \}$ contains all sets and this is call the universal set, denoted as $V$.

#### More definitions

For class $A$, the (absolute) complement of A is $V - A$ denoted as $-A$.

We also define $A \subseteq B$ and $A \subset B$.
"A is a subclass/proper subclass of B".

Exercise: Define these

$\cup A$ is the union of the class A, that is $\{x;(\exists x)(a \in A \wedge x \in a)\}$

$\cap A$ is the intersection of A, that is $\{x;(\forall a)(a \in A \rightarrow x \in a)\}$

Remark: $\cap \phi = V$ as $(\forall x)(\forall a)(a \in \phi \rightarrow x \in a)$ is true.

The power class of A is the class $\{a;a \subseteq A\}$

Exercise: Is it true that $\mathcal{P}(V) = V$

Lemma and exercise: The universal set is not a set,i.e, a proper class.

Lemma: If $A$ is a class and $a$ is a set, $a \cap A$ is a set.
Proof:
This is directly from the axiom schema of separation.

$A := \{x;\varphi(x)\}$

$a \cap A = \{ x | x \in a \wedge x \in A \}$ where $x \in A$ is the formula in separation.

#### Cartesian product of classes

The cartesian product denoted as $A \times B$ is the class $\{(a,b) | a \in A \wedge b \in B \}$ which is a shorthand for

$$
\{x;(\exists a)(\exists b)(x = (a,b) \wedge a \in A \wedge b \in B)\}
$$

Lemma: If $u,y$ are sets, then $u \times y$ is a set.
Proof:

Claim: $u \times y \subseteq \mathcal{P}(\mathcal{P}(u \times y))$
Because

If $u \in w$ and $v \in y$, $\{u\},\{u,v\} \subseteq w \cup y$.

So, $\{u\},\{u,v\} \in \mathcal{P}(w \cup y)$

Then $\{\{u\},\{u,v\}\} \subseteq \mathcal{P}(w \cup y)$.

So, $\{\{u\}, \{u,v\}\} \in \mathcal{P}(\mathcal{P}(w \cup y))$

Def: If $X$ is a class, then $X^1$ is $X$. $X^{n+1}$ is $X^n \times X$.

Observation: $X^n$ is a class of all ordered n-tuples from $X$.

Observation: $V^{n+1} \subseteq V^n \subseteq ... \subseteq V^2 \subseteq V^1 = V$

Exercise: Show that in general $X \times X^2$ is not equal to $X^3$($X^2 \times X$)

Remark: For this exercise, try substituting smaller cases. E.g $X =\{x\}$ or $X = \{\phi\}$

