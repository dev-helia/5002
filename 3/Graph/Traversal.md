==Starting at vertex a traverse the graph by...processing the neighbors of
each vertex in the order they appear on the adjacency list of that vertex (thus not in the
alphabetical order). In your drawing, color the tree edges in red and next to each vertex write
its place in the order in which the vertices are first visited (with a as 1).==
==can be with spanning tree==

---
# depth-first-search

![image-20241113180726445](image-20241113180726445.png)

![image-20241113180741980](image-20241113180741980.png)

![[Pasted image 20241203162207.png]]
B → A, A → C, C → F, F → D, D → H, H → E, E → G, G → I

---

# breadth-First Search

![image-20241113180800640](image-20241113180800640.png)

![image-20241113180814982](image-20241113180814982.png)

---

# Dijkstra
![[Pasted image 20241203163205.png]]![[Pasted image 20241203163213.png]]

### **为什么看起来像“走回头路”？**

Dijkstra 算法计算的不是**路径顺序**，而是**从起点到各个顶点的最短距离**。所以，即使最终路径看起来有“回头”的情况，这些“回头”是算法在更新距离时计算出来的，而不是真正去实际走这些回头路！

### **回头路是怎么回事？**

以 `B → I → A` 和其他路径为例：

1. **第一步**：
    
    - 从起点 `B` 出发，`B → A = 21`，`B → I = 11`。
    - 这时，`I` 的距离被更新为 11，但 `A` 已经通过直接路径 `B → A` 确定为 21。
2. **第二步**：
    
    - 到达 `I` 后，虽然有路径 `I → A = 23`，但加上权重 `B → I + I → A = 11 + 23 = 34`，比直接路径 `B → A = 21` 长，所以不会更新 `A` 的距离。
3. **为什么顺序是 `B → I → A`？**
    
    - **注意：这只是算法的顺序问题**。算法依次访问顶点，并尝试更新邻居的距离，但最终只会记录从起点到每个顶点的**最短路径**。

### **Dijkstra 算法处理“回头”的原则**

1. **访问顺序≠最终路径**：
    
    - 算法按顺序访问每个顶点，但最终记录的是最短距离，不是实际行走的顺序。
2. **贪心原则**：
    
    - 每次选择当前最短路径的顶点，尝试更新其他顶点的距离。
    - 如果新路径比已知最短路径长，就不会更新。
### **总结**

- **为什么会有 `B → I → A` 这样的顺序？**
    
    - 这是算法的访问顺序，不是最终的路径。
    - 算法尝试从 `I` 更新 `A`，发现绕路更长，所以保持 `B → A` 的直接路径。
- **最终的最短路径**：
    
    - 从起点到各顶点的最短路径不会受“回头路”影响。
