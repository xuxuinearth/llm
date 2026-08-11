# ReLU 激活函数详解

## 1. 什么是 ReLU

**ReLU（Rectified Linear Unit，修正线性单元）** 是目前深度学习中最常用的激活函数之一。它于 2010 年由 Nair 和 Hinton 提出，因其简单高效而广泛应用于各类神经网络中。

### 1.1 数学定义

$$
f(x) = \max(0, x) = \begin{cases}
x & \text{if } x > 0 \\
0 & \text{if } x \leq 0
\end{cases}
$$

### 1.2 导数

$$
f'(x) = \begin{cases}
1 & \text{if } x > 0 \\
0 & \text{if } x \leq 0
\end{cases}
$$




