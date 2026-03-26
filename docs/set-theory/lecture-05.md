## Lecture 5

### Table of contents

- [Orderings](#orderings)
- [Blackboard images](#blackboard-images)

### Orderings

#### Definitions

A relation $R$ is an ordering on a class $A$ iff it is reflexive, weakly anti-symmetric and transitive on $A$.

$x,y \in A$ are comparable (by $R$) iff $(x,y) \in R$ or $(y,x) \in R$.

Notation: We write $x \leq_{R} y$ to say $(x,y) \in R$. Aka "$x$ is smaller than or equal to $y$ with respect to $R$".

An ordering on $R$ is linear iff $R$ is trichotomic.

$R'$ is a strict ordering iff it is of the form $R - ID$ where $R$ is an ordering.

Remark: $R'$ is anti-reflexive, anti-symmetric and transitive.

$x <_{R} y$ denotes $(x,y) \in R'$ aka "x is smaller than y with respect to R"


Exericise: Consider $E$(the membership relation) and $ID$(the identity relation). Determine if they are orderings or strict orderings.

#### E
It is not reflexive so not an ordering.

It is not transitive so not a strict ordering

#### Id

It is an ordering.(Check for the properties)
It is not a strict ordering as it is not anti-reflexive.

#### Examples: which orderings do we already know(Lecturer asks the students)

- $(\mathbb{N}, \leq)$
- $(\text{words},\text{lexigraphic ordering})$
- $X^2, \text{lexigraphic ordering}$ (If $X$ is ordering)
- $(\mathbb{N}, |)$(divisibility)
- $(X, \subseteq)$
- $(V, \in^*)$ (Transitive closure of $\in$)
- $(\mathbb{Z}, \leq)$
- $(\mathbb{R}, \leq)$
- $(\text{Gaussian Integers}, \text{absolute value or lexigraphic ordering})$ (Author's note: verify?)
- $(\mathbb{C}, \text{strictly order by absolute value or lexigraphic ordering})$ (Author's note: verify?)

### Bounds

Let $R$ be an ordering on a class $A$. Let $X \subseteq A$. We say $a \in A$ is (with respect to  $R$ and $X$) 

- A majorant(upper bound) of class $X$ iff $(\forall x \in X)(x \leq_{R} a)$ aka "a is larger than or equal to all elements of X"
- A maximal element of $X$ iff $a \in X \wedge (\forall x \in X)(\neg (a <_{R} x))$ aka "no element of $X$ is larger than $a \in X$"
- A maximum element(largest element) iff $a \in X$ and $a$ is a majorant of $X$.
- A supremum of $X$ iff $a$ is the smallest element of the class of all majorants of $X$.

We can similarly define minorant, minimal, minimum(smallest) and infinmum.

#### Example

Author's note: The lecturer then illustrates these definitions on an example. It is a visual proof so I decided not to add it.

#### Properties

Observation(s): 
- If an element is maximum, it is maximal.
- If $R$ is linear, then there is at most 1 maximal  element and it is also the maximum
- Maximum and supremum are always unique(if they exist).

Notation: We may write $a = max_{R}(X)$ and $a = sup_{R}(X)$ to denote them.

#### More definitions

We say that $X$ is bounded from above iff there exists a majorant of $X$ in $A$.(Similarly for bounded from below)

$X$ is a lower set(respectively class) in $A$ iff $(\forall x \in X)(\forall y \in A)(y \leq_{R} x \rightarrow y \in X)$

If $x \in A$, then $(\leftarrow, x ]$ is $\{y; y \in A \wedge y \leq_{R} x\}$
This is called the principal ideal determined by $x$/

Observation: If $R$ is an ordering on a class $A$, then for arbitrary $x,y \in A$, we have $x \leq_{R} y \leftrightarrow (\leftarrow, x] \subseteq (\leftarrow, y]$

Remark: We can construct $\mathbb{R}$ from $\mathbb{Q}$ by so-called "Dedekind" cut

If $X \subseteq \mathbb{Q}$, $X$ is a lower set and if $sup(X)$ exists, then $sup(X) \in X$.

For instance, $\mathbb{Q} \cap (- \infty, 1)$ is not a dedekind cut but $\mathbb{Q} \cap (- \infty, 1]$ is a dedekind cut.
$\mathbb{Q} \cap (- \infty, \sqrt{2})$ is a dedekind cut and this can be written as $\{x; x \in \mathbb{Q}, x^2 \leq 2 \wedge x \leq 0\}$

Definition: An ordering $R$ on a class $A$ is a well-ordering iff every non-empty subset of A has a smallest element with respect to $R$.

Exercise: Write this definition using a formula!

Observation: Well-ordering is a hereditary condition, that is if $B \subset eq$, $R$ is a well-ordering on $B$.

Remark: Do well-ordering and linear-ordering imply one another?
No, there are linear orderings which are not well-ordered but every well-ordering is a linear-ordering.(Proof?)

For example,

$(\mathbb{N}, \leq), (\{0,1,....,n\}, \leq), (\mathbb{N} \times \mathbb{N}, \text{Lexigraphic ordering})$ are well-ordered.

But the following are linear orders that are not well-ordered.

$(\mathbb{Z}, \leq), (\mathbb{R}, \leq), (\mathbb{Q}, \leq)$

Exercise: Find some set on which $E$ is a strict well-ordering.

Where "strict well-ordering" is of the form $R - ID$ where $R$ is a well-ordering.

### Blackboard images

I was sleep-deprived so not all the writings were photographed~~

[Download Lecture 5 (PDF)](set_theory_lecture_05.pdf)

