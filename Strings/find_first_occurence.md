# Find the Index of the First Occurence in a String

> Given two strings needle and haystack, return the index of the first occurrence of needle in haystack, or -1 if needle is not part of haystack.

> Runtime 0ms

```python
def strStr(self, haystack: str, needle: str) -> int:
    nlen = len(needle)
    hlen = len(haystack)
    if nlen==1 and hlen==1:
        if needle==haystack:
            return 0
        else:
            return -1
    else:
        for i in range(hlen-nlen+1):
            if haystack[i:i+nlen]==needle:
                return i
    return -1
```
