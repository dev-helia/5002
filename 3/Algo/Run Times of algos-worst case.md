==log -> log2 ==
==忽略常数constant==
![[Pasted image 20241202152952.png]]
 -> algos runs on a list of length ... in times of ...
 -> asymtotic running time


### **Big O 表示法及复杂度整理表**

|**名称**|**复杂度表示法**|**特点/定义**|**常见算法**|**示例描述**|
|---|---|---|---|---|
|**常数时间**|O(1)O(1)|算法的运行时间不随输入规模变化，无论输入多大，时间都是固定的。|访问数组元素、哈希表查询|在数组中通过索引访问第一个元素，如 `arr[0]`。|
|**对数时间**|O(log⁡n)O(\log n)|输入规模每增加一倍，算法运行时间只增加一个常数；通常见于分治法。|二分查找、平衡二叉树搜索|从有序数组中找目标元素，逐步将范围减半，例如查找 50 的位置。|
|**线性时间**|O(n)O(n)|运行时间随输入规模呈线性增长。|遍历数组、线性查找|遍历列表中每个元素找出最大值。|
|**线性对数时间**|O(nlog⁡n)O(n \log n)|输入规模的线性增长与对数增长叠加，通常见于排序或复杂分治问题。|快速排序、归并排序|将数组按大小排序。|
|**平方时间**|O(n2)O(n^2)|运行时间随输入规模的平方增长，常见于嵌套循环。|冒泡排序、插入排序、矩阵乘法|对二维数组执行嵌套循环处理，例如检查两个列表中所有可能的组合。|
|**立方时间**|O(n3)O(n^3)|运行时间随输入规模的立方增长，常见于三重嵌套循环或复杂的矩阵问题。|矩阵链乘法、三重嵌套循环|计算三维矩阵的所有元素乘积。|
|**指数时间**|O(2n)O(2^n)|运行时间随输入规模呈指数增长，解决此类问题通常需要优化或近似算法。|汉诺塔问题、递归求解排列问题|在递归过程中生成所有可能的排列组合，例如解决旅行商问题（TSP）。|
|**阶乘时间**|O(n!)O(n!)|随输入规模增长，计算量迅速增长，几乎无法处理较大规模的问题。|排列生成、TSP最优解|生成一个集合的所有排列组合，例如为10个人分配座位。|

---

### **复杂度等级对比表**

|**复杂度**|**输入规模 nn**|**运行时间（假设每步耗时1ms）**|**实际意义**|
|---|---|---|---|
|O(1)O(1)|任意|1ms|无论输入多大，运行时间恒定。|
|O(log⁡n)O(\log n)|n=106n = 10^6|20ms|比线性时间快很多，用于搜索和查找算法。|
|O(n)O(n)|n=106n = 10^6|1秒|输入规模每增大1倍，运行时间相应增加1倍。|
|O(nlog⁡n)O(n \log n)|n=106n = 10^6|20秒|排序算法中常见复杂度，对大规模数据有较好的效率。|
|O(n2)O(n^2)|n=106n = 10^6|约11.6天|嵌套循环算法，适用于小规模问题；大规模数据需要优化。|
|O(2n)O(2^n)|n=20n = 20|1分钟|每增加一个输入，运行时间加倍；一般仅适用较小规模输入。|
|O(n!)O(n!)|n=20n = 20|超过240万年|只适用于非常小的输入规模；较大问题需要使用近似算法解决。|

---

### **常用算法的时间复杂度总结**

|**算法类型**|**最佳情况**|**最坏情况**|**平均情况**|
|---|---|---|---|
|**冒泡排序**|O(n)O(n)|O(n2)O(n^2)|O(n2)O(n^2)|
|**快速排序**|O(nlog⁡n)O(n \log n)|O(n2)O(n^2)|O(nlog⁡n)O(n \log n)|
|**归并排序**|O(nlog⁡n)O(n \log n)|O(nlog⁡n)O(n \log n)|O(nlog⁡n)O(n \log n)|
|**二分查找**|O(1)O(1)|O(log⁡n)O(\log n)|O(log⁡n)O(\log n)|
|**哈希查找**|O(1)O(1)|O(n)O(n)|O(1)O(1)|
|**线性查找**|O(1)O(1)|O(n)O(n)|O(n)O(n)|

---

### 通俗例子说明

- **O(1)**：拿钥匙开门，只需要一步。
- **O(\log n)**：用地图查找目的地，逐步缩小范围（如二分法）。
- **O(n)**：在一堆书中找目标书，逐本翻查。
- **O(n \log n)**：将书按分类排序。
- **O(n^2)**：比对每一本书与其他书的内容。

---

以上是整理好的表格内容！如果你需要我再讲解某个部分，或者补充细节，尽管告诉我~ 😊

![alt text](时间复杂度图.jpeg)

