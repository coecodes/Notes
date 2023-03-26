单词在日常用语中的流行程度: 我们认为出题人考虑了单词的易用性和常见性, 事实上确实如此, 我们在对wordle的调查当中找到了出题集。

自然语言处理

wordle wordlist

树状图分类

单词相似度: 分5级
0个相同
1个相同
2个相同
3个相同
4个相同

对不同人

我们所认为合法的单词都在12972

第一次全灰的概率为14%

对于每一个瓷砖我们可以获得的信息有:
该词不在单词当中, 这里我们获得的信息由字母在单词库中的词频决定
该词在单词中, 这里我们可以获得信息

玩游戏群体的质量固定
玩游戏群体不随时间变化

prediction interval

词语的属性:
- 一个单词最少由三种不同的字母组成 3，4，5 有 311, 221, 2111, 11111 四种可能的分布情况。
- 相似度分析
  - Jaro-Winkler Distance
  - 信息熵

我们假定每一位玩家的目标都是尽可能少的次数猜出答案。

# Problem
-  The number of reported results vary daily. Develop a model to explain this variation and use your model to create a prediction interval for the number of reported results on March 1, 2023. 
- 报告结果的数量每天都在变化。建立一个模型来解释这种变化，并用你的模型为2023年3月1日的报告结果数量创建一个预测区间。1, 2023. 

- Do any attributes of the word affect the percentage of scores reported that were played in Hard Mode? If so, how? If not, why not? 
- 词语的任何属性是否会影响报告的分数的百分比？在困难模式下进行的得分的百分比？如果是，如何影响？如果没有，为什么没有？

- For a given future solution word on a future date, develop a model that allows you to predict the distribution of the reported results. In other words, to predict the associated percentages of (1, 2, 3, 4, 5, 6, X) for a future date. 
- 对于一个给定的未来的解决方案，开发一个模型，使你能够在未来的某一天预测报告结果的分布。换句话说，要预测未来某个日期的（1，2，3，4，5，6，X）的相关百分比。

- What uncertainties are associated with your model and predictions? Give a specific example of your prediction for the word EERIE on March 1, 2023. How confident are you in your model’s prediction? 你的模型和预测有哪些不确定因素？举一个具体的例子，说明你对2023年3月1日的EERIE这个词的预测。你对你的模型的预测有多大信心？

- Develop and summarize a model to classify solution words by difficulty. Identify the attributes of a given word that are associated with each classification. Using your model, how difficult is the word EERIE? Discuss the accuracy of your classification model. 
- 开发并总结一个模型，按难度对解题词汇进行分类。找出与每个分类相关的给定单词的属性。使用你的模型，EERIE这个词的难度如何？讨论一下你的分类模型的准确性。

- List and describe some other interesting features of this data set.
- 列出并描述这个数据集的一些其他有趣的特征。

# Solve
- ARIMA 时间序列分析
- wordle 具有相当社交属性，在前期获得大量的游戏用户，后因为游戏体验单一而快速走向衰败。不断的有新用户加入和旧用户流失，因为无法长期保有现存的用户，同时社交热度下降，导致下降。游戏泡沫周期模型。
- 假定会影响, 我们采用极端思考的方式，若出现一个极为冷门的单词。
- 将单词定量化, 建立单词之间的相似度关系, 观察相似单词的百分比数据是否相关。

- 不确定因素
- 相比失败和很多次才能完成，1次或两次完成的用户更倾向于炫耀，相比总体这个样本完成次数总体偏小。
- 随时间推移，玩家将更有经验。

- 

$$5\log(26)/\log(2)- \min\{\prod_{i=1}^{5-G-Y}\log(26-B-Y_i), \prod_{k=1}^Y\log(26-B-)\}/\log(2)$$

$$r=\dfrac{n\sum xy-\sum x\sum y}{\sqrt{n\sum x^2-(\sum x)^2}\sqrt{n\sum y^2-(\sum y)^2}}$$


- entropy
- neighbours
- repeat_letter
- holiday
- week
- n
- v
- adj
- adv


- Failed
- Hard_per
- Score_all
- Score_success
- difficlut

常用的模型与算法评价模型：

层次分析、Topsis(优劣解距离法)、数据包络分析(DEA)、模糊综合评价、秩和比综合评价、主成分分析、灰色关联分析法

预测分析模型：微分方程模型、差分方程模型、回归分析、时间序列、马尔可夫、神经网络、插值拟合、混沌序列预测、小波分析预测、灰色预测模型

优化模型：

数学规划模型（多目标、单目标、0-1整数规划等）、复杂网络优化、排队论与计算机仿真、图论、博弈论

数理统计模型：多元分析（主成分分析、聚类分析、因子分析、判别分析、典型相关性分析等）、相关回归分析、假设检验、方差检验、贝叶斯统计

分类与判别算法：

距离聚类(系统聚类)、关联性聚类，层次聚类、贝叶斯分类与判别、SVM支持向量机、决策树、极限学习机

排名算法

常见程度

可以发现，随着时间的变化，报告结果数量先增后减。增属于一个吸引玩家的过程，减属于玩家因为某些原因不再参与此游戏，退出游戏的人大于参与游戏的人。可以把某些原因具体分析分析，比如难度大、单词量积累不够、厌倦心理等等

正态性检验
方差其检验
差异性分析

Hard mod
数量分析
概率分析

ADF
RSS
PCA
KMO统计值


正态化

$26\times 5$

每有一个G, $(26-B)\times (5-G)$, 这里 G B 是指字母不同的色块的数目。

在 $(26-B)\times (5-G)$ 的区域中我们去考虑剩余格子内 Y 的作用。Y 所具有的信息既有列位置也有行位置。Y 的字母

$$PMI(x,y)=\log\frac{p(x,y)}{p(x)\cdot p(y)}$$

现在的频率有单词

wordle in 