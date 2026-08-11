# tanh 激活函数

**tanh**（双曲正切函数，Hyperbolic Tangent）是一种经典的非线性激活函数，输出范围在 $(-1, 1)$ 之间，是 Sigmoid 函数的零中心化版本。



## 数学定义

$$ \text{tanh}(x) = \frac{e^{x} - e^{-x}}{e^{x} + e^{-x}} $$

或等价地：

$$ \text{tanh}(x) = 2 \cdot \sigma(2x) - 1 $$

其中 $\sigma(x) = \frac{1}{1 + e^{-x}}$ 是 Sigmoid 函数。



## 函数图像特征
