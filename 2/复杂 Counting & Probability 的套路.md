### **通用思路总结**

这种题的套路都是：

1. 把问题拆成独立的选择步骤。
2. 每一独立的集合用组合公式 (nr)\binom{n}{r}(rn​) 表示可能性。
3. 互斥或者不互斥
4. 每一步的结果相乘，得到最终答案。 结合所有的
---
#### **分步法则（Multiplication Rule）**

**原理**：一个任务分为多个步骤完成，每步有不同选择数，最终总数等于每步选择数相乘。

- **例子**： 一个密码有 3 位，每位可以选 0-9（共 10 个数字），总共有： 10×10×10=1000 种可能性10 \times 10 \times 10 = 1000 \text{ 种可能性}

---

#### **排除法则（Complement Rule）**

**原理**：通过算“不发生”的概率，反推出“发生”的概率：

P(E)=1−P(not E)P(E) = 1 - P(\text{not E})

- **例子**： 抛掷一个 6 面骰子，至少出现一次 6 的概率： P(at least one 6)=1−P(no 6 at all)P(\text{at least one 6}) = 1 - P(\text{no 6 at all}) P(no 6 at all)=(56)nP(\text{no 6 at all}) = \left(\frac{5}{6}\right)^n，其中 nn 是骰子次数。

---

#### **独立事件的概率**

**原理**：多个事件之间互不干扰，事件 AA 和 BB 的概率：

P(A∩B)=P(A)×P(B)P(A \cap B) = P(A) \times P(B)

- **例子**： 抛掷两个骰子，出现两个“6”的概率是： P(6 on die 1)×P(6 on die 2)=16×16=136P(\text{6 on die 1}) \times P(\text{6 on die 2}) = \frac{1}{6} \times \frac{1}{6} = \frac{1}{36}

---

#### **总数公式**

- 对于大规模组合问题，使用排列和组合公式。
- **组合公式（无顺序）**： $C(n,r)=n!r!(n−r)!C(n, r) = \frac{n!}{r!(n-r)!}$
- **排列公式（有顺序）**： $P(n,r)=n!(n−r)!P(n, r) = \frac{n!}{(n-r)!}$

---
