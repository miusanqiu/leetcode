# [面试题27. 二叉树的镜像](https://leetcode-cn.com/problems/er-cha-shu-de-jing-xiang-lcof/)

## 题目描述
请完成一个函数，输入一个二叉树，该函数输出它的镜像。

例如输入：

```
     4
   /   \
  2     7
 / \   / \
1   3 6   9
```

镜像输出：

```
     4
   /   \
  7     2
 / \   / \
9   6 3   1
```

**示例 1：**

```
输入：root = [4,2,7,1,3,6,9]
输出：[4,7,2,9,6,3,1]
```

**限制：**

- `0 <= 节点个数 <= 1000`

## 解法
<!-- tabs:start -->

### **Python3**
```python
# Definition for a binary tree node.
# class TreeNode:
#     def __init__(self, x):
#         self.val = x
#         self.left = None
#         self.right = None

class Solution:
    def mirrorTree(self, root: TreeNode) -> TreeNode:
        if root is None or (root.left is None and root.right is None):
            return root
            
        self.mirrorTree(root.left)
        self.mirrorTree(root.right)
        root.left, root.right = root.right, root.left
        return root
```

### **Java**
```java
/**
 * Definition for a binary tree node.
 * public class TreeNode {
 *     int val;
 *     TreeNode left;
 *     TreeNode right;
 *     TreeNode(int x) { val = x; }
 * }
 */
class Solution {
    public TreeNode mirrorTree(TreeNode root) {
        if (root == null || (root.left == null && root.right == null)) {
            return root;
        }
        mirrorTree(root.left);
        mirrorTree(root.right);
        TreeNode t = root.left;
        root.left = root.right;
        root.right = t;
        return root;
    }
}
```

### **JavaScript**
```js
/**
 * Definition for a binary tree node.
 * function TreeNode(val) {
 *     this.val = val;
 *     this.left = this.right = null;
 * }
 */
/**
 * @param {TreeNode} root
 * @return {TreeNode}
 */
var mirrorTree = function(root) {
    function dfs(node) {
        if(!node) return null
        let left = dfs(node.left)
        let right = dfs(node.right)
        node.left = right
        node.right = left
        return node
    }
    return dfs(root)
};
```

### **Go**

```go
func mirrorTree(root *TreeNode) *TreeNode {
    if root == nil {
        return root
    }
    root.Left, root.Right = root.Right, root.Left
    root.Left = mirrorTree(root.Left)
    root.Right = mirrorTree(root.Right)
    return root
}
```



### **...**

```

```

<!-- tabs:end -->