# Chapter 1 Notes


### Definition 
A _list_ of length $n$ where $n \in \mathbb{Z}^+ \cup\{0 \}$ is an **ordered** collection of $n$ elements. $(x_1,x_2,...,x_n)$. Two lists are said to be equal if and only if they are of the same length and they have the same elements in the same order.

### Definition 

$F^n$ is the set of all lists of length $n$ of elements of $F$.
$$F^n=\{(x_1,x_2,...,x_n) \mid x_i \in F \text{ where } 1\leq i\leq n\}$$

### Definition 
_addition in_ $F^n$

**Addition** in $F^n$ is defined by adding the i'th terms. Example 

$$(a_1,a_2,...,a_i)+(b_1,b_2,...,b_i)=(a_1+b_1,a_2+b_2,...,a_i+b_i)$$

## Theorem
_Commutativity of addition in_ $F^n$

If $a,b \in F^n$ then $a+b=b+a$

**Proof**

$a+b=(a_1,...,a_n)+(b_1,...,b_n) =(a_1+b_1,...,a_n +b_ n)=(b_1+a_1,...,b_ n+a_n)= b+a$

$\square$

_We are able to say_ $(a_1+b_1,...,a_n +b_ n)=(b_1+a_1,...,b_ n+a_n)$ because $F$ is a field. 

### Definition 

$0$ is the list of length $n$ where $0=(0,...,0)$

### Definition
_The additive inverse in_ $F^n$

If $a\in F^n$ then $-a$ is said to be the **additive inverse**.

### Definition
_Scalar Multiplication_

The **product** of a number $a$ and a vector $x \in F^n$ is the number multiplied by each coordinate of the vector.

$a\in F,x\in F^n \;\;a\cdot x=(a\cdot x_1,a\cdot x_2,...,a\cdot x_n)$


## Definition 
**addition** on a set $V$ is a function from each pair of elements $a,b \in V$ another element $a+b \in V$.

**scalar multiplication** on a set $V$ is a function that assigns an element $av \in V$ to each $a \in F$ and each $v \in V$

## Definition of Vector Space

A **vector space** is a set $V$ along with an addition on $V$ and a scalar multiplication on $V$ such that the follow properties hold:

**commutativity**

* $a+b=b+a \;\forall a,b \in V$

**associativity**

* $(u+v)+w= u+(v+w)\; \; \forall u,v,w \in V$
* $(ab)v=a(bv) \; \; \forall v \in V, \forall a,b \in F$
 
**additive identity**

* $\exist 0,\forall v\in V$ such that $0+v=v$
  
**additive inverse**

* $\forall v,\exist u\in V$ such that $v+u=v$

**multiplicative identity**

* $1v=v ,\forall v \in V$

**distributive properties**
* $a(u+v)=au+av, \forall a\in F,\forall u,v\in V$
* $(a+b)v=av+bv, \forall a,b\in F,\forall v\in V$

