# Natural Number
- Lax definition
  - $\mathbb{N}=\{0,1,2,3,4,\cdots\}$
- Peano axioms
  - $\exists<\mathbb{N},S,e>\ s.t.\ \mathbb{N}\ne\emptyset\wedge S:\natnums\mapsto\natnums$
  - $e\in\mathbb{N}$
  - $a\in\mathbb{N}\Rightarrow S(a)\in\mathbb{N} $
  - $S(a)=S(b)\Rightarrow a=b$
  - $a\in\mathbb{N}\Rightarrow S(a)\ne e$
  - $(A\subseteq\mathbb{N})\wedge(e\in A)\wedge (S:A\to A)\Rightarrow A=\mathbb{N}$

Not hard to conclude
$$
\begin{aligned}
\exist &\natnums \\ 
( \\
  &\quad\natnums\ne\emptyset \\ 
  \qquad\wedge &\quad \exists f:\natnums\mapsto\natnums(\forall x\forall y((x\in\natnums\wedge y\in\natnums\wedge x\ne y)\Rightarrow(f(x)\ne f(y)))\\
  \qquad\wedge &\quad\exists 0(0\in\natnums\wedge(\nexists x(x\in\natnums\wedge f(x)=0))) \\
  \qquad\wedge &\quad \forall S((S\subseteq\natnums\wedge 0\in S\wedge\forall x(x\in S\Rightarrow f(x)\in S))\Rightarrow S=N) \\
) \\
\end{aligned}
$$

The Principle of Mathematical induction
$$(\psi(0)\wedge\forall n\in\mathbb{N}(\psi(n)\Rightarrow\psi(n+1)))\Rightarrow\forall n\in\mathbb{N}\ \psi(n)$$
The Principle of Strong Mathematical induction
$$\begin{aligned}&(\forall m(m\ge m_0)\Rightarrow((\forall m'(m_0\le m'\le m)\Rightarrow P(m'))\Rightarrow P(m)))\\ &\Rightarrow(\forall m(m\ge m_0\Rightarrow P(m)))\wedge(m_0,m,m'\in\natnums)\end{aligned}$$
Minimumprinciple
$$X\ne\emptyset\Rightarrow\exists n(n\in X\wedge\forall m(m\in X\Rightarrow n\le m))$$
