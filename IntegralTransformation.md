# Fourier Transformation
## Fourier 级数
- 内积: 对于连续空间 $[a,b]$ 上的函数 $f(x),g(x)$, 我们将其视为无限维的向量, 定义其上的内积为 $$<f(x),g(x)>=\int_{a}^{b}f(x)g(x)\text dx$$
- 正交函数: 对于连续空间 $[a,b]$ 上的函数 $f(x),g(x)$, 若其内积为 $$<f(x),g(x)>=\int_{a}^{b}f(x)g(x)\text dx=0$$ 则我们称其为互为正交函数.
\paragraph{正交函数集} 对于函数集合, 对于其中任意两个不同的函数, 其内积都为 $0$, 则称该集合为正交函数集.
- 三角函数系: 对于区间 $[a,b]$ 上的函数集 $$\{1,\cos \omega x,\sin \omega x,\cos 2\omega x,\sin 2\omega x,\cdots\},\ \omega=\dfrac{2\pi}{b-a}$$ 为正交函数集.

- 引理1: $1$ 与 $\cos n\omega x$ 为正交函数.
<details>
<summary>Proof</summary>

$$\begin{align*}
    &\int_{a}^{b}\cos n\omega x\text dx \\ =& \dfrac{\sin n\omega x}{n\omega}\bigg|_a^b \\ =& \dfrac{1}{n\omega}\left(\sin n\omega b-\sin n\omega a\right) \\ =& \dfrac{1}{n\omega}\left(\sin n\omega b-\sin (n\omega a+2n\pi)\right) \\ =& \dfrac{1}{n\omega}\left(\sin n\omega b-\sin n\omega b\right) \\ =& 0
\end{align*}$$
</details>

- 引理2: $1$ 与 $\sin n\omega x$ 为正交函数.

<details>
<summary>Proof</summary>
$$\begin{align*}
    &\int_{a}^{b}\sin n\omega x\text dx \\ =& \dfrac{-\cos n\omega x}{n\omega}\bigg|_a^b \\ =& \dfrac{1}{n\omega}\left(\cos n\omega a-\cos n\omega b\right) \\ =& \dfrac{1}{n\omega}\left(\cos n\omega a-\cos (n\omega b-2n\pi)\right) \\ =& \dfrac{1}{n\omega}\left(\cos n\omega a-\cos n\omega a\right) \\ =& 0
\end{align*}$$
</details>

- 引理3: $\cos n\omega x$ 与 $\cos m\omega x$ 为正交函数 $(n\ne m)$.
<details>
<summary>Proof</summary>

$$\begin{align*}
    &\int_{a}^{b}\cos n\omega x\cos m\omega x\text dx \\ =& \dfrac{1}{2} \int_{a}^{b}\cos (n+m)\omega x\text dx+\dfrac{1}{2}\int_{a}^{b}\cos (n-m)\omega x\text dx \\ =& 0
\end{align*}$$
</details>

- 引理4: $\sin n\omega x$ 与 $\sin m\omega x$ 为正交函数 $(n\ne m)$.
<details>
<summary>Proof</summary>

$$\begin{align*}
    &\int_{a}^{b}\sin n\omega x\sin m\omega x\text dx \\ =& \dfrac{1}{2} \int_{a}^{b}\cos (n+m)\omega x\text dx-\dfrac{1}{2}\int_{a}^{b}\cos (n-m)\omega x\text dx \\ =& 0
\end{align*}$$
</details>

- 引理5: $\sin n\omega x$ 与 $\cos m\omega x$ 为正交函数.
<details>
<summary>Proof</summary>

$$\begin{align*}
    &\int_{a}^{b}\sin n\omega x\cos m\omega x\text dx \\ =& \dfrac{1}{2} \int_{a}^{b}\sin (n+m)\omega x\text dx+\dfrac{1}{2}\int_{a}^{b}\sin (n-m)\omega x\text dx \\ =& 0
\end{align*}$$
综上, 上述两两互为正交函数.
</details>

- 黎曼-勒贝格定理: 若 $f(x)$ 在 $[a,b]$ 上绝对可积, 则 $$\lim_{p\to+\infty}\int_{a}^{b}f(x)\sin(px)\text dx=0$$ $$\lim_{p\to+\infty}\int_{a}^{b}f(x)\cos(px)\text dx=0$$
Proof: 
$$\bigg|\int_{a}^{b}\sin(px)\text dx\bigg|=\bigg|\dfrac{\cos(pa)-\cos(pb)}{p}\bigg|\le\dfrac{2}{p}$$

- Dirichlet 核
- 黎曼局部化定理
- Dini 判别法
- Lipschitz 判别法

- Dirichlet 条件: 一个以 $T$ 为周期的函数 $f_T(t)$, 如果在 $\left[-\dfrac{T}{2},\dfrac{T}{2}\right]$ 上满足:
1. 连续或只有有限个第一类间断点.
2. 只有有限个极值点.

- Fourier 级数: 如果一个以 $T$ 为周期的函数 $f_T(t)$ 满足 Dirichlet 条件, 则在 $\left[-\dfrac{T}{2},\dfrac{T}{2}\right]$ 上可以展开为 Fourier 级数, 在 $f_T(t)$ 的连续点处, 级数的三角形式为 $$f_T(t)=\dfrac{a_0}{2}+\sum_{n=1}^{\infty}(a_n\cos n\omega t+b_n\sin n\omega t)$$

<details>
<summary>Proof</summary>

$$f(x)=\dfrac{a_0}{2}+\sum_{n=1}^{\infty}(a_n\cos n\omega x+b_n\sin n\omega x)$$
$$\begin{align*}
    &\int_{a}^{b}f(x)\text dx \\ =& \int_{a}^{b}\dfrac{a_0}{2}\text dx+\sum_{n=1}^{\infty}(\int_{a}^{b}a_n\cos n\omega x\text dx+\int_{a}^{b}b_n\sin n\omega x\text dx) \\ =& \int_{a}^{b}\dfrac{a_0}{2}\text dx
\end{align*}$$
$$a_0=\dfrac{2}{b-a}\int_{a}^{b}f(x)\text dx$$
</details>

<details>
<summary>Proof</summary>

$$f(x)=\dfrac{a_0}{2}+\sum_{n=1}^{\infty}(a_n\cos n\omega x+b_n\sin n\omega x)$$
两边同时乘以 $\cos k\omega x$
$$\begin{align*}
    &f(x)\cos k\omega x \\ =& \dfrac{a_0}{2}\cos k\omega x+\sum_{n=1}^{\infty}(a_n\cos n\omega x\cos k\omega x \\ &+b_n\sin n\omega x\cos k\omega x)
\end{align*}$$
$$\begin{align*}
    &\int_{a}^{b}f(x)\cos k\omega x\text dx \\ =& \int_{a}^{b}\dfrac{a_0}{2}\cos k\omega x\text dx+\sum_{n=1}^{\infty}(\int_{a}^{b}a_n\cos n\omega x\cos k\omega x\text dx \\ &+\int_{a}^{b}b_n\sin n\omega x\cos k\omega x\text dx) \\ =& \int_{a}^{b}a_k\cos^2 k\omega x\text dx
\end{align*}$$
$$a_k=\dfrac{\int_{a}^{b}f(x)\cos k\omega x\text dx}{\int_{a}^{b}\cos^2 k\omega x\text dx}$$
Proof:
$$f(x)=\dfrac{a_0}{2}+\sum_{n=1}^{\infty}(a_n\cos n\omega x+b_n\sin n\omega x)$$
两边同时乘以 $\sin k\omega x$
$$\begin{align*}
    &f(x)\sin k\omega x \\ =& \dfrac{a_0}{2}\sin k\omega x+\sum_{n=1}^{\infty}(a_n\cos n\omega x\sin k\omega x \\ &+b_n\sin n\omega x\sin k\omega x)
\end{align*}$$
$$\begin{align*}
    &\int_{a}^{b}f(x)\sin k\omega x\text dx \\ =& \int_{a}^{b}\dfrac{a_0}{2}\sin k\omega x\text dx+\sum_{n=1}^{\infty}(\int_{a}^{b}a_n\cos n\omega x\sin k\omega x\text dx \\ &+\int_{a}^{b}b_n\sin n\omega x\sin k\omega x\text dx) \\ =& \int_{a}^{b}b_k\sin^2 k\omega x\text dx
\end{align*}$$
$$b_k=\dfrac{\int_{a}^{b}f(x)\sin k\omega x\text dx}{\int_{a}^{b}\sin^2 k\omega x\text dx}$$
</details>

## Fourier 积分

## 傅里叶变换
- Fourier 变换: 若函数 $f(t)$ 在 $(-\infty,\infty)$ 上满足 Fourier 积分定理的条件, 则称函数 $$F(\omega)=\int_{-\infty}^{\infty}f(t)e^{-i\omega t}\text dt$$
- Fourier 逆变换:
## 卷积
- 卷积: 若已知函数 $f_1(x),f_2(x)$ 则积分 $$\int_{-\infty}^{+\infty} f_1(t)f(x-t)\text dt$$ 称为 $f_1(x),f_2(x)$ 的卷积, 记为 $f_1(x)\star f_2(x)$ 即 $$\int_{-\infty}^{+\infty} f_1(t)f(x-t)\text dt=f_1(x)\star f_2(x)$$
- (交换律): $$f_1(x)\star f_2(x)=f_2(x)\star f_1(x)$$
- (结合律): $$f_1(x)\star [f_2(x)\star f_3(x)]=[f_1(x)\star f_2(x)]\star f_3(x)$$

<details>
<summary>Emple</summary>

</details>