# Plus One

> You are given a large integer represented as an integer array digits, where each digits[i] is the ith digit of the integer.
> The digits are ordered from most significant to least significant in left-to-right order.
> The large integer does not contain any leading 0's.
> Increment the large integer by one and return the resulting array of digits.

```python
def plusOne(self, digits: List[int]) -> List[int]:
    carry = 0
    for i in range(len(digits)-1, -1, -1):
        if i==len(digits)-1:
            if digits[i]==9:
                digits[i]=0
                carry = 1
            else:
                digits[i]+=1
                break
        else:
            if carry==1:
                if digits[i]==9:
                    digits[i]=0
                else:
                    digits[i]+=1
                    carry=0
                    break
    if carry==1:
        digits.insert(0, carry)
    return digits



```
