# [1564. Put Boxes Into the Warehouse I](https://leetcode.com/problems/put-boxes-into-the-warehouse-i)

[中文文档](/solution/1500-1599/1564.Put Boxes Into the Warehouse I/README.md)

## Description

<p>Given two arrays of positive integers&nbsp;<code>boxes</code>&nbsp;and&nbsp;<code>warehouse</code>&nbsp;representing the heights of some boxes&nbsp;of unit width, and the heights of <code>n</code>&nbsp;rooms in a warehouse, respectively.&nbsp;The warehouse&#39;s&nbsp;rooms are labeled from&nbsp;<code data-stringify-type="code">0</code>&nbsp;to&nbsp;<code data-stringify-type="code">n - 1</code>&nbsp;from left to right where&nbsp;<code data-stringify-type="code">warehouse[i]</code>&nbsp;(0-indexed) is the height of the&nbsp;<code data-stringify-type="code">i<sup>th</sup></code>&nbsp;room.</p>

<p>Boxes are put into the warehouse by the following rules:</p>

<ul>
	<li>Boxes can&#39;t be piled up.</li>
	<li>You can rearrange the order of the boxes.</li>
	<li>Boxes&nbsp;can only be pushed into the warehouse from left to right only.</li>
	<li>If the height of some room&nbsp;in the warehouse is less than the height of a box, then the box will be stopped before that room, so are the boxes&nbsp;behind it.</li>
</ul>

<p>Return <em>the maximum number of boxes you can put into the warehouse.</em></p>

<p>&nbsp;</p>
<p><strong>Example 1:</strong></p>

<p><strong><img alt="" src="https://assets.leetcode.com/uploads/2020/08/26/11.png" style="width: 400px; height: 242px;" /></strong></p>

<pre>
<strong>Input:</strong> boxes = [4,3,4,1], warehouse = [5,3,3,4,1]
<strong>Output:</strong> 3
<strong>Explanation:&nbsp;
</strong><img alt="" src="https://assets.leetcode.com/uploads/2020/08/26/12.png" style="width: 280px; height: 242px;" />
We can first put the box of height 1 in room 4. Then we can put the box of height 3 in either of the 3 rooms 1, 2, or 3. Lastly, we can put one box of height 4 in room 0.
There is no way we can fit all 4 boxes in the warehouse.</pre>

<p><strong>Example 2:</strong></p>

<p><strong><img alt="" src="https://assets.leetcode.com/uploads/2020/08/26/21.png" style="width: 400px; height: 202px;" /></strong></p>

<pre>
<strong>Input:</strong> boxes = [1,2,2,3,4], warehouse = [3,4,1,2]
<strong>Output:</strong> 3
<strong>Explanation: 
<img alt="" src="https://assets.leetcode.com/uploads/2020/08/26/22.png" style="width: 280px; height: 202px;" />
</strong>Notice that it&#39;s not possible to put the box of height 4 into the warehouse since it cannot pass the first room of height 3.
Also, for the last two rooms, 2 and 3, only boxes of height 1 can fit.
We can fit 3 boxes maximum as shown above. The yellow box can also be put in room 2 instead.
Swapping the orange and green boxes is also valid, or swapping one of them with the red box.</pre>

<p><strong>Example 3:</strong></p>

<pre>
<strong>Input:</strong> boxes = [1,2,3], warehouse = [1,2,3,4]
<strong>Output:</strong> 1
<strong>Explanation: </strong>Since the first room in the warehouse is of height 1, we can only put boxes of height 1.
</pre>

<p><strong>Example 4:</strong></p>

<pre>
<strong>Input:</strong> boxes = [4,5,6], warehouse = [3,3,3,3,3]
<strong>Output:</strong> 0
</pre>

<p>&nbsp;</p>
<p><strong>Constraints:</strong></p>

<ul>
	<li><code>n == warehouse.length</code></li>
	<li><code>1 &lt;= boxes.length, warehouse.length &lt;= 10^5</code></li>
	<li><code>1 &lt;= boxes[i], warehouse[i] &lt;= 10^9</code></li>
</ul>


## Solutions



<!-- tabs:start -->

### **Python3**


```python

```

### **Java**


```java

```

### **...**
```

```

<!-- tabs:end -->