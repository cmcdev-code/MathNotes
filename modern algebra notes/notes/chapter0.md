

- [What is a function?](#what-is-a-function)
    - [Various Sets](#various-sets)
    - [Axiom \[Well ordering principle\]](#axiom-well-ordering-principle)
    - [Theorem \[Principle of Mathematical Induction\]](#theorem-principle-of-mathematical-induction)
  - [Exercises](#exercises)
- [Number Theory](#number-theory)
    - [Definition \[Divides\]](#definition-divides)
    - [Theorem \[Division Algorithm\]](#theorem-division-algorithm)

# What is a function?

A function $f:A\mapsto B$ is a relation between two sets in this case the set  $A$ and $B$ where each element of $A$ is related to exactly one element of $B$.
In proper notation $\forall a\in A, \exists ! f(a)\in B$.

If we say that the function $f:A\mapsto B$ is _injective (one-to-one)_ then that means $f(a)=f(b)\implies a=b,\forall a,b\in A$

If we say that a function $f: A\mapsto B$ is _surjective (onto)_ then that means $\forall b\in B, \;\exists a \in A\text{ such that } f(a)=b$.

The _image (range)_ of $f$ is $f(A)$ in set notation $\{b\in B\mid \exists a \in A ,f(a)=b \}$ informally we can think of this as all the values of $B$ that are related to something in $A$

The _coDomain_ of the function $f:A\mapsto B$ is the set $B$ if the coDomain is equal to the image then we can say that it is surjective (onto).

The _Domain_ of the function $f: A\mapsto B$ is the set $A$

The _preimage_ of the function $f: A\mapsto B$ with $C\subseteq B$ is the set $\{x \in A\mid f(x)\in C\}$ 

### Various Sets

* The _natural numbers_ $\mathbb{N}=\{0,1,2,...\}$
* The _integers_ $\mathbb{Z}=\{...,-2,-1,0,1,2...\}= \mathbb{Z}\;\cup\{-x\mid x\in \mathbb{Z}\}$
* The _rational numbers_ $\mathbb{Q}=\{\frac{a}{b}\mid a,b\in \mathbb{Z},\; b\neq0\}$
* The _real numbers_ $\mathbb{R}=\{\text{set of real numbers}\}$
* The _complex numbers_ $\mathbb{C}=\{a+bi\mid a,b \in \mathbb{R}\}$

The sets $\mathbb{N},\mathbb{Z},\mathbb{Q}$ have a natural order defined by $a < b \iff b-a >0$.

### Axiom [Well ordering principle] 

Let $S \subset \mathbb{Z}$ be nonempty subset of the integers which is bounded below. Then $S$ contains a smallest element denoted by $\min(S)$.

### Theorem [Principle of Mathematical Induction]

Let $P(n)$ be a mathematical statement depending on an integer $n$ where $n\geq n_0$. Assume that:
* $P(n_0)$ is true
* $\forall n\geq n_0$ if $P(n)$ is true, then $P(n+1)$ is true.

Then $P(n)$ is true $\forall n\geq n_0$

**Proof** _of principle of mathematical induction_

Assume that $P(n_0)$ is true and $\forall n\geq n_0$ $P(n)$ is true and $P(n+1)$ is true but $\exists n_1\geq n_0$ where $P(n_1)$ is not true.
Then we know that the set $S$ that contains integers $i$ where $P(i)$ is not true is nonempty. Because its bounded bellow by $n_0$ and also nonempty then we can say $\exists \min(S)$ we will say that $a=\min(S)$ we can say that  $P(a-1)$ is true and by the assumption that would imply that $P(a)$ is true this is a contradiction. $\square$


## Exercises

1. Use the Well Ordering Principle to show that every nonempty set of negative integers has a greatest element.

**Proof**

Assume we have the non-empty set $S_n=\{-x\mid x\in \mathbb{Z}^+\}$ we can make the set $S_p=\{-x\mid x\in S_n \}$ then $S_p$ has a least element by the well ordering principle $a=\min(S_p)$ we know that $-a\in S_n$ and we know that this is the $-a=\max(S_n)$ suppose that it was not the max. Then that would mean that $\exist b\geq -a$ but that would mean that $-b \in S_p$ and $-b\leq a$ however we said $a$ was the $\min(S_p)$ which is a contradiction. $\square$ 

2. Conjecture a formula for $A^n$ where $A=\begin{pmatrix}
    1 & 1 \\ 
    0 & 1
\end{pmatrix}$

**Proof** 

$A^n=\begin{pmatrix}
    1&n\\
    0&1
\end{pmatrix}$ where $A=\begin{pmatrix}1&1 \\0 &1 \end{pmatrix}$

Base case is $A^1=\begin{pmatrix}1&1 \\0 &1 \end{pmatrix}$

Inductive hypothesis assume that $\exist n\geq 1$ where  $A^n=\begin{pmatrix}
    1&n\\
    0&1
\end{pmatrix}$

Then  $A^n=\begin{pmatrix}
    1&n\\
    0&1
\end{pmatrix} \implies A^n\cdot A=\begin{pmatrix}
    1&n\\
    0&1
\end{pmatrix}\cdot\begin{pmatrix}1&1 \\0 &1 \end{pmatrix}$ 

If we multiply the terms we end up with.

$A^{n+1}=\begin{pmatrix}1&n+1 \\0 &1 \end{pmatrix}\square$

3. Show that any amount of postage that is an integer number of cents greater than 11 cents can be formed using just 4-cent stamps and 5-cent stamps.

**Proof**

 Base cases $12¢$ can be formed by three 4-cent stamps. $13¢$ can be formed by two 4-cent stamps and a single 5-cent stamp.

 _Inductive hypothesis_
 
 Assume that $\exists n\geq 12$ where $i$ cents can be formed where $12\leq i \leq n$.

 We can form $n+1¢$ by forming $n-3$ and then adding another 5-cent stamp to 
 form $n+1¢\square$ 

4. Prove using mathematical induction that 
$$1^3+2^3+...+n^3=(\frac{n(n+1)}{2})^2, \forall n\geq 1$$

**Proof**

Base case $n=1$
$$1^3=1=(\frac{1\cdot2}{2})^2$$

_Induction hypothesis_

Assume that $\exists n\geq 1$ such that $\sum_{i\geq 1}^ni^3=(\frac{n(n+1)}{2})^2$


$$\sum_{i \geq 1}^{n+1}i^3=(n+1)^3+(\frac{n(n+1)}{2})^2$$
$$\frac{4*(n+1)^3+n^2(n+1)}{4}^2=\frac{(n+1)^2\cdot(4(n+1)+n^2)}{4}$$
$$\frac{(n+1)^2\cdot(4n+4+n^2)}{4}=\frac{(n+1)^2\cdot(n+2)^2}{4}$$

$$\frac{(n+1)^2\cdot(n+2)^2}{4}=\frac{(n+1)^2\cdot((n+1)+1)^2}{4}\square$$

# Number Theory
### Definition [Divides]
Let $a,b\in \mathbb{Z}$. We say $a$ divides $b$ written as $a\mid b$ if $\exists j \in \mathbb{Z}$, s.t. $b=a\cdot j$

### Theorem [Division Algorithm]

Let $a,b \in \mathbb{Z}, b>0$. Then $\exist!q,r\in \mathbb{Z}$ s.t. $a=bq+r \land 0\leq r \leq b-1$

**Proof**


_____________


