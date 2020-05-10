# Reading Comprehension

## 前提理论

### 动态规划

动态规划是一种在数学、管理科学、计算机科学、经济学和生物信息学中使用的，通过把原问题分解为相对简单的子问题的方式求解负责问题的方法。

动态规划背后的思想大致是，若要解决一个问题，我们解其不同部分，再根据子问题的解以得出原问题的解。通常情况下，许多子问题非常相似，为此动态规划试图仅仅解决每个子问题，从而减少计算量：一旦某个给定子问题的解已经算出，则将其记忆化存储，以便下次需要同一子问题解时直接查表。这种做法在重复子问题的数目关于输入的规模呈指数增长时特别有用。

点击[这里](https://leetcode-cn.com/tag/dynamic-programming/)，可以在leetcode上找到很多很多关于动态规划的算法题，而且都有详细解释。

下面给出课上老师给出的两个例子：

1、N个矩阵相乘，求一个计算顺序让总计算次数最少。

如矩阵$m_1$、$m_2$、$m_3$、$m_4$，分别是5x20、20x50、50x1、1x100的矩阵。那么：

- 如果是$(((m_1 * m_2) * m_3) * m_4)$的顺序，则需要5x20x50+5x50+5x100次乘法运算，即5750次
- 如果是$((m_1 * (m_2 * m_3)) * m_4)$的顺序，则需要20x50x1+5x20x1+5x1x100次乘法运算，即1600次
- 其他以此类推


2、求两个字符串的最长公共子序列。如$X=abcbdab$，$Y=bdcaba$，$Z=bcab$。