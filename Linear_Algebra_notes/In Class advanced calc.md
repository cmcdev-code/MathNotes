
Recall: A sequence is a function $f:\mathbb{N}\mapsto \mathbb{R}$.
This requires sequences are infinite. If we have to consider a finite sequence then we just call it a finite sequence. 

_Cardinality_ 

Our main **theorem**:

1. The rationals $\mathbb{Q}$ are countable 
2. The reals  $\mathbb{R}$ are uncountable 

_Definition_ 

Let $A,B$ be sets, $A,B\neq \emptyset$. A function $f:A \mapsto B$ is called _one to one_ also called _injection_ if $f(a_1)=f(a_{2}),\; a_1,a_{2}\in A\implies a_1=a_2$. The function $f$ is called _onto_ or _surjective_ if $b\in B$ there is an $a\in A$ s.t. $f(a)=b$. If a function $f$ has both these properties then it is a _bijection_, in which case we say that $A,B$ are in _one to one correspondence_. The notion is $A$~$B$.


_Prop._ If $A,B$ are finite sets, then $A$ ~ $B$ iff $\mid A\mid =\mid B\mid$.

*Proof*
($\implies$)
	We may write $A=\{a_{1},a_{2},...,a_{n}\}$ where $n=\mid A\mid$. Also, if $\mid B\mid =n$
 we can write $B=\{b_{1},b_{2},...,b_{n}\}$. We define the function $f:A\mapsto B$ by $f(a_{i})=b_{i}$ for $i=1,...,n$. 
To see that $f$ is a 1-1 function, assume that $f(a)=b$ for some $a\in A,\; b\in B$ .There is some $i\in [n]$ s.t. $a=a_i$, and some $j\in [n]$ s.t. $b=b_{j}$. By the definition of $f$ we have that $f(a_{i})=b_{i}$, and also that $f(a_{i})=b_{j}$ by our assumption. Putting these together we have $b_i=b_j$, and so $i=j$ and $f$ is 1-1.  To show that $f$ is an _onto_ function fix an arbitrary $b\in B$. Then $b=b_j$ for some $1\leq j \leq n$. In turn we have $f(a_{j})=b_j$ as $b$ was chosen arb we have that $f$ is onto. 


_Def:_ A set $A$ is countable if $A$~$\mathbb{N}$  

_Prop_. A subset of a countable set, is finite or countable.
