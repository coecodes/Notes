# 数列极限
略
## 极限的证明
==递推形式的极限及其存在性证明==
- 已知 $S_1=\sqrt{2}$ , $S_{n+1}=\sqrt{2+S_n}$, 求证: 数列 $\{S_n\}$ 有极限, 并求这个极限
连分数
- 证明并计算$$2,2+\frac 12,2+\frac 1{2+\frac 12},\cdots$$
- 
==用极限存在准则证明极限存在==
==用极限定义证明极限存在==
==用数列及其子列的极限关系证明极限存在==

# 函数极限

- 描述性定义
	- 如果当自变量$x$无限接近实数$x_0$时，$f(x)$无限接近某个常数$A$，我们称这个常数$A$为当$x\to x_0$时，函数$f(x)$的极限，记作$$\lim_{x\to x_0}f(x)=A$$
- $\epsilon-N$语言
	- $\lim_{n\to\infty}a_n=A\Leftrightarrow \forall\varepsilon >0,\exists N,当n>N时,恒有$$$\mid a_n-A\mid<\varepsilon$$

- 收敛数列
- 函数极限
	- $$\lim_{x\to\infty}f(x)=A\Leftrightarrow\forall\varepsilon>0,\exists X>0,当\mid x\mid>X时,恒有\mid f(x)-A\mid<\varepsilon$$
	- $$\lim_{x\to+\infty}f(x)=A\Leftrightarrow\forall\varepsilon>0,\exists X>0,当x>X时,恒有\mid f(x)-A\mid<\varepsilon$$
	- $$\lim_{x\to-\infty}f(x)=A\Leftrightarrow\forall\varepsilon>0,\exists X>0,当x<-X时,恒有\mid f(x)-A\mid<\varepsilon$$
	- $$\lim_{x\to\infty}f(x)=A\Leftrightarrow\lim_{x\to+\infty}f(x)=\lim_{x\to-\infty}f(x)=A$$
	- $$\lim_{x\to x_0}f(x)=A\Leftrightarrow\forall\varepsilon>0,\exists\delta>0,当0<\mid x-x_0\mid<\delta时，恒有\mid f(x)-A\mid<\varepsilon$$
- 单侧极限
	- 左极限$$\lim_{x\to x_0^-}f(x)=A\Leftrightarrow\forall\varepsilon>0,\exists\delta>0,当x_0-\delta<x<x_0时，恒有\mid f(x)-A\mid< \varepsilon$$
	- 右极限$$\lim_{x\to x_0^+}f(x)=A\Leftrightarrow\forall\varepsilon>0,\exists\delta>0,当x_0<x<x_0+\delta时，恒有\mid f(x)-A\mid< \varepsilon$$
## 极限的性质
==唯一性==
- 如果数列$\{x_n\}$收敛, 那么它的极限唯一
<details>
<summary>证明</summary>

反证法: 
假设同时有 $\lim_{n\to\infty}x_n=a$及$\lim_{n\to\infty}x_n=b$, 且$a<b$, 取$\varepsilon =\frac{b-a}2$
故存在$N_1$, 有$$\mid x_n-a\mid<\frac{b-a}2$$存在$N_2$, 有$$\mid x_n-b\mid<\frac{b-a}2$$取$N=max\{N_1, N_2\}$有$$x_n<\frac {a+b}2$$和 $$x_n>\frac {a+b}2$$ 不能同时成立, 产生矛盾
</details>

- 有界性(数列)、局部有界性(函数)
	- 如果数列$\{x_n\}$收敛, 那么数列$\{x_n\}$一定有界


==保序性==
- 若$\lim_{n\to\infty}x_n=A,\lim_{n\to\infty}y_n=B$,则
	- 当$B>A$时,$\exists N,s.t.\ n>N,y_n>x_n$
	- 从某项以后有$y_n>x_n,则B\ge A$
- 保号性
	- 如果$\lim_{n\to\infty}x_n=a, 且a>0\ (或a<0)$, 那么存在正数$N$, 当$n>N$时, 都有$x_n>0\ (或x_n<0)$
	- 如果数列$\{x_n\}$从某项起有$x_n\ge 0\ (或x_n\le 0)$, 且$\lim_{n\to\infty}x_n=a$, 那么$a\ge 0\ (或a\le 0)$

==收敛数列与且子数列间的关系==
- 如果数列$\{x_n\}$收敛于$a$, 那么它的任意子数列也收敛, 且极限也是$a$
- 常运用于反证法证明极限不存在

==存在性==
- O'Stolz定理
	- 是处理数列不定式极限的有力工具，O'Stolz定理用于数列，它有函数形式的推广，这两个都可以认为是洛必达法则的离散版本。
	- $\frac{\infty}{\infty}$

==极限的运算性质==
- 域公理性
	- 若$\lim f(x)=A,\lim g(x)=B$,则
	- $$\lim[f(x)\pm g(x)]=\lim f(x)\pm\lim g(x)=A\pm B$$
	- $$\lim[f(x)g(x)]=\lim f(x)\cdot\lim g(x)=A\cdot B$$
	- $$\lim[\frac{f(x)}{g(x)}]=\frac{\lim f(x)}{\lim g(x)}=\frac{A}{B}\quad (B\ne 0)$$
- 正则公理性

<details>
<summary>经典极限</summary>

## 经典极限
- $$\lim_{x\to 0}\frac {sin\ x}{x}=1$$
	- $$\lim_{x\to\infty}\frac {sin\ x}{x}=0$$
	- $$\lim_{x\to 0}\frac {sin\ mx}{sin\ nx}=\frac{m}{n}$$
- $$\lim_{x\to 0}\frac {tan\ x}{x}=1$$
	- $$\lim_{x\to \frac{\pi}{2}\pm 0}\frac {tan\ x}{x}=\mp\infty$$
- $$\lim_{x\to\infty}(1+\frac{1}{x})^{x}=e$$
	- $$\lim_{x\to +0}(1+\frac{1}{x})^{x}=1$$
	- $$\lim_{x\to -1^{-0}}(1+\frac{1}{x})^{x}=+\infty$$
	- $$\lim_{x\to 0}(1+kx)^{\frac{1}{x}}=e^k$$
- $$⁤\lim_{x\to 0}\frac{\ln (1+x)}{x}=1$$
	- $$\lim_{x \to +\infty}\frac{\ln (1+x)}{x}=0$$
	- $$\lim_{x \to -1^{-0}}\frac{\ln (1+x)}{x}=+\infty$$
- $$⁤\lim _{x\to 0} \frac{1- \cos x}{x^{2}}= \frac {1}{2}$$
- $$\lim _{x \to 0} \frac { \log _{a}(1+x)}{x}= \log _{a}e\quad(a>0,a \neq 1)$$
- $$\lim _{x\to 0} \frac {a^{x}-1}{x}= \ln a\quad(a>0,a \neq 1)$$
	- $$\lim _{x\to 0} \frac {e^{x}-1}{x}=1$$
- $$\lim_{x\to 0} \frac {(1+x)^{\mu}-1}{x}= \mu\quad(\mu为实数)$$
- $$\lim_{x\to 0}x\ln x=0$$
- $$\lim_{x\to 0}x^x=1$$
- $$\lim_{x\to +\infty}\frac{\ln x}{x}=0$$
- $$\lim_{x\to +0}\frac{\ln x}{x}=-\infty$$
- $$\lim_{x\to +\infty}x^{\frac{1}{x}}=1$$

- $$\lim_{x\to 0}\frac{\ln(x+\sqrt{1+x^2})}{x}=1$$
</details>

# 习题
## 通法
- 等价代换
  - 泰勒展开式代换
  - 等价无穷小因子代换
  - 非零因子代换
  - 变限积分等价无穷小代换
  - 逆用等价无穷小代换
- 比阶法
  - 抓大放小
- 代数等价变形
  - 倒带换 $x=\frac{1}{t}$
  - $f(x)^{g(x)}=e^{g(x)\ln f(x)}$
  - $\ln(1+x)\sim x\Rightarrow x-1\sim \ln x$
  - $f(x)^{g(x)}\sim 1\Rightarrow f(x)^{g(x)}-1\sim g(x)\ln f(x)$
  - $f(x)g(x)\sim 1\Rightarrow f(x)g(x)-1\sim\ln f(x)+\ln g(x)$
  - $a^c-b^c=b^c[(\frac{a}{b})^c-1]$
  - $a^b-a^c=a^c(a^{b-c}-1)$
  - $a^b-c^d=a^b-c^b+c^b-c^d$
## $\frac 00$未定式
- Calculate$$\lim_{x\to 0}\frac 1x\biggl(\frac 1{\sin x}-\frac 1{\tan x}\biggr)$$Hint 通分 & $\sin^2 x+\cos^2 x=1$
- Calculate$$\lim_{x\to 0}\frac{\ln(a+x)+\ln(a-x)-2\ln a}{x^2}$$Hint $\ln(1-\frac{x^2}{a^2})$
- Calculate$$\lim_{x\to 0}\frac{\sqrt{1-\cos x^2}}{1-\cos x}$$Hint 等价无穷小代换可以用在乘除, 不可用在加减
- Calculate$$\lim_{x\to a}\frac{\sqrt x-\sqrt a+\sqrt{x-a}}{\sqrt{x^2-a^2}}$$Hint 分离 & 根号化有理 & 小量化有界 & $x-a=(\sqrt{x-a})^2$
- Calculate$$\lim_{x\to 0}\frac{\sqrt{1+x}-\sqrt{1+x^2}}{\sqrt{1+x}-1}$$Hint $+1-1\quad (x\to 0)\ (1+x)^u-1=ux$
- Calculate$$\lim_{x\to 0}\frac{\tan mx}{\sin nx}$$Hint 分子分母同时补 $mnx$
- Calculate$$\lim_{x\to 0}\frac{\ln(1+x+x^2)+\ln(1-x+x^2)}{\sec x-\cos x}$$Hint 在不为乘积的情况下不要无穷小量代换
- Calculate$$\lim_{x\to 0}\frac 1x\ln\frac{e^x+e^{2x}+\cdots+e^{nx}}{n}$$Hint $\frac00$洛必达法则
- Calculate$$\lim_{x\to 0}\frac{\cos^{\sin x}x-1}{x^3}$$
- Calculate$$\lim_{x\to 0}\frac{(a+b)x+b}{\sqrt{3x+1}-\sqrt{x+3}}=4$$求$a,b$
- Calculate$$\lim_{x\to 0}\frac{(1+x\sin x)^x-1}{x^3}$$

==无理化整数==
- Calculate$$\lim_{n\to\infty}\sin(\sqrt{n^2+a^2}\pi)$$Hint 无理趋近于整数&对整数作差


==$\frac{\infty}{\infty}$未定式==

==无穷级数==
- Calculate$$\lim_{n\to\infty}\sum_{k=1}^n\frac{1}{k(1+k)}$$Hint 裂项相消 & 错位相减
- Calculate$$\lim_{n\to\infty}\sum_{k=1}^n\frac{1}{(2k-1)(2k+1)}$$Hint 裂项相消 & 错位相减
- Calculate$$\lim_{n\to\infty}\sum_{k=1}^n\frac{1}{(a+k-1)(a+k)(a+k+1)}\quad a>0$$Hint 裂项相消 & 错位相减
- Calculate$$\lim_{n\to\infty}\sum_{k=1}^n\frac{2k-1}{2^k}$$Hint 裂项相消 & 错位相减
- Calculate$$\lim_{n\to\infty}\sum_{k=1}^n\frac{x}{(1+x^2)^k}$$Hint 裂项相消 & 错位相减
- Calculate$$\lim_{n\to\infty}\sum_{k=0}^n\frac{x^k(1-x)^k}{2^k}$$Hint 裂项相消 & 错位相减
- Calculate$$\lim_{n\to\infty}\sum_{k=1}^n\frac{k}{(1+k)!}$$Hint 裂项相消 & 错位相减
- Calculate$$\lim_{n\to\infty}\sum_{k=1}^n\frac{1}{\sqrt{n^2+k}}$$Hint 裂项相消 & 错位相减









- Calculate$$\lim_{n\to\infty}\sum_{k=1}^n\frac{1}{(n+k)^2}$$Hint 裂项相消 & 错位相减


- Calculate$$\lim_{x\to 0}\frac{\cos^{\sin x}x-1}{x^3}$$


==$1^{\infty}$类型==
幂指函数求极限问题
- Calculate$$\lim_{n\to\infty}\biggl(\frac{2n+1}{2n-1}\biggr)^n$$化指数, 换极限
- Calculate$$\lim_{n\to\infty}\biggl(\frac{3n^2-2}{3n^2+4}\biggr)^{n(n+1)}$$化指数, 换极限
- Calculate$$\lim_{n\to\infty}\biggl(\frac{\sqrt[n]{a}+\sqrt[n]{b}}{2}\biggr)^n$$化指数, 换极限, 配 $\ln$, 对数内部加减难操作, 想办法提出外面来
- Calculate$$\lim_{n\to\infty}\biggl(\frac{\sqrt{n^2+1}}{n+1}\biggr)^n$$ 化指数, 换极限, 配 $\ln$
- Calculate$$\lim_{n\to\infty}\biggl(\frac{1}{n}+e^{\frac 1n}\biggr)^n$$ 化指数, 换极限, 配 $\ln$
- Calculate$$\lim_{x\to +0}\biggl(\cos\sqrt{x}\biggr)^{\frac 1x}$$
- Calculate$$\lim_{x\to 0}\biggl(\sqrt{1+x^2}+x\biggr)^{\frac 1x}$$

==$0\cdot\infty$类型==
- Calculate$$\lim_{n\to\infty}n(a^{\frac 1n}-1)$$
- Calculate$$\lim_{n\to\infty}n^2\biggl[e^{2-\frac 1n}+e^{2+\frac 1n}-2e^2\biggr]$$
- Calculate$$\lim_{n\to\infty}n^2\biggl[\ln(a+\frac 1n)+\ln(a-\frac 1n)-2\ln a\biggr]$$
- Calculate$$\lim_{n\to\infty}n\biggl[e^{\frac an}-e^{\frac bn}\biggr]$$
- Calculate$$\lim_{n\to\infty}n\biggl[\ln(n+1)-\ln n\biggr]$$
- Calculate$$\lim_{x\to\infty}x\biggl[\ln(x+1)-\ln(x-1)\biggr]$$
- Calculate$$\lim_{x\to+\infty}x\biggl[(x+2)\ln(x+2)-2(x+1)\ln (x+1)+x\ln x\biggr]$$
- Calculate$$\lim_{x\to\infty}x^2\biggl[\biggl(\frac{x+1}{x-1}\biggr)^{\frac 1x}-1\biggr]$$

****
# 我是隔离线
****
- 未定式"$1^{\infty}$"&"$\infty^0$"幂指函数求极限问题
- Calculate $$\lim_{x\to 0}\biggl(\frac{e^x+e^{2x}+\cdots+e^{nx}}{n}\biggr)^{\frac ex}$$
- 未定式"$\frac 00,\ \frac{\infty}{\infty},\ \infty\cdot 0$ " L'Hospital法则
## 极限的计算
==利用stolz定理求极限==
- Calculate$$\lim_{n\to\infty}\frac{1+\frac 12+\cdots+\frac 1n}{\ln n}$$Hint

==利用恒等变换求极限==
- 主要包括以下情形：
	- 完全平方差公式
	- 求和&求积裂项
	- 三角恒等变换
- (CMC-2014预赛)Calculate $$\lim_{n\to\infty}\sum_{k=1}^n\frac{k}{(k+1)!}$$Hint $\frac{k}{(k+1)!}=\frac 1k-\frac 1{k+1}$
> 解
> $$\begin{equation}\begin{split}x_n &=\sum_{k=1}^n\frac{k}{(k+1)!}\\&=\sum_{k=1}^{n}\biggl[\frac{1}{k!}-\frac{1}{(k+1)!}\biggr]\\&=1-\frac{1}{(n+1)!}\end{split}\end{equation}$$ 
> $$\lim_{n\to\infty}\sum_{k=1}^n\frac{k}{(k+1)!}=\lim_{n\to\infty}\biggl(1-\frac 1{(n+1)!}\biggr)=1$$
- (CMC-200)Calculate $$\lim_{n\to\infty}\cos\frac{\theta}{2}\cos\frac{\theta}{4}\cdots\cos\frac{\theta}{2^n}$$Hint $\sin 2x=2\sin x\cos x$
> 解
> 1. $\theta=0$$$\lim_{n\to\infty}a_n=1$$
> 2. $\theta\ne 0$$$\begin{equation}\begin{split}a_n&=\cos\frac{\theta}{2}\cos\frac{\theta}{2^2}\cdots\cos\frac{\theta}{2^n}\\&=\cos\frac{\theta}{2}\cos\frac{\theta}{2^2}\cdots\cos\frac{\theta}{2^n}2\sin\frac{\theta}{2^n}\frac{1}{2\sin\frac{\theta}{2^n}}\\&=\frac{\sin\theta}{2^n\sin\frac{\theta}{2^n}}\end{split}\end{equation}$$ 
> $$\lim_{n\to\infty}a_n=\lim_{n\to\infty}\frac{\sin\theta}{2^n\sin\frac{\theta}{2^n}}=\lim_{n\to\infty}\frac{\sin\theta}{2^n\frac{\theta}{2^n}}=\frac{\sin\theta}{\theta}$$
- 设$x_n=(1+a)(1+a^2)\cdots(1+a^{2^n}),其中\mid a\mid<1,求\lim_{n\to\infty}x_n$Hint 陪凑$\frac 1{1-a}$连续使用完全平方差公式
- 已知$\lim_{x\to 0}\frac{x}{f(3x)}=2$，求$\lim_{x\to 0}\frac{f(-2x)}{x}$Hint 凑出相同的元进行换元

==利用夹逼定理==
- Find $$\lim_{n\to\infty}(n!)^{\frac 1{n^2}}$$Hint 转化为$e^{\ln(n!)\frac 1{x^2}}$
> 解
> 
- Find $$\lim_{x\to+\infty}\sqrt[3]x\int_x^{x+1}\frac{\sin t}{\sqrt{t+\cos t}}\text dx$$

==利用等价无穷小代换==
- Calculate $$\lim_{x\to 0}\frac{1-\cos x\sqrt{\cos 2x}\sqrt[3]{\cos 3x}}{x^2}$$
- 设$f(x),g(x)$在$x=0$的某一邻域$U$内有定义，对$\forall x\in U,f(x)\neq g(x)$且$\lim_{x\to 0}f(x)=\lim_{x\to 0}g(x)=A>0$，则$$\lim_{x\to 0}\frac{[f(x)]^{g(x)}-[g(x)]^{g(x)}}{f(x)-g(x)}$$

==利用洛必达法则==
==利用泰勒公式==
==利用导数定义==
==利用定积分定义==
==利用数列极限定义==
==有关函数连续性==
==其他==
- Calculate$$\lim_{n\to\infty}(1+n+\frac {n^2}2+\cdots+\frac{n^n}{n!})e^{-n}$$
- Calculate$$\lim_{x\to 0}\frac{e^{(1+x)^{\frac 1 x}}-(1+x)^{\frac e x}}{x^2}$$
- Calculate$$\lim_{x\to 0}\frac{\ln(e^{\sin x}+\sqrt[3]{1-\cos x})-\sin x}{\arctan(4\sqrt[3]{1-\cos x})}$$Hint


# 连续性
- 连续性(逐点连续)
- 一致连续
- 半连续函数
	- 上半连续
	- 下半连续
- 等度连续
- 一致等度连续
- Lipschitz 连续
- 