
# 在一个有 $n$ 个顶点的完全图中，边的数量是 $|E| = \frac{n(n-1)}{2}$，其中 $n \in \mathbb{Z}^+$。

**命题**：在一个有 $n$ 个顶点的完全图中，边的数量是 $|E| = \frac{n(n-1)}{2}$，其中 $n \in \mathbb{Z}^+$。

### 证明 (Proof) - 数学归纳法 (Induction)

1. **基例 (Base Case)**：当 $n = 1$ 时，$|E| = \frac{1 \times 0}{2} = 0 \quad \checkmark$，这个情况成立。

2. **归纳假设 (Inductive Hypothesis)**：假设对于某个 $n$ 值，$E(n) = \frac{n(n-1)}{2}$ 成立。

3. **归纳步骤 (Inductive Step)**：
   - 证明 $E(n+1) = \frac{(n+1)n}{2}$ 也成立。
   - 计算 $E(n+1)$：$E(n+1) = \frac{n(n-1)}{2} + n$
   - 化简得到：$= \frac{n^2 + n}{2} = \frac{n(n+1)}{2}$

   因此，$E(n+1) = \frac{n(n+1)}{2}$ 成立。

4. **结论**：通过数学归纳法证明了命题对所有 $n \in \mathbb{Z}^+$ 都成立。

---
# Handshake Lemma (握手引理)

**握手引理**：具有奇数度数的顶点数量是偶数。

- 公式：$\sum \text{degree}(V) = 2|E|$

- 可以拆分为：$\sum_{\text{even}} \text{degree}(V_1) + \sum_{\text{odd}} \text{degree}(V_2)$

- 总和为偶数，因为 $\sum \text{degree}(V) = 2|E|$ 是偶数。

因此，奇数度数的顶点数量必须为偶数，以保持总和为偶数。



