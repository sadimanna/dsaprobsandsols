# Length of Last Word

> Given a string s consisting of words and spaces, return the length of the last word in the string.

```python
def lengthOfLastWord(self, s: str) -> int:
    splitted_str = s.rstrip(' ').split(' ')
    return len(splitted_str[-1])
```
