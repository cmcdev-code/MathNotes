<p style="text-align: center; font-size :24px">Group Class assignment 1</p>
<p style="text-align: center;">Collin McDevitt</p>
<p style="text-align: center; font-size:12px">21 August 2023</p>


(1) Prove $\mathbb{Z}  \subsetneq \mathbb{Q}$


Let $a\in \mathbb{Z} \implies a=\frac{a}{1}\implies a\in \mathbb{Q}$

Reasoning that $a=\frac{a}{1}$

Assume $a\neq \frac{a}{1}\implies a-\frac{a}{1}\neq 0$

By the multiplicative identity 

$1 \cdot a -a\neq 0\implies a-a\neq 0$



$a-a\neq0$ is a contradiction because $-a$ is the additive inverse of $a$ and $0$ is the additive identity


$\frac{3}{2} \in \mathbb{Q} \text{ but }\frac{3}{2} \notin \mathbb{Z}$

$\mathbb{Z} \subseteq \mathbb{Q} \;\land \frac{3}{2}\in \mathbb{Q} \text{ but }\frac{3}{2}\notin\mathbb{Z}\implies \mathbb{Z}\subseteq \mathbb{Q} \;\square$



(2) Prove $\mathbb{Q} \subsetneq \mathbb{R}$



Assume $\frac{a}{b}\in \mathbb{Q} \text{ but } \frac{a}{b}\notin \mathbb{R}$

$a,b\in \mathbb{R}$ and we know $\mathbb{R}$ is closed under multiplication so $a\cdot b^{-1}\in \mathbb{R}$ which is a contradiction because we assumed it was not in $\mathbb{R}$



$\sqrt{2} \in \mathbb{R} \text{ but }\sqrt{2} \notin \mathbb{Q}$

Assume $\sqrt{2}\in \mathbb{Q} \text{ with }\sqrt{2}=\frac{a}{b},\;a,b\in \mathbb{Z}^+, \gcd(a,b)=1$


$\sqrt{2}=\frac{a}{b}\implies b\cdot \sqrt{2}=a$

If we square both sides we end up with $a$ has to be even because even and odd numbers are closed under multiplication

$b^2\cdot2=a^2 \implies a=2\cdot k,\;k \in \mathbb{Z}^+$

$b^2\cdot 2=(2k)^2=4k^2$

$b^2\cdot2=4k^2\implies b^2=2k^2$

By the same reasoning above this implies $b$ is even

$b=2j,\; j\in \mathbb{Z}^+$

$\gcd(a,b)=1 \land gcd(a,b)\neq1$ is a contradiction which implies $\sqrt{2}\notin \mathbb{Q}$

$\mathbb{Q}\subseteq \mathbb{R} \; \land \sqrt{2}\in\mathbb{R}\text{ but }\sqrt{2} \notin \mathbb{Z} \implies \mathbb{Q}\subsetneq \mathbb{R} \;\square$
