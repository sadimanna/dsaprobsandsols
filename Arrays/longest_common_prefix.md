# Longest Common Prefix

> Write a function to find the longest common prefix string amongst an array of strings.
> If there is no common prefix, return an empty string "".

> Runtime 0ms | Memory 19.55 MB

```python
def longestCommonPrefix(self, strs: List[str]) -> str:
    if len(strs)==0:
        return ""
    elif len(strs)==1:
        return strs[0]
    min_l = 200
    for s in strs:
        slen = len(s)
        if slen < min_l:
            min_l = slen
    if min_l==0:
        return ""
    lcp = ''
    for i in range(min_l):
        for s in strs:
            if s[i] != strs[0][i]:
                return strs[0][:i]
        lcp+=strs[0][i]
    return lcp
```
