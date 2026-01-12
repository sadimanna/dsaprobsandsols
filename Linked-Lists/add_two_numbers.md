# Add Two Numbers

> You are given two non-empty linked lists representing two non-negative integers.
> The digits are stored in reverse order, and each of their nodes contains a single digit.
> Add the two numbers and return the sum as a linked list.
> You may assume the two numbers do not contain any leading zero, except the number 0 itself.

> Runtime: 0ms | Memory: 19.30 MB

```python
# Definition for singly-linked list.
# class ListNode(object):
#     def __init__(self, val=0, next=None):
#         self.val = val
#         self.next = next
def addTwoNumbers(l1, l2):
    """
    :type l1: Optional[ListNode]
    :type l2: Optional[ListNode]
    :rtype: Optional[ListNode]
    """
    carry = 0
    res = ListNode()
    temp = res
    while l1 or l2:
        curr1 = l1.val if l1 else 0
        curr2 = l2.val if l2 else 0
        val = curr1 + curr2 + carry
        carry = val//10
        val = val%10
        temp.next = ListNode(val, None)
        temp = temp.next
        l1 = l1.next if l1 else None
        l2 = l2.next if l2 else None
    if carry:
        temp.next = ListNode(carry,  None)
        
    return res.next
```
