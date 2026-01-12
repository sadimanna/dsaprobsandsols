> Given a string `s`, find the length of the longest substring without duplicate characters.

> Runtime 12ms | Memory 12.66MB

```python
def lengthOfLongestSubstring(s):
    """
    :type s: str
    :rtype: int
    """
    char_map = {}
    lp = 0
    max_length = 0
    for rp, char in enumerate(s):
        if char in char_map and char_map[char] >= lp:
            lp = char_map[char] + 1
        char_map[char] = rp
        max_length = max(max_length, rp - lp + 1) 
    return max_length
```
