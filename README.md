# Leetcode 练习记录
## 算法入门
### 二分查找
时间复杂度为**O(logn)**，适用于**顺序存储结构**，数据需**有序排列**
写二分法，区间的定义一般为两种，左闭右闭即[left, right]，或者左闭右开即[left, right)。

<br>第一种写法，我们定义 target 是在一个在左闭右闭的区间里，**也就是[left, right] （这个很重要非常重要）**。
有如下两点：
* while (left <= right) 要使用 <= ，因为left == right是有意义的，所以使用 <=
* if (nums[middle] > target) right 要赋值为 middle - 1，因为当前这个nums[middle]一定不是target，那么接下来要查找的左区间结束下标位置就是 middle - 1

<br>第二种写法，我们定义 target 是在一个在左闭右开的区间里，也就是[left, right) ，那么二分法的边界处理方式则截然不同。
有如下两点：
* while (left < right)，这里使用 < ,因为left == right在区间[left, right)是没有意义的
* if (nums[middle] > target) right 更新为 middle，因为当前nums[middle]不等于target，去左区间继续寻找，而寻找区间是左闭右开区间，所以right更新为middle，即：下一个查询区间不会去比较nums[middle]

##### Easy
[704. 二分查找](https://github.com/Lvma-0323/Leetcode/blob/main/704.%20%E4%BA%8C%E5%88%86%E6%9F%A5%E6%89%BE.md) 
<br>[35. 搜索插入位置](https://github.com/Lvma-0323/Leetcode/blob/main/35.%20%E6%90%9C%E7%B4%A2%E6%8F%92%E5%85%A5%E4%BD%8D%E7%BD%AE.md)
<br>[278. 第一个错误的版本](https://github.com/Lvma-0323/Leetcode/blob/main/278.%20%E7%AC%AC%E4%B8%80%E4%B8%AA%E9%94%99%E8%AF%AF%E7%9A%84%E7%89%88%E6%9C%AC.md)
<br>[69. Sqrt(x)](https://github.com/Lvma-0323/Leetcode/blob/main/69.%20Sqrt(x).md)
##### Medium
[34. Find First and Last Position of Element in Sorted Array](https://github.com/Lvma-0323/Leetcode/blob/main/34.%20Find%20First%20and%20Last%20Position%20of%20Element%20in%20Sorted%20Array.md)
<br>[153. Find Minimum in Rotated Sorted Array](https://github.com/Lvma-0323/Leetcode/blob/main/153.%20Find%20Minimum%20in%20Rotated%20Sorted%20Array.md)
<br>[33. Search in Rotated Sorted Array](https://github.com/Lvma-0323/Leetcode/blob/main/33.%20Search%20in%20Rotated%20Sorted%20Array.md)
<br>[74. Search a 2D Matrix](https://github.com/Lvma-0323/Leetcode/blob/main/74.%20Search%20a%202D%20Matrix.md)
<br>[162. Find Peak Element](https://github.com/Lvma-0323/Leetcode/blob/main/162.%20Find%20Peak%20Element.md)
##### Hard
[154. Find Minimum in Rotated Sorted Array II](https://github.com/Lvma-0323/Leetcode/blob/main/154.%20Find%20Minimum%20in%20Rotated%20Sorted%20Array%20II.md)

### 双指针
指的是在遍历对象的过程中，不是普通的使用单个指针进行访问，而是使用两个**相同方向（快慢指针）** 或者**相反方向（对撞指针）** 的指针进行扫描，从而达到相应的目的。
* 快慢指针：主要解决**链表**中的问题，比如典型的判定链表中是否包含环
* 对撞指针：主要解决**数组（或者字符串）** 中的问题，比如二分查找。
* 滑动窗口：主要解决一些查找满足一定条件的**连续区间**的性质（长度等）的问题。

##### Easy
[876. 链表的中间结点](https://github.com/Lvma-0323/Leetcode/blob/main/876.%20%E9%93%BE%E8%A1%A8%E7%9A%84%E4%B8%AD%E9%97%B4%E7%BB%93%E7%82%B9.md) 
<br> [977. 有序数组的平方](https://github.com/Lvma-0323/Leetcode/blob/main/977.%20%E6%9C%89%E5%BA%8F%E6%95%B0%E7%BB%84%E7%9A%84%E5%B9%B3%E6%96%B9.md) 
<br> [283. 移动零](https://github.com/Lvma-0323/Leetcode/blob/main/283.%20%E7%A7%BB%E5%8A%A8%E9%9B%B6.md) 
<br> [344. 反转字符串](https://github.com/Lvma-0323/Leetcode/blob/main/344.%20%E5%8F%8D%E8%BD%AC%E5%AD%97%E7%AC%A6%E4%B8%B2.md) 
<br> [557. 反转字符串中的单词 III](https://github.com/Lvma-0323/Leetcode/blob/main/557.%20%E5%8F%8D%E8%BD%AC%E5%AD%97%E7%AC%A6%E4%B8%B2%E4%B8%AD%E7%9A%84%E5%8D%95%E8%AF%8D%20III.md)
<br> [844. Backspace String Compare](https://github.com/Lvma-0323/Leetcode/blob/main/844.%20Backspace%20String%20Compare.md)

##### Medium
[19. 删除链表的倒数第 N 个结点](https://github.com/Lvma-0323/Leetcode/blob/main/19.%20%E5%88%A0%E9%99%A4%E9%93%BE%E8%A1%A8%E7%9A%84%E5%80%92%E6%95%B0%E7%AC%AC%20N%20%E4%B8%AA%E7%BB%93%E7%82%B9.md)
<br> [189. 旋转数组](https://github.com/Lvma-0323/Leetcode/blob/main/189.%20%E6%97%8B%E8%BD%AC%E6%95%B0%E7%BB%84.md) 
<br> [167. 两数之和 II - 输入有序数组](https://github.com/Lvma-0323/Leetcode/blob/main/167.%20%E4%B8%A4%E6%95%B0%E4%B9%8B%E5%92%8C%20II%20-%20%E8%BE%93%E5%85%A5%E6%9C%89%E5%BA%8F%E6%95%B0%E7%BB%84.md) 
<br> [3. 无重复字符的最长子串](https://github.com/Lvma-0323/Leetcode/blob/main/3.%20%E6%97%A0%E9%87%8D%E5%A4%8D%E5%AD%97%E7%AC%A6%E7%9A%84%E6%9C%80%E9%95%BF%E5%AD%90%E4%B8%B2.md)
<br> [567. 字符串的排列](https://github.com/Lvma-0323/Leetcode/blob/main/567.%20%E5%AD%97%E7%AC%A6%E4%B8%B2%E7%9A%84%E6%8E%92%E5%88%97.md)
<br> [15. 3Sum](https://github.com/Lvma-0323/Leetcode/blob/main/15.%203Sum.md)
<br> [82. Remove Duplicates from Sorted List II](https://github.com/Lvma-0323/Leetcode/blob/main/82.%20Remove%20Duplicates%20from%20Sorted%20List%20II.md)
<br> [986. Interval List Intersections](https://github.com/Lvma-0323/Leetcode/blob/main/986.%20Interval%20List%20Intersections.md)
<br> [11. Container With Most Water](https://github.com/Lvma-0323/Leetcode/blob/main/11.%20Container%20With%20Most%20Water.md)
<br> [438. Find All Anagrams in a String](https://github.com/Lvma-0323/Leetcode/blob/main/438.%20Find%20All%20Anagrams%20in%20a%20String.md)
<br> [713. Subarray Product Less Than K](https://github.com/Lvma-0323/Leetcode/blob/main/713.%20Subarray%20Product%20Less%20Than%20K.md)
<br> [209. Minimum Size Subarray Sum](https://github.com/Lvma-0323/Leetcode/blob/main/209.%20Minimum%20Size%20Subarray%20Sum.md)

### 广度优先搜索/深度优先搜索 (BFS/DFS)

<br> 广度优先搜索：我们每一次搜索到一个点的时候，如果这个点不符合条件，那么搜索同一层中符合条件的点，再把这一层中符合要求的点一一拓展，按照上述形式搜索下去。它需要借助一个**队列queue**来实现。
<br><br> Follow the below method to implement BFS traversal:
* Declare a queue and insert the starting vertex.
* Initialize a visited array and mark the starting vertex as visited.
* Follow the below process till the queue becomes empty:
* Remove the first vertex of the queue.
* Mark that vertex as visited.
* Insert all the unvisited neighbours of the vertex into the queue.

<br> 深度优先搜索：我们每一次搜索到一个点的时候，如果这个点不符合条件，那么就return，返回到上一层（就是常说的回朔），如果这个点符合条件，就一直搜索下去，直到没有点可以搜索。它是一个**递归**的过程，通常借助**栈stack**来实现。
<br><br> Follow the below steps to solve the problem:
* Create a recursive function that takes the index of the node and a visited array.
* Mark the current node as visited and print the node.
* Traverse all the adjacent and unmarked nodes and call the recursive function with the index of the adjacent node.

##### Easy
[617. 合并二叉树](https://github.com/Lvma-0323/Leetcode/blob/main/617.%20%E5%90%88%E5%B9%B6%E4%BA%8C%E5%8F%89%E6%A0%91.md)
<br> [733. 图像渲染](https://github.com/Lvma-0323/Leetcode/blob/main/733.%20%E5%9B%BE%E5%83%8F%E6%B8%B2%E6%9F%93.md)
##### Medium
[695. 岛屿的最大面积](https://github.com/Lvma-0323/Leetcode/blob/main/695.%20%E5%B2%9B%E5%B1%BF%E7%9A%84%E6%9C%80%E5%A4%A7%E9%9D%A2%E7%A7%AF.md)
<br> [116. 填充每个节点的下一个右侧节点指针](https://github.com/Lvma-0323/Leetcode/blob/main/116.%20%E5%A1%AB%E5%85%85%E6%AF%8F%E4%B8%AA%E8%8A%82%E7%82%B9%E7%9A%84%E4%B8%8B%E4%B8%80%E4%B8%AA%E5%8F%B3%E4%BE%A7%E8%8A%82%E7%82%B9%E6%8C%87%E9%92%88.md)
<br> [200. Number of Islands](https://github.com/Lvma-0323/Leetcode/blob/main/200.%20Number%20of%20Islands.md)
<br> [542. 01 矩阵](https://github.com/Lvma-0323/Leetcode/blob/main/542.%2001%20%E7%9F%A9%E9%98%B5.md)
<br> [994. 腐烂的橘子](https://github.com/Lvma-0323/Leetcode/blob/main/994.%20%E8%85%90%E7%83%82%E7%9A%84%E6%A9%98%E5%AD%90.md)


### 递归/回溯
##### 递归：基本思想就是把规模大的问题转化为规模小的相似的子问题来解决。 三要素：明确递归终止条件；给出递归终止时的处理办法；提取重复的逻辑，缩小问题规模。
[21. 合并两个有序链表](https://github.com/Lvma-0323/Leetcode/blob/main/21.%20%E5%90%88%E5%B9%B6%E4%B8%A4%E4%B8%AA%E6%9C%89%E5%BA%8F%E9%93%BE%E8%A1%A8.md)
<br> [206. 反转链表](https://github.com/Lvma-0323/Leetcode/blob/main/206.%20%E5%8F%8D%E8%BD%AC%E9%93%BE%E8%A1%A8.md)
##### 回溯：把问题的解空间转化成了图或者树的结构表示，然后使用深度优先搜索策略进行遍历，遍历的过程中记录和寻找所有可行解或者最优解。
[77. 组合](https://github.com/Lvma-0323/Leetcode/blob/main/77.%20%E7%BB%84%E5%90%88.md)
