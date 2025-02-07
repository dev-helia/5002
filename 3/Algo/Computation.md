

---

# **对数和指数**

## **1. 指数函数（Exponentiation Function）**

### **定义**
指数函数 $\exp_b : \mathbb{R} \rightarrow \mathbb{R}^+$ 定义为：
$$
\exp_b(x) = b^x
$$
其中：
- $b$ 是**正实数**且 $b \neq 1$（称为底数）。
- $x$ 是指数。

---

### **指数的性质**
对于任意正实数 $b, c$ 和任意实数 $x, y$，以下性质成立：

1. **加法法则**：
   $$
   b^x \cdot b^y = b^{x+y}
   $$

2. **乘法法则**：
   $$
   (b^x)^y = b^{xy}
   $$

3. **除法法则**：
   $$
   \frac{b^x}{b^y} = b^{x-y}
   $$

4. **乘积的指数**：
   $$
   (bc)^x = b^x \cdot c^x
   $$

---

## **2. 对数函数（Logarithmic Function）**

### **定义**
对数函数是指数函数的逆函数。当 $b > 0$ 且 $b \neq 1$ 时，定义 $\log_b : \mathbb{R}^+ \rightarrow \mathbb{R}$ 为：
$$
b^x = y \iff \log_b y = x
$$
- $b$ 是底数，$y$ 是对数函数的输入。

---

### **对数的性质**

1. **加法法则**：
   $$
   \log_b(xy) = \log_b x + \log_b y
   $$

2. **减法法则**：
   $$
   \log_b \left(\frac{x}{y}\right) = \log_b x - \log_b y
   $$

3. **幂法则**：
   $$
   \log_b(x^y) = y \log_b x
   $$

4. **换底公式**：
   $$
   \log_c x = \frac{\log_b x}{\log_b c}
   $$

---

### **常见公式总结**
1. **换底公式**：
   $$
   \log_a b = \frac{\log_c b}{\log_c a}
   $$

2. **对数与指数的逆关系**：
   $$
   a^{\log_a b} = b \quad \text{且} \quad \log_a(a^x) = x
   $$

3. **特殊值**：
   $$
   \log_a 1 = 0 \quad \text{和} \quad \log_a a = 1
   $$

4. **倒数性质**：
   $$
   \log_a b = \frac{1}{\log_b a}
   $$

---

## **3. 严格递增与递减**

1. 当 $b > 1$ 时，$f(x) = b^x$ 和 $f(x) = \log_b x$ 都是**严格递增函数**。
2. 当 $0 < b < 1$ 时，$f(x) = b^x$ 和 $f(x) = \log_b x$ 都是**严格递减函数**。

**示例**：
- 若 $\log_3 81 = 4$ 且 $\log_3 243 = 5$，则 $\log_3 200$ 的值介于 4 和 5 之间。

---

## **4. 应用示例**

### 示例 1：指数函数描述人口增长
假设某岛的蜥蜴数量随时间呈指数增长：
$$
\text{liz}(t) = p \cdot b^t
$$
其中：
- $p$ 是初始数量，
- $b$ 是增长速率，
- $t$ 是时间。

若蜥蜴数量从 $p$ 增长到 $n$，求所需时间 $t$：
$$
n = p \cdot b^t \implies \frac{n}{p} = b^t \implies t = \log_b \left(\frac{n}{p}\right)
$$

---
