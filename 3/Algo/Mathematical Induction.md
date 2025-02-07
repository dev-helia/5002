1. Base case
2. Assume
3. Inductive Step : goal: we want to prove
	1. use assumption: According to the recursive definition
	2. Substitute the inductive hypothesis
	3. Also, according to the non-recursive formula
4. conclusion
	We have thus shown that if the statement holds for k it holds for k + 1. In combination with
our base case, and by the principle of mathematical induction, the statement holds for all
n ≥2.


#### 1.基础情况 (Base Case) 

> [!TIP]
>
> base case

**Base Case**

当 $n = 1$ 时:
**When $n = 1$:**

$$
T(1) = 1
$$

而根据公式 $T(n) = 2n - 1$，当 $n = 1$ 时:
**According to the formula $T(n) = 2n - 1$, when $n = 1$:**

$$
T(1) = 2 \times 1 - 1 = 1
$$

因此，基础情况成立。
**Thus, the base case holds.**

#### 2.归纳假设 (Inductive Hypothesis)

> [!TIP]
>
> assume

**Inductive Hypothesis**

假设对于某个正整数 $k$，$T(k) = 2k - 1$ 是成立的。
**Assume that for a positive integer $k$, $T(k) = 2k - 1$ holds.**

#### 3.归纳步骤 (Inductive Step)

> [!TIP]
>induction step
> goal:  we want to aprove
> steps: use assumption

**Inductive Step**

我们需要证明对于 $n = k + 1$ 的情况也成立，即 $T(k + 1) = 2(k + 1) - 1$。
==**We need to prove that for $n = k + 1$, the statement also holds, i.e., $T(k + 1) = 2(k + 1) - 1$.**==

根据递归定义:
==**According to the recursive definition:**==
$$
T(k + 1) = T(k) + 2
$$

利用归纳假设 $T(k) = 2k - 1$ 代入:
==**Substitute the inductive hypothesis $T(k) = 2k - 1$:**==
$$
T(k + 1) = (2k - 1) + 2 = 2k + 1
$$

同时，根据非递归公式:
==**Also, according to the non-recursive formula:**==
$$
T(k + 1) = 2(k + 1) - 1 = 2k + 2 - 1 = 2k + 1
$$

>[!note]conclusion
>We have thus shown that if the statement holds for k it holds for k + 1. In combination with
> our base case, and by the principle of mathematical induction, the statement holds for all
n ≥2.

所以，归纳步骤也成立。
**Therefore, the inductive step also holds.**

因此，根据数学归纳法，公式 $T(n) = 2n - 1$ 对所有正整数 $n$ 成立。
**Thus, by mathematical induction, the formula $T(n) = 2n - 1$ is valid for all positive integers $n$.**

这就是完整的中英对照的归纳法证明过程。

