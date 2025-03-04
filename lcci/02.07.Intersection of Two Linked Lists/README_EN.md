# [02.07. Intersection of Two Linked Lists](https://leetcode-cn.com/problems/intersection-of-two-linked-lists-lcci)

[中文文档](/lcci/02.07.Intersection%20of%20Two%20Linked%20Lists/README.md)

## Description
<p>Given two (singly) linked lists, determine if the two lists intersect. Return the inter&shy; secting node. Note that the intersection is defined based on reference, not value. That is, if the kth node of the first linked list is the exact same node (by reference) as the jth node of the second linked list, then they are intersecting.</p>



<p><strong>Example 1: </strong></p>



<pre>

<strong>Input: </strong>intersectVal = 8, listA = [4,1,8,4,5], listB = [5,0,1,8,4,5], skipA = 2, skipB = 3

<strong>Output: </strong>Reference of the node with value = 8

<strong>Input Explanation:</strong> The intersected node&#39;s value is 8 (note that this must not be 0 if the two lists intersect). From the head of A, it reads as [4,1,8,4,5]. From the head of B, it reads as [5,0,1,8,4,5]. There are 2 nodes before the intersected node in A; There are 3 nodes before the intersected node in B.</pre>



<p><strong>Example 2: </strong></p>



<pre>

<strong>Input: </strong>intersectVal = 2, listA = [0,9,1,2,4], listB = [3,2,4], skipA = 3, skipB = 1

<strong>Output: </strong>Reference of the node with value = 2

<strong>Input Explanation:</strong>&nbsp;The intersected node&#39;s value is 2 (note that this must not be 0 if the two lists intersect). From the head of A, it reads as [0,9,1,2,4]. From the head of B, it reads as [3,2,4]. There are 3 nodes before the intersected node in A; There are 1 node before the intersected node in B.</pre>



<p><strong>Example 3: </strong></p>



<pre>

<strong>Input: </strong>intersectVal = 0, listA = [2,6,4], listB = [1,5], skipA = 3, skipB = 2

<strong>Output: </strong>null

<strong>Input Explanation:</strong> From the head of A, it reads as [2,6,4]. From the head of B, it reads as [1,5]. Since the two lists do not intersect, intersectVal must be 0, while skipA and skipB can be arbitrary values.

<strong>Explanation:</strong> The two lists do not intersect, so return null.</pre>


<p><b>Notes:</b></p>

- If the two linked lists have no intersection at all, return&nbsp;<code>null</code>.
- The linked lists must retain their original structure after the function returns.
- You may assume there are no cycles anywhere in the entire linked structure.
- Your code should preferably run in O(n) time and use only O(1) memory.

## Solutions


<!-- tabs:start -->

### **Python3**

```python
# Definition for singly-linked list.
# class ListNode:
#     def __init__(self, x):
#         self.val = x
#         self.next = None

class Solution:
    def getIntersectionNode(self, headA: ListNode, headB: ListNode) -> ListNode:
        len1, len2 = self._length(headA), self._length(headB)
        if len1 < len2:
            headA, headB = headB, headA
        differ = abs(len1 - len2)
        for _ in range(differ):
            headA = headA.next
        while headA:
            if headA == headB:
                return headA
            headA = headA.next
            headB = headB.next
        return None

    def _length(self, node: ListNode) -> int:
        n = 0
        while node:
            node = node.next
            n += 1
        return n
```

### **Java**

```java
/**
 * Definition for singly-linked list.
 * public class ListNode {
 *     int val;
 *     ListNode next;
 *     ListNode(int x) {
 *         val = x;
 *         next = null;
 *     }
 * }
 */
public class Solution {
    public ListNode getIntersectionNode(ListNode headA, ListNode headB) {
        int len1 = len(headA), len2 = len(headB);
        int differ = Math.abs(len1 - len2);
        if (len1 < len2) {
            ListNode t = headA;
            headA = headB;
            headB = t;
        }
        while (differ-- > 0) {
            headA = headA.next;
        }
        while (headA != null) {
            if (headA == headB) {
                return headA;
            }
            headA = headA.next;
            headB = headB.next;
        }
        return null;
    }

    private int len(ListNode node) {
        int n = 0;
        while (node != null) {
            node = node.next;
            ++n;
        }
        return n;
    }
}
```

### **...**
```

```

<!-- tabs:end -->