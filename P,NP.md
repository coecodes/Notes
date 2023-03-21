- (P 多项式时间) 可在多项式时间内判定的YES/NO问题. 能用经典计算机求解的大多数问题
- (NP 非确定性多项式时间) 可在多项式时间内验证答案是YES的YES/NO问题.
- (NP完全 非确定性多项式时间(完全)) NP中最难的问题. 布尔可满足性问题、哈密顿路径问题等
- (NP困难 非确定性多项式时间(困难)) 比NP难的问题. 旅行推销员问题、背包问题、最大割问题等
- (NPI 非确定性多项式时间(过渡)) 介于P和NP完全之间的问题. 质因数分解问题等
- (BOP 有界错误量子多项式时间) 可在多项式时间内通过量子算法以大于2/3的准确率判定的YES/NO问题. 质因数分解问题、离散对数问题等
布尔满足性问题 （SAT）
背包问题
哈密顿路径问题
旅行推销员问题（决策版）
子图同构问题
子集和问题
集团问题
顶点覆盖问题
独立集问题
支配集问题
图形着色问题

```mermaid
flowchart TB
A[Circuit-SAT]-->B[SAT]-->C[3-CNF SAT]-->D[Clique Problem]-->F[Vertex Cover Problem]-->G[Hamiltonian Cycle]-->H[Travelling Salesman]
C-->E[Subset Problem]