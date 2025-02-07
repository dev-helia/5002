Methods to represent graphs, such as adjacency lists or adjacency matrices. ---> Draw this graph in the plane so that no two edges intersect, except at common end vertices.
不是path 只是adjacency
![[Pasted image 20241203153550.png]]
![[Pasted image 20241203154014.png]]


![image-20241113180109625](image-20241113180109625.png)

1. **Adjacency List (邻接表)**： 无权重
   - 在 Python 中可以用字典表示。
   - 无权重（No Weight）的图表示：
     - $A$ - $B, D, E$
     - $B$ - $A, C, D$
     - $C$ - $B, D$
     - $D$ - $A, B, C, E$
     - $E$ - $A, D$

2. **Adjacency Matrix (邻接矩阵)**：无权重
   - 通过矩阵的形式表示顶点之间的连接关系。
   - 表格中 $1$ 表示两个顶点之间有边相连，$0$ 表示没有连接。
   
3. **Weighted Graph (带权图)**：无权重
   - 带有边权重的图表示，例如：
     - $A$ 到 $B$ 的权重为 $3$
     - $A$ 到 $E$ 的权重为 $1$
     - $B$ 到 $D$ 的权重为 $5$
     - $C$ 到 $D$ 的权重为 $1$
     - $D$ 到 $E$ 的权重为 $2$

