# Generating Function Notes
 

 ### Definition of generating function
  
Let $\{f_n\}_{n \geq 0}$ be a sequence of real numbers. Then the formal power series $F(x)= \sum_{n \geq 0}f_nx^n$ is
called the ordinary generating function of the sequence $\{f_n\}_{n \geq 0}$

### Products of Generating Functions 

#### **Lemma**
Let $\{a_n\}_{n \geq 0}$ and $\{b_n\}_{n \geq 0}$ be two sequences, and let $A(x)= \sum_{n\geq 0}a_nx^n$, and $B(x)= \sum_{n \geq 0}b_nx^n$ be their respective generating functions. Define $c_n = \sum_{i=0}^na_ib_{n-i}$, and let $C(x) = \sum_{n \geq 0}c_nx^n$. Then 
$$A(x)B(x)=C(x)$$ 
**Proof**

Assume that we multiply the two sequences term by term. Every term can be written in the form $a_ix^i\cdot b_jx^j$ the power of x will only be $n$ iff $n=i+j$ and because $i \geq 0, j \geq 0$ then if we group by powers of x we know that there is a total of $n+1$ terms in the parentheses. The sum of these terms is $c_n = \sum_{i=0}^na_ib_{n-i}$ if we sum over the whole series we end up with $C(x) = \sum_{n \geq 0}c_nx^n$ $\square$

### Theorem [The Product formula]

Let $a_n$ be the number of ways to build a certain structure on an $n\text{-element}$ set, and let $b_n$ be the number of ways to build another structure on an $n \text{-element}$ set. Let $c_n$ be the number of ways to separate $n$ into the intervals $S= \{1,2,...,i\}$ and $T= \{i+1,i+2,...,n\}$,(the intervals $S$ and $T$ are allowed to be empty), then build a certain structure of the first kind on $S$, and a structure of the second kind on $T$. Let $A(x),B(x),\text{and},C(x)$ be the respective generating functions of the sequences $\{a_n\},\{b_n\},\text{and} \{c_n\}$. Then 

$$A(x)B(x)=C(x)$$

**Proof**

There are $a_i$ ways to build a structure of the first kind on $S$, and $b_{n-i}$ on $T$. This is true for all $1\leq i\leq n$. Therefore $c_n=\sum_{i=0}^na_ib_{n-i}$ and by the previous lemma we know what $A(x)B(x)$ is equal to.$\square$

## Compositions of Generating Functions

### Definition

Let $F(x) = \sum_{n \geq 0}f_n x^n$ be a formal power series, and let $G$ be a formal power series 
with a constant term 0. Then we define $(F\circ G)(x)= \sum_{n \geq 0}f_n(G(x))^n= f_0 + f_1G(x)+f_2G(x)^2...$

### Theorem 
Let $a_n$ be the number of ways to build a certain structure on an n-element set, and let us assume that $a_0=0$. Let $h_n$ be the number of ways to split the set $[n]$ into an unspecified number of disjoint ($\text{The sets A and B are disjoint} \iff S \cap T= \emptyset$) nonempty intervals, then build a structure of the given kind on each of these intervals. Set $h_0=1$. Denote $A(x)= \sum_{n\geq 0}a_nx^n$, and $H(x)= \sum _{n\geq 0}h_nx^n$. Then 
$$H(x)=\frac{1}{1-A(x)}$$

**Proof**

From the product formula we know that $A(x)^k$ is the number of ways to split a n-element set into $k$ disjoint intervals. If we then sum over all $k$ we get $\sum_{k \geq 1}A^k$. We know that $h_0=1$ so if we add that back we end up with
$$H(x)=1+\sum_{k \geq 1}A(x)^k=\sum_{k \geq 0}A(x)^k=\frac{1}{1-A(x)} \; \;\square$$

### Theorem 
_The Compositional formula_

Let $a_n$ be the number of ways to build a certain structure on an n-element set, and assume $a_0=0$. Let $b_n$ be the number of ways to build a second structure on an n-element set, and let $b_0=1$. Let $g_n$ be the number of ways to split the set $[n]$ into an unspecific number of nonempty intervals, build a structure of the given kind on each of these interval, and then build a structure of the second kind on the set of the intervals. Set $g_0$. Denote by $A(x),B(x),\text{ and }G(x)$ the generating functions of the sequences $\{a_n\},\{b_n\},\text{ and } \{g_n\}$. Then 
$$G(x)=A(x)B(x)$$

**Proof**

If we divide the set $[n]$ into $k$ intervals then there is $b_k$ ways to build a structure of the second kind. Because we divided it into $k$ intervals we know that if we built a structure of the first kind that the generating function would be $A(x)^k$. It's contribution to $G(x)$ is $b_kA(x)^k$ if we then sum over all values of $k$ we end up with
$$G(x)=\sum_{k\geq 0}b_kA(x)^k \; \; \square$$


## Exponential Generating Functions  
### Definition 

Let $\{f_n\}_{n \geq 0}$ be a sequence of real numbers. Then the formal power series $F(x) = \sum_{n \geq 0}f_n \frac{x^n}{n!}$ is called the _the exponential generating function_ of the sequence $\{f_n\}_{n \geq 0}$.

The reason that it is called _exponential_ is because if you had $f_n =1$. Then you would just have $F(x) = \sum_{n\geq 0}\frac{x^n}{n!}=e^x$

### Products of Exponential Generating Functions  

**Lemma**

Let $\{a_i\} \text{ and } b_k$ bet two sequences, and let $A(x)= \sum_{i \geq 0}a_i\frac{x^i}{i!} \text{ and } B(x)=\sum_{k\geq 0}b_k\frac{x^k}{k!}$ be their exponential generating functions. Define $c_n =\sum_{i\geq 0}^n{n \choose i}a_ib_{n-i}$, and let $C(x)$ be the exponential generating function of the sequence $\{c_n\}$. Then 
$$A(x)B(x)=C(x)$$

**Proof**

Suppose that we multiple out $A(x) \text{ and } B(x)$ term by term. Then each term would be of the form 
$a_i\frac{x^i}{i!} \cdot b_j\frac{x^j}{j!}$. The product would only be of degree $n$ iff $n=i+j$. Next $a_i b_j \cdot\frac{x^{i+j}}{i!j!}= a_i b_j \cdot\frac{x^{i+j}}{i!j!}\cdot \frac{(i+j)!}{(i+j)!}=a_i b_j \cdot\frac{x^{i+j}}{(i+j)!}\cdot {i+j \choose i}$. So if we then sum over all the possible ways to get a power of $x^n$ we end up with $\sum_{i \geq 0}^na_ib_{n-j}\frac{x^{n}}{n!}{n \choose i }$ if we then factor out $x^n, \frac{1}{n!}$ and then sum over all $n$ we end up with 
$$C(x)=\sum_{n \geq 0} \big( \sum_{i \geq 0}^n{n \choose i} a_i b_{n-i} \big)\frac{x^n}{n!}\; \square$$

### Theorem
_Product Formula for Exponential Generating Functions_

Let  $a_n$ be the number of ways to build a certain structure on an n-element set, and let $b_n$ be the number of ways to build another structure on an n-element set. Let $c_n$ be the number of ways to partition $[n]$ into the sets $S$ and $T$, then to build a structure of the first kind on $S$ and a structure of the second kind on $T$. Let $A(x),B(x),$ and $C(x)$ be the respective exponential generating functions of the sequence $\{a_n\},\{b_n\},$ and \{c_n\}. Then 
$$A(x)B(x)=C(x)$$

**Proof**

If $S$ has $i$ elements then there are ${n \choose i}$ ways to choose the elements of $S$ and $a_i$ ways to build a structure on $S$ and $b_{n-i}$ ways to build a structure on $T$ and because ${n \choose i}= {n \choose n-i}$ if we sum all of the ways we end up with $c_n=\sum_{i \geq 0}^n{n \choose i}a_ib_{n-i}$ and by the previous proof we know the generating function for $c_n$ $\square$

### Compositions of Exponential Generating Functions

### Theorem
__The Exponential Formula__

Let $a_n$ be the number of ways to build a certain structure on an n-element set, and assume $a_0=0$. Let $h_n$ be the number of ways to partition the set $[n]$ into an unspecified number of nonempty subsets, then build a structure of the given kind on each of these subsets. Set $h_0=1$. Denote by $A(x)$ and $H(x)$ the exponential generating functions of these sequences. Then 
$$H(x)=e^{A(x)}$$

**Proof**

From the product formula for exponential generating functions we know that the generating function for the number of ways to partition the set $[n]$ into $k$ subsets and then build a structure using $a_n$ is given by $\frac{A(x)^k}{k!}$ summing over all values of $k$ we end up with $\sum_{k \geq 1}\frac{A(x)^k}{k!}$ if we then add back in $h_0=1$ we end up with 
$$H(x)=1+ \sum_{k\geq 0}\frac{A(x)^k}{k!}=\sum_{k \geq 0}\frac{A(x)^k}{k!}= e^{A(x)}$$

### Theorem 

_The Compositional formula for Exponential Generating Functions_

Let $a_n$ be the number of ways to build a certain structure on an n-element set, and assume $a_0=0$. Let $b_n$ be the number of ways to build a second structure on an n-element set, and let $b_0=1$. Let $g_n$ be the number of ways to partition the set $[n]$ into an unspecified number of nonempty subsets, then build a structure of the first given kind on each of these subsets, then build a structure of the second kind jon the set of the subsets. Denote $A(x),B(x),$ and $G(x)$ the generating functions of the sequences ${a_n},{b_n},$ and ${g_n}$.
    Then 
$$G(x)=(B \circ A)(x)$$

**Proof**

We know from the product formula for exponential generating function that the generating function to create $k$ disjoin subsets that form a partition and build a structure on them using $a_n$ is given by $\frac{A(x)^k}{k!}$  and we know that $b_k$ gives the way to build another structure on those sets. If then add back in $g_0=1$ we end up with
$$G(x)=1+\sum_{k\geq 1}b_kA(x)^k=\sum_{k\geq 0}b_kA(x)^k=(B \circ A)(x)\; \square$$