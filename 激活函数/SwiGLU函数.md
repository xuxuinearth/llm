## SwiGLU 激活函数

**SwiGLU** (Swish-Gated Linear Unit) 的数学定义：

$$ \text{SwiGLU}(a, b) = \text{Swish}(a) \odot \sigma(b) $$

其中：
- **Swish**(a) = a · sigmoid(a)  — 非线性激活
- **σ(b)** = sigmoid(b)  — 门控信号（0~1 之间）
- **⊙** 表示逐元素乘法（Hadamard 乘积）

---

### 直观理解

| 分支 | 作用 |
|------|------|
| Swish(a) | 主信息流（经过非线性变换） |
| σ(b) | 门控开关（决定哪些信息通过） |
| ⊙ | 逐元素相乘，实现门控 |

### 实际应用

在 Transformer 的 FFN 中：

$$ \text{FFN}(x) = (\text{Swish}(xW_1) \odot \sigma(xW_2)) \cdot W_3 $$

这是 LLaMA、PaLM、Mistral 等现代 LLM 的标准配置。