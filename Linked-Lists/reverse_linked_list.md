# Reverse Linked List

> Given the head of a singly linked list, reverse the list, and return the reversed list.

> Runtime 0 ms | Memory 14.16 MB

```python
# Definition for singly-linked list.
class ListNode(object):
    def __init__(self, val=0, next=None):
        self.val = val
        self.next = next

def reverseList(head):
    """
    :type head: Optional[ListNode]
    :rtype: Optional[ListNode]
    """
    if head is None:
        return None
    if head.next is None:
        return head
    next_node = ListNode(head.val, None)
    temp = ListNode(head.val, None)
    head.val = head.next.val
    head.next = head.next.next
    while head.next != None:
        temp = ListNode(head.val,next_node)
        next_node = temp
        head.val = head.next.val
        head.next = head.next.next
    temp = ListNode(head.val, next_node)
    head = temp
    return head
```


