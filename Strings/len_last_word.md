# Length of Last Word

> Given a string s consisting of words and spaces, return the length of the last word in the string.

```python
def lengthOfLastWord(self, s: str) -> int:
    return len(s.rstrip(' ').split(' ')[-1])
```
