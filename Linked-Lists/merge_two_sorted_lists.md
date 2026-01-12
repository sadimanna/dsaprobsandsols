# Merge Two Sorted Lists

> You are given the heads of two sorted linked lists list1 and list2.
> Merge the two lists into one sorted list. The list should be made by splicing together the nodes of the first two lists.
> Return the head of the merged linked list.

>  Runtime 0ms | Memory 19.32 MB

```python
def mergeTwoLists(list1: Optional[ListNode], list2: Optional[ListNode]) -> Optional[ListNode]:
    res = ListNode()
    temp = res
    while list1 or list2:
        curr1 = list1.val if list1 else float('inf')
        curr2 = list2.val if list2 else float('inf')
        if curr1 < curr2:
            temp.next = list1
            list1 = list1.next
        else:
            temp.next = list2
            list2 = list2.next
        temp = temp.next
    return res.next
```
