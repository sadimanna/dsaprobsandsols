# Valid Parenthesis

> Given a string s containing just the characters '(', ')', '{', '}', '[' and ']', determine if the input string is valid.

> An input string is valid if:

> - Open brackets must be closed by the same type of brackets.
> - Open brackets must be closed in the correct order.
> - Every close bracket has a corresponding open bracket of the same type.

> Runtime 3 ms

```python
def isValid(self, s):
    """
    :type s: str
    :rtype: bool
    """
    closing = [')', '}', ']']
    opening = ['(', '{', '[']
    bracket_dict = dict(zip(closing, opening))
    len_s = len(s)
    if len_s==1:
        return False
    elif len_s==0:
        return True
    stack = [s[0]]
    for i in range(1,len_s):
        if s[i] in closing:
            if len(stack)>0 and bracket_dict[s[i]]==stack[-1]:
                stack.pop()
            else:
                return False
        else:
            stack.append(s[i])
    if len(stack) > 0:
        return False
    return True
```
