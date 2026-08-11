# LeakyReLU 激活函数简介

## 1. 什么是 LeakyReLU

**LeakyReLU（Leaky Rectified Linear Unit）** 是 ReLU 激活函数的一种改进版本。它解决了 ReLU 在负值区域神经元"死亡"的问题。

### 1.1 数学定义

$$
f(x) = \begin{cases}
x & \text{if } x > 0 \\
\alpha x & \text{if } x \leq 0
\end{cases}
$$

其中 **α（alpha）** 是一个很小的正数，通常取值为 0.01。

### 1.2 导数

$$
f'(x) = \begin{cases}
1 & \text{if } x > 0 \\
\alpha & \text{if } x \leq 0
\end{cases}
$$


## 2. 与其他激活函数的对比

| 激活函数 | 公式 | 优点 | 缺点 |
|---------|------|------|------|
| **ReLU** | max(0, x) | 计算简单，收敛快 | 神经元死亡问题 |
| **LeakyReLU** | max(αx, x) | 解决神经元死亡 | 需要调参 α |
| **PReLU** | 可学习参数 α | 自适应 | 增加参数量 |
| **ELU** | x>0: x, x≤0: α(e^x-1) | 输出均值接近0 | 计算复杂度高 |
| **Sigmoid** | 1/(1+e^-x) | 平滑，可解释性强 | 梯度消失 |
| **Tanh** | (e^x-e^-x)/(e^x+e^-x) | 零中心化 | 梯度消失 |



## 3. LeakyReLU 的优势

### 3.1 解决神经元死亡问题
- ReLU 在负值区域梯度为 0，导致神经元无法更新
- LeakyReLU 在负值区域保留小梯度（αx），允许梯度流动

### 3.2 计算效率高
- 几乎与 ReLU 同样简单快速
- 不需要指数运算或复杂计算

### 3.3 保持稀疏性
- 虽然负值有小梯度，但正值的稀疏性仍然保持

---

## 4. 主要变体

### 4.1 PReLU (Parametric ReLU)
```python
# PReLU 的 α 是可学习的参数
f(x) = max(αx, x)  # α 通过反向传播学习