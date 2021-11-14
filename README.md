# Leetcode 练习记录
## 算法入门
#### 二分查找
时间复杂度为**O(logn)**，适用于**顺序存储结构**，数据需**有序排列**
* 简单二分查找：
<br> [704. 二分查找](https://github.com/Lvma-0323/Leetcode/blob/main/704.%20%E4%BA%8C%E5%88%86%E6%9F%A5%E6%89%BE.md) 
<br> [35. 搜索插入位置](https://github.com/Lvma-0323/Leetcode/blob/main/35.%20%E6%90%9C%E7%B4%A2%E6%8F%92%E5%85%A5%E4%BD%8D%E7%BD%AE.md)
* 寻找右侧边界的二分查找: 
<br> [278. 第一个错误的版本](https://github.com/Lvma-0323/Leetcode/blob/main/278.%20%E7%AC%AC%E4%B8%80%E4%B8%AA%E9%94%99%E8%AF%AF%E7%9A%84%E7%89%88%E6%9C%AC.md)

#### 双指针
指的是在遍历对象的过程中，不是普通的使用单个指针进行访问，而是使用两个**相同方向（快慢指针）** 或者**相反方向（对撞指针）** 的指针进行扫描，从而达到相应的目的。
* 快慢指针：主要解决**链表**中的问题，比如典型的判定链表中是否包含环
<br> [876. 链表的中间结点](https://github.com/Lvma-0323/Leetcode/blob/main/876.%20%E9%93%BE%E8%A1%A8%E7%9A%84%E4%B8%AD%E9%97%B4%E7%BB%93%E7%82%B9.md) 
<br> [19. 删除链表的倒数第 N 个结点](https://github.com/Lvma-0323/Leetcode/blob/main/19.%20%E5%88%A0%E9%99%A4%E9%93%BE%E8%A1%A8%E7%9A%84%E5%80%92%E6%95%B0%E7%AC%AC%20N%20%E4%B8%AA%E7%BB%93%E7%82%B9.md)
* 对撞指针：主要解决**数组（或者字符串）** 中的问题，比如二分查找。
<br> [977. 有序数组的平方](https://github.com/Lvma-0323/Leetcode/blob/main/977.%20%E6%9C%89%E5%BA%8F%E6%95%B0%E7%BB%84%E7%9A%84%E5%B9%B3%E6%96%B9.md) 
<br> [189. 旋转数组](https://github.com/Lvma-0323/Leetcode/blob/main/189.%20%E6%97%8B%E8%BD%AC%E6%95%B0%E7%BB%84.md) 
<br> [283. 移动零](https://github.com/Lvma-0323/Leetcode/blob/main/283.%20%E7%A7%BB%E5%8A%A8%E9%9B%B6.md) 
<br> [167. 两数之和 II - 输入有序数组](https://github.com/Lvma-0323/Leetcode/blob/main/167.%20%E4%B8%A4%E6%95%B0%E4%B9%8B%E5%92%8C%20II%20-%20%E8%BE%93%E5%85%A5%E6%9C%89%E5%BA%8F%E6%95%B0%E7%BB%84.md) 
<br> [344. 反转字符串](https://github.com/Lvma-0323/Leetcode/blob/main/344.%20%E5%8F%8D%E8%BD%AC%E5%AD%97%E7%AC%A6%E4%B8%B2.md) 
<br> [557. 反转字符串中的单词 III](https://github.com/Lvma-0323/Leetcode/blob/main/557.%20%E5%8F%8D%E8%BD%AC%E5%AD%97%E7%AC%A6%E4%B8%B2%E4%B8%AD%E7%9A%84%E5%8D%95%E8%AF%8D%20III.md)
* 滑动窗口：主要解决一些查找满足一定条件的**连续区间**的性质（长度等）的问题。
<br> [3. 无重复字符的最长子串](https://github.com/Lvma-0323/Leetcode/blob/main/3.%20%E6%97%A0%E9%87%8D%E5%A4%8D%E5%AD%97%E7%AC%A6%E7%9A%84%E6%9C%80%E9%95%BF%E5%AD%90%E4%B8%B2.md)
<br> [567. 字符串的排列](https://github.com/Lvma-0323/Leetcode/blob/main/567.%20%E5%AD%97%E7%AC%A6%E4%B8%B2%E7%9A%84%E6%8E%92%E5%88%97.md)

#### 广度优先搜索/深度优先搜索 (BFS/DFS)
深度优先搜索和广度优先搜索，都是图形搜索算法
* 广度优先搜索：我们每一次搜索到一个点的时候，如果这个点不符合条件，那么搜索同一层中符合条件的点，再把这一层中符合要求的点一一拓展，按照上述形式搜索下去。它需要借助一个**队列queue**来实现。
<br> [733. 图像渲染](https://github.com/Lvma-0323/Leetcode/blob/main/733.%20%E5%9B%BE%E5%83%8F%E6%B8%B2%E6%9F%93.md)
<br> [542. 01 矩阵](https://github.com/Lvma-0323/Leetcode/blob/main/542.%2001%20%E7%9F%A9%E9%98%B5.md)
* 深度优先搜索：我们每一次搜索到一个点的时候，如果这个点不符合条件，那么就return，返回到上一层（就是常说的回朔），如果这个点符合条件，就一直搜索下去，直到没有点可以搜索。它是一个**递归**的过程，通常借助**栈stack**来实现。
<br> [695. 岛屿的最大面积](https://github.com/Lvma-0323/Leetcode/blob/main/695.%20%E5%B2%9B%E5%B1%BF%E7%9A%84%E6%9C%80%E5%A4%A7%E9%9D%A2%E7%A7%AF.md)
<br> [617. 合并二叉树](https://github.com/Lvma-0323/Leetcode/blob/main/617.%20%E5%90%88%E5%B9%B6%E4%BA%8C%E5%8F%89%E6%A0%91.md)
<br> [116. 填充每个节点的下一个右侧节点指针](https://github.com/Lvma-0323/Leetcode/blob/main/116.%20%E5%A1%AB%E5%85%85%E6%AF%8F%E4%B8%AA%E8%8A%82%E7%82%B9%E7%9A%84%E4%B8%8B%E4%B8%80%E4%B8%AA%E5%8F%B3%E4%BE%A7%E8%8A%82%E7%82%B9%E6%8C%87%E9%92%88.md)
