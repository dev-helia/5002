> [!NOTE]
>
> T(N) = O(N) 前面是具体的准确的公式,后面是big O.


> [!TIP]
>
> 假如n是具体的值,可以暂时不求通解,简单地进行化解,时间更快,也更容易.

>[!WARNING]
>
> 注意是怎么展开的,先不要合并.


---

### **递归方程及主定理分析**

|**递归公式**|**复杂度解**|**说明**|
|---|---|---|
|T(n)=2T(n2)+nT(n) = 2T\left(\frac{n}{2}\right) + n|O(nlog⁡n)O(n \log n)|归并排序等分治法场景：分成两部分，各自解决，再合并，合并的时间是线性 nn。|
|T(n)=T(n2)+1T(n) = T\left(\frac{n}{2}\right) + 1|O(log⁡n)O(\log n)|二分查找场景：每次将问题规模缩小一半，每次操作时间是常数 O(1)O(1)。|
|T(n)=4T(n2)+nT(n) = 4T\left(\frac{n}{2}\right) + n|O(n2)O(n^2)|分治问题中，分成四部分解决，每次合并代价是线性 nn。|
|T(n)=6T(n3)+nT(n) = 6T\left(\frac{n}{3}\right) + n|O(nlog⁡36)O(n^{\log_3 6})|分治问题，划分为6个子问题，每个问题的大小为原来的 1/31/3，合并代价是线性 nn。|

---

# 解$T(n) = 6T\left(\frac{n}{3}\right) + n $ 递归公式

### 递归展开



我们从递归式开始：
$$
T(n) = 6T\left(\frac{n}{3}\right) + n
$$

继续递归展开 $T\left(\frac{n}{3}\right)$：
$$
T(n) = 6\left(6T\left(\frac{n}{9}\right) + \frac{n}{3}\right) + n = 6^2T\left(\frac{n}{9}\right) + 6 \cdot \frac{n}{3} + n
$$

继续展开 $T\left(\frac{n}{9}\right)$：
$$
T(n) = 6^2\left(6T\left(\frac{n}{27}\right) + \frac{n}{9}\right) + 6 \cdot \frac{n}{3} + n = 6^3T\left(\frac{n}{27}\right) + 6^2 \cdot \frac{n}{9} + 6 \cdot \frac{n}{3} + n
$$

---

### 找到一般项

我们可以发现一个模式，每次递归展开后，系数为 $6^k$，而自变量变成 $\frac{n}{3^k}$。因此，经过 $k$ 次展开后，我们可以得到：
$$
T(n) = 6^k T\left(\frac{n}{3^k}\right) + n \sum_{i=0}^{k-1} \frac{6^i}{3^i}
$$

---

### 当 $k = \log_3 n$ 时停止展开

我们继续展开，直到 $\frac{n}{3^k} = 1$，即 $k = \log_3 n$。此时，$T(1) = 1$，所以：
$$
T(n) = 6^{\log_3 n} \cdot T(1) + n \sum_{i=0}^{\log_3 n - 1} \frac{6^i}{3^i}
$$

---

### 计算 $6^{\log_3 n}$

利用指数和对数的性质 $6^{\log_3 n} = n^{\log_3 6}$，因此我们有：
$$
T(n) = n^{\log_3 6} + n \sum_{i=0}^{\log_3 n - 1} \frac{6^i}{3^i}
$$

---

### 计算求和项

观察到 $\sum_{i=0}^{\log_3 n - 1} \frac{6^i}{3^i}$ 是一个等比数列，公比为 $\frac{6}{3} = 2$。对于等比数列求和公式：
$$
\sum_{i=0}^{k-1} r^i = \frac{r^k - 1}{r - 1}
$$

这里 $r = 2$，所以：
$$
\sum_{i=0}^{\log_3 n - 1} 2^i = 2^{\log_3 n} - 1 = n^1 - 1 = O(n)
$$

---

### 最终结果

因此，递归式的解为：
$$
T(n) = n^{\log_3 6} + O(n) = \Theta(n^{\log_3 6})
$$

---

# Sequence
==constant ：common difference==

## 算术数列 Arithmetic series
==constant, first term, counts==[]()
算术数列的一般公式为：
$$ T(n) = \text{first term} + (n - 1) \times \text{common difference} $$


示例：
若数列的初项为 $a$，公差为 $d$，则
$$
T(n) = a + d \cdot (n - 1)
$$
==算术数列求和==:

部分和的公式为：
$$
\text{Sum} = \frac{\text{first term} + \text{last term}}{2} \times \text{number of terms}
$$

例如，对于数列 7, 12, 17, 22,...,177，计算其和。

#### 步骤：

1. ==求数列项数：==
   $$
   \text{number of terms} = \frac{177 - 7}{5} + 1 = 35
   $$

2. 计算和：
   $$
   \text{Sum} = \frac{(15 + 175) \times 35}{2}
   $$




## 几何数列 Geometric sequence

几何数列的通项公式为：
$$ T(n) = \text{first term} \cdot q^{n-1} $$

示例：
若数列的初项为 $a$，公比为 $q$，则
$$
T(n) = a \cdot q^{n-1}
$$
==几何级数求和 a start constant r difference constant==

几何级数的求和公式为：
$$
S = \frac{a(1 - r^n)}{1 - r} \quad (r \neq 1)
$$

示例：
对于数列 $S = 1 + 3 + 3^2 + \dots + 3^6$，计算其和。

步骤：

1. 将数列表示为 $S = a + ar + ar^2 + \dots + ar^{n-1}$

2. 使用公式：
   $$
   S = \frac{a(1 - r^n)}{1 - r}
   $$


## 二次数列 Quadratic series

二次数列的一般公式为：
$$ T(n) = an^2 + bn + c $$

示例：
若数列的系数为 $a$、$b$、$c$，则
$$
T(n) = an^2 + bn + c
$$
需要三个公式才能求解

可以使用线性代数来求解二次数列中的未知系数 $a$、$b$、$c$。

二次数列的通项公式为：
$$
T(n) = an^2 + bn + c
$$

如果我们知道几个特定项的值，例如 $T(1), T(2), T(3)$，我们可以通过这三个已知项的方程构建一个线性方程组，利用矩阵的形式求解 $a$、$b$、$c$ 的值。

### 步骤

假设已知以下项的值：
- $T(1) = d_1$
- $T(2) = d_2$
- $T(3) = d_3$

那么可以得到以下方程组：
1. $a \cdot 1^2 + b \cdot 1 + c = d_1$
2. $a \cdot 2^2 + b \cdot 2 + c = d_2$
3. $a \cdot 3^2 + b \cdot 3 + c = d_3$

可以将其表示为矩阵形式：
$$
\begin{bmatrix}
1 & 1 & 1 \\
4 & 2 & 1 \\
9 & 3 & 1
\end{bmatrix}
\begin{bmatrix}
a \\
b \\
c
\end{bmatrix}
=
\begin{bmatrix}
d_1 \\
d_2 \\
d_3
\end{bmatrix}
$$

此时，通过求解矩阵方程
$$
AX = B
$$
其中 $ A $ 是系数矩阵，$ X $ 是包含 $ a $、$ b $、$ c $ 的向量，$ B $ 是已知项的向量，可以求解 $ X $ 来得到 $ a $、$ b $、$ c $ 的值。

### 解法

1. 计算 $A^{-1}$（如果 $ A $ 是可逆的），然后 $X = A^{-1} B$。
2. 直接使用高斯消元法或者其他矩阵解法求解该方程组。

这种方法可以有效地求出二次数列中的系数 $a$、$b$、$c$，适用于只知道少量项的情况下的系数求解。


## 部分求和公式

### 部分和的表示

对于符号求和，使用 Sigma 符号表示上下界。upper bond  k 是“迭代变量”或“索引”

$$
\sum_{k=1}^{n} 6k
$$





